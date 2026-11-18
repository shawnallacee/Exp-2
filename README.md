# Experiment 2: Data Visualization Using Matplotlib and Seaborn

## Aim

To visualize data using Matplotlib and Seaborn libraries.

## Algorithm

1.  **Start.**
2.  Import the Matplotlib and Seaborn libraries.
3.  Load data into a Pandas DataFrame.
4.  Plot a histogram for age distribution using `plt.hist()`.
5.  Plot a scatter plot for Age vs. Salary using `sns.scatterplot()`.
6.  Plot salary distribution using `sns.boxplot()`.
7.  Show the plots sequentially.
8.  **Stop.**


## Program
import matplotlib.pyplot as plt  
import numpy as np  
import pandas as pd    
import seaborn as sns    

\# Set a random seed for reproducibility    
np.random.seed(42)  

\# Load data into a Pandas DataFrame (simulating an employee dataset)    
print("--- 1. Dataset Initialization ---")    
data = {    
    "Age": np.random.randint(22, 60, 100),  
    "Salary": np.random.randint(35000, 130000, 100),  
}  
df = pd.DataFrame(data)    
print("First 5 rows of the DataFrame:")  
print(df.head())  

\# Set seaborn style for better aesthetics  
sns.set_theme(style="whitegrid")  

\# Create a figure to hold the sequential/subplot visualizations    
plt.figure(figsize=(15, 5))  

\# Plot a histogram for age distribution using plt.hist()  
plt.subplot(1, 3, 1)  
plt.hist(df["Age"], bins=8, color="skyblue", edgecolor="black")  
plt.title("Age Distribution (Histogram)")  
plt.xlabel("Age")        
plt.ylabel("Frequency")    
  
\# Plot a scatter plot for Age vs. Salary using sns.scatterplot()  
plt.subplot(1, 3, 2)  
sns.scatterplot(  
    x="Age", y="Salary", data=df, color="purple", alpha=0.8, edgecolor="w"  
)  
plt.title("Age vs. Salary (Scatter Plot)")  
plt.xlabel("Age")  
plt.ylabel("Salary ($)")  

\# Plot salary distribution using sns.boxplot()  
plt.subplot(1, 3, 3)  
sns.boxplot(y=df["Salary"], color="lightgreen")  
plt.title("Salary Distribution (Box Plot)")  
plt.ylabel("Salary ($)")  

\# Show the plots sequentially / layout adjustment  
plt.tight_layout()  
print(    
    "\n--- 2. Plots Rendered Successfully ---"  
    "\n(Histograms, scatter plots, and box plots displayed)"  
)  
plt.show()  


## output
<img width="1367" height="697" alt="image" src="https://github.com/user-attachments/assets/841bdcf8-ee98-4c8d-8579-e251ad0afbf2" />


## result
Thus to visualize data using Matplotlib and Seaborn libraries successfully.

