# EX:6 DATA VISUALIZATION USING SEABORN LIBRARY

# AIM:
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

          import pandas as pd
          import seaborn as sns
          import matplotlib.pyplot as plt
          df=pd.read_csv("titanic_dataset.csv")
          df.head()

![328475114-79f4819c-dfc3-4906-84c0-9e03ce115c32](https://github.com/user-attachments/assets/578be36c-05f6-485b-906a-3b733143edab)

LINE PLOT


          x=[1,2,3,4,5]
          y=[3,6,2,7,1]
          sns.lineplot(x=x,y=y)
          plt.title('Line Plot')

![328475177-68a63045-f6dc-4229-bc53-e4e4e71b14f5](https://github.com/user-attachments/assets/6a61e223-9951-4b74-81d4-dc8ea4cb57f4)

MULTI LINE PLOT

          x=[1,2,3,4,5]
          y1=[3,5,2,6,1]
          y2=[1,6,4,3,8]
          y3=[5,2,7,1,4]
          sns.lineplot(x=x,y=y1)
          sns.lineplot(x=x,y=y2)
          sns.lineplot(x=x,y=y3)
          plt.title('Multi Line Plot')
                      
![328475234-aae1a706-a5b2-41ed-bd91-3bfde2f18fae](https://github.com/user-attachments/assets/a71bd193-53a2-4262-a2e6-8c1b95d968b8)

TO VISUALIZE RELATIONSHIPS

BAR CHART

          plt.figure(figsize=(8,5))
          sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
          plt.title("Fare Of Passenger By Embarked Town")

![328475304-5b1aa904-42d7-47dc-8ad2-9803d35a864f](https://github.com/user-attachments/assets/751a88c1-b5d7-4193-a44d-daea962bd45b)


SCATTER PLOT

          sns.scatterplot(x="Age", y="Fare", data=df)
          plt.title('Scatterplot of Age vs Fare')
          plt.show()

![328475366-c7ad7761-a406-4582-931f-ad1515696c58](https://github.com/user-attachments/assets/125eebd7-5902-44a1-b109-5b8efc0737de)

TO CAPTURE DISTRIBUTIONS

HISTOGRAM

          sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)

![328475479-a5f69477-e68b-4892-b3cd-965610b7faef](https://github.com/user-attachments/assets/add2d75d-30fb-445a-bc26-bfab5951000c)


BOX PLOT

          sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
          plt.title("Age By Passenger Class")


![328475542-0caa044f-a411-49e8-b05e-66cf67c49383](https://github.com/user-attachments/assets/5de46787-acc9-4b89-b29b-0b1bcaaf407f)


VIOLIN PLOT

          sns.violinplot(x="Pclass", y="Fare", data=df)
          plt.title('Violin Plot of Fare by Passenger Class')
          plt.show()

![328475591-b725d969-8c14-4cfc-9ef8-80035a388b93](https://github.com/user-attachments/assets/402109ff-6112-4145-80e9-556df0f8b8bd)

DENSITY PLOT


          sns.kdeplot(data=df['Age'], shade=True)
          plt.title('Density Plot of Passenger Ages')
          plt.show()

![328475671-2da67e4d-d184-4c90-8859-cca668c52057](https://github.com/user-attachments/assets/5d2a077c-f6fd-4759-85b1-9c1c36ceb719)

HEATMAP

          numeric_df = df.select_dtypes(include=['float64', 'int64'])
          corr_matrix = numeric_df.corr()
          sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
          plt.title('Heatmap of Titanic Dataset')
          plt.show()
          
![328475785-5cc6be20-4ef3-4db4-86fd-5eb9f9299a0d](https://github.com/user-attachments/assets/aa068982-23c9-4e62-a1a9-f3deac0c72b9)




# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully
