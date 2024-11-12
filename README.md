# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

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
```
```
sns.violinplot(x="day",y="total_bill",hue="smoker",data=tip,linewidth=2,width=0.6,palette="Set3",inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/6e3cf1ae-87df-442d-b2ad-0ce6d0e1eac8)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/7cb579d1-ee2c-4661-85f7-d6b5e5dc0201)

```
import seaborn as sns
sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/1ebe337f-4d53-436b-a570-1f5e4b44ad49)

```
import seaborn as sns
# use to set style of background of plot
sns.set(style="whitegrid")
# loading data-set
tips = sns.load_dataset("tips")
sns.violinplot(x="tip",y="day",data=tip)
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/0fc01e14-1ccb-444d-b9ba-20ec145212ba)

```
sns.kdeplot(data=tips,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set2',alpha=0.8)
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/ed91a715-74ca-4582-817e-5b84a8b1ba5a)
```
import seaborn as sns
import matplotlib.pyplot as plt
```
```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
```
```
sns.lineplot(x=x,y=y)
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/466cd021-e330-4a2e-9e02-69ee465432ef)

```
df=sns.load_dataset("tips")
```
```
df
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/89d48040-9a76-423b-a76a-b2e7f452ce9b)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue="sex",linestyle='solid',legend="auto")
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/cab73f90-2257-42fd-9271-809db7c8b872)

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
```
```
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title("Multi-Line Plot")
plt.xlabel("X Label")
plt.ylabel("y Label")
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/92591c63-d333-4609-842f-be1719201696)

```
import seaborn as sns
import matplotlib.pyplot as plt
tips=sns.load_dataset("tips")
avg_total_bill=tips.groupby("day")["total_bill"].mean()
avg_tip=tips.groupby("day")["tip"].mean()
```
```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label="Total Bill")
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label="Tip")
plt.xlabel("Day of the Week")
plt.ylabel("Amount")
plt.title("Average Total Bill and Tip by Day")
plt.legend()
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/711f9c79-4bb6-4067-a8e7-2d5610328396)

```
avg_total_bill=tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time')['tip'].mean()
```

```
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill',width=0.4)
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip',width=0.4)
plt.xlabel('Time of Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Time of Day')
plt.legend()
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/d38db932-954e-4a58-a890-623d70a38c77)

```
years=range(2000,2012)
apples=[0.895,0.91,0.919,0.926,0.929,0.931,0.934,0.936,0.937,0.9375,0.9372,0.939]
oranges=[0.962,0.941,0.930,0.923,0.918,0.908,0.907,0.904,0.901,0.898,0.9,0.896]
```
```
plt.bar(years,apples)
plt.bar(years,oranges,bottom=apples)
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/0eca0181-7c05-40ec-82d1-89ab37ef8cf5)

```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the week')
plt.ylabel('Total Bill')
plt.title('Total Bill by Day and Gender')
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/54997f32-1700-47af-aebc-bb6b5e50e611)
```
import seaborn as sns
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/dc042326-5769-475f-9715-f4c865ba9da1)

```
import seaborn as sns
import numpy as np
import pandas as pd

```

```
np.random.seed(1)
num_var=np.random.randn(1000)
num_var=pd.Series(num_var,name="Numerical variable")
num_var
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/078f56ba-87f5-45eb-9f57-ae453f864666)
```
sns.histplot(data=num_var,kde=True)
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/d654b09e-8565-47e5-999a-bec754a4ec0c)

```
import seaborn as sns
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt

```
```
np.random.seed(0)
marks=np.random.normal(loc=70,scale=10,size=100)
```

```
marks
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/d1a67767-a6c4-4781-bc4d-4d0dea43b1fc)
```
sns.histplot(data=marks,bins=10,kde=True,stat='count',cumulative=False,multiple='stack',element='bars',palette='Set1',shrink=0.7)
plt.xlabel('Marks')
plt.ylabel('Density')
plt.title('Histogram of Students Marks')
```

![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/f9cf9d08-e1d8-460a-961f-491998dfb311)

```
import seaborn as sns
import pandas as pd
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'],y=tips['total_bill'],hue=tips['sex'])
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/29ec26cc-e51c-4e68-8ccd-8266ab5fbebc)

```
sns.boxplot(x='day',y='total_bill',hue='smoker',data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"lightblue","edgecolor":"darkblue"},
whiskerprops={"color":"black","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
![image](https://github.com/Jeevapriya14/EXNO-6-DS/assets/121003043/79bb879c-7db8-46cc-808d-ff269323fa58)


























# Result:
 Thus, the implementation of data visualization using seaborn library has been successfully executed.
