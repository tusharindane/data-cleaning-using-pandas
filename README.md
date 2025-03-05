import pandas as pd
import matplotlib.pyplot as plt

# Load the Titanic dataset (Ensure 'train.csv' is in the same directory)
df = pd.read_csv("train.csv")

# Plot Age Distribution (Histogram)
plt.figure(figsize=(8, 5))
plt.hist(df['Age'].dropna(), bins=20, color='skyblue', edgecolor='black')
plt.xlabel("Age")
plt.ylabel("Number of Passengers")
plt.title("Age Distribution of Titanic Passengers")
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()

# Plot Gender Distribution (Bar Chart)
gender_counts = df['Sex'].value_counts()
plt.figure(figsize=(6, 5))
plt.bar(gender_counts.index, gender_counts.values, color=['blue', 'pink'], edgecolor='black')
plt.xlabel("Gender")
plt.ylabel("Number of Passengers")
plt.title("Gender Distribution of Titanic Passengers")
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()
