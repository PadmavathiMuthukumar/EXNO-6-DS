# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY
# REGISTER NUMBER: 212223040141
# NAME: PADMAVATHI M
# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```
![image](https://github.com/user-attachments/assets/748e12ac-7a2e-4825-9c04-09e362cb6973)
```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/8ec0a0eb-93b9-4d49-945b-6e2085477990)
![image](https://github.com/user-attachments/assets/23e8b855-2582-49ff-8a2f-9ee1d14aac36)
```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```
![image](https://github.com/user-attachments/assets/6f234ec4-350a-4c29-999c-352dc8f3ae73)
```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```
![image](https://github.com/user-attachments/assets/35808753-b818-47c0-8563-cabab13c816d)
```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/4e8a43a6-1787-4a86-b784-f35a7e5f0fbc)
```
avg_total_bill = tips.groupby('time')['total_bill'].mean() 
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```
![image](https://github.com/user-attachments/assets/b4269204-899b-4a51-9f4e-a570f3e629f2)
```
years=range(2000, 2012)
apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939] 
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]
plt.bar(years, apples)
plt.bar(years, oranges, bottom=apples)
```
![image](https://github.com/user-attachments/assets/6d0b010b-4bbd-4a37-88a3-a6a22b0603ea)
```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/user-attachments/assets/ec7ae5d0-cc5f-4992-b1e5-8be9577bbce7)
```
tit=pd.read_csv("titanic_dataset.csv")
tit
```
![image](https://github.com/user-attachments/assets/f870af0a-d5fe-4a29-b8ba-a124f57e8937)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow') 
plt.title("Fare of Passenger by Embarked Town")
```
![image](https://github.com/user-attachments/assets/48b8ee2a-3124-4086-b70a-1bf9ac47cb5a)
```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass') 
plt.title("Fare of Passenger by Embarked Town, Divided by Class")
```
![image](https://github.com/user-attachments/assets/83ef5736-d423-4e08-9abb-66f943f545e1)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/92d90cb7-db08-45d6-bb6c-92f23bd3f90e)
```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/63464dfa-6dfa-4f2a-8fc1-6e681a826982)
```
sns.histplot(data = num_var, kde = True)
```
![image](https://github.com/user-attachments/assets/7295edfc-d12a-4f8b-b96c-3efcb1ca5ffa)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/126e6089-edb0-4831-b8e5-b9cb2683c485)
```
df=pd.read_csv("titanic_dataset.csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```
![image](https://github.com/user-attachments/assets/1935b790-d575-4e47-a2d9-0dfca5b05c9e)
```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/1cea17b5-fcdb-45b0-a177-629ba4cf7de9)
```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```
![image](https://github.com/user-attachments/assets/4d04a49a-d874-441d-97e0-5802c047ebb1)
```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/b2b6525a-6716-402f-aca8-a3c7acc35c2c)
```
mart=pd.read_csv("titanic_dataset.csv")
mart
```
![image](https://github.com/user-attachments/assets/58fc8c33-b5ff-416f-8250-6b502b2459ef)
```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']] 
mart.head(10)
```
![image](https://github.com/user-attachments/assets/c20012fb-a370-4610-acfb-55e972206ea0)
```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/90bc3945-a284-4f49-9ae2-513dd0397c4f)
```
import seaborn as sns
import pandas as pd

# Assuming 'mart' is your DataFrame
mart=pd.read_csv("titanic_dataset.csv")
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]

sns.kdeplot(data=mart, x='Age')
```
![image](https://github.com/user-attachments/assets/10834569-6803-4eef-ab77-3a574cdbeae9)
```
sns.kdeplot(data=mart)
```
![image](https://github.com/user-attachments/assets/6e8ac23c-76e8-4989-9567-f18b2f57faa2)
```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```
![image](https://github.com/user-attachments/assets/7e563c63-9738-495e-9e91-8e7696996358)
```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```
![image](https://github.com/user-attachments/assets/55421d1b-08ea-404d-9558-6799865fcb66)
```
import numpy as np  # Import numpy and assign it the alias 'np'
import seaborn as sns

data = np.random.randint(low=1, high=100, size=(10, 10))  # Now np is defined and can be used
hm = sns.heatmap(data=data, annot=True)
```
![image](https://github.com/user-attachments/assets/5bd35a57-f935-4041-a026-75d6ca9025b1)
```
hm=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/bc3a4ac9-5838-4e1c-8e92-09ecc15d7a5c)

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.


