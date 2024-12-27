
# NumPy and Pandas 🚀  
 

## NumPy  📊  

### 1. Installing NumPy 🛠️  
To get started, install NumPy using pip:  
```bash  
pip install numpy  
```  

---  

### 2. Creating Arrays and Performing Basic Operations 📏  

#### Creating a NumPy Array  
```python  
import numpy as np  

# Create an array from a list  
a = np.array([1, 2, 3])  
b = np.array((1, 2, 3))  
print(a)  # Output: [1 2 3]  
print(b)  # Output: [1 2 3]  

# Modify an element  
b[1] = 4  
print(b)  # Output: [1 4 3]  
```  

#### Multi-dimensional Arrays  
```python  
c = np.array([[1, 2, 3], [4, 5, 6]])  
print(c)  
# Output:  
# [[1 2 3]  
#  [4 5 6]]  
```  

#### Slicing and Indexing  
```python  
print(c[0])      # First row: [1 2 3]  
print(c[:1])     # First row using slicing: [[1 2 3]]  
print(c[:, 1:])  # Slicing from 1st column to the end: [[2 3] [5 6]]  
```  

---  

### 3. Array Creation Methods 🛠️  

#### Zeros and Ones Arrays  
```python  
a = np.zeros((3, 4))  # 3x4 array of zeros  
print(a)  
```  
Output:  
```
[[0. 0. 0. 0.]  
 [0. 0. 0. 0.]  
 [0. 0. 0. 0.]]  
```  

#### Range and Arange  
```python  
a = np.arange(10, 25, 5)  # Start, stop, step  
print(a)  # Output: [10 15 20]  
```  

#### Linspace  
```python  
b = np.linspace(5, 7, 11)  # Generate 11 numbers between 5 and 7  
print(b)  
```  
Output:  
```
[5.  5.2 5.4 5.6 5.8 6.  6.2 6.4 6.6 6.8 7. ]  
```  

#### Random Arrays  
```python  
d = np.random.random((3, 4))  # Random numbers between 0 and 1  
print(d)  
```  
Output:  
```
[[0.1338468  0.9186682  0.11899144 0.52624798]  
 [0.76680892 0.35966834 0.42790354 0.71934597]  
 [0.03181066 0.57729023 0.71955814 0.41275151]]  
```  

---  

### 4. Array Manipulation and Reshaping 🛠️  

#### Reshaping Arrays  
```python  
a = np.array([[1, 2, 3], [4, 5, 6]])  
print(a.shape)      # (2, 3)  
a.shape = (3, 2)  
print(a)             # Output: [[1 2] [3 4] [5 6]]  
print(a.shape)       # Shape: (3, 2)  
```  

#### Flattening Arrays  
```python  
a = np.arange(24)  # 0 to 23  
print(a.size)      # Output: 24  
```  

---  

### 5. Basic Array Operations 🛠️  

#### Sum, Subtract, Multiply, Divide  
```python  
a = np.array([5, 10])  
b = np.array([2, 3])  
print(np.sum([a, b]))        # Output: 20  
print(np.subtract(a, b))     # Output: [3 7]  
print(np.multiply(a, b))     # Output: [10 30]  
print(np.divide(a, b))       # Output: [2.5 3.33]  
```  

#### Trigonometric Functions  
```python  
print(np.cos(a))             # Output: [ 0.28366219 -0.83907153]  
```  

---  

### 6. Indexing and Slicing 🛠️  

#### Multi-dimensional Slicing  
```python  
a = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])  
print(a[:1, 1:])  # [[2 3]]  
```  

#### Concatenation  
```python  
b = np.array([[3, 4, 5], [5, 6, 7]])  
print(np.concatenate([a, b], axis=0))  # Vertical concatenation  
print(np.concatenate([a, b], axis=1))  # Horizontal concatenation  
```  

---  

### 7. Statistical Operations 🛠️  

#### Sum, Min, Max, Mean, Standard Deviation  
```python  
a = np.array([[1, 2, 3], [4, 5, 6]])  
print(np.sum(a))       # Output: 21  
print(np.min(a))       # Output: 1  
print(np.max(a))       # Output: 6  
print(np.mean(a))      # Output: 3.5  
print(np.std(a))       # Output: 1.7078  
```  

#### Correlation Coefficient  
```python  
print(np.corrcoef(a))  # Output: Correlation matrix  
```  

---  

### 8. Broadcasting 🛠️  

#### Arrays with Different Shapes  
```python  
a = np.array([[1, 2, 3], [4, 5, 6]])  
b = np.array([3, 4, 5])  
print(np.sum([a, b]))  # Broadcasting works  
```  

---  

### 9. Creating & Manipulating Datatypes 🛠️  

#### Changing Data Types  
```python  
a = np.array([1, 2, 3, 4, 5])  
print(a.dtype)   # int64  
b = a.astype('U')  # Change to string  
print(b.dtype)    # Output: U11  
```  

---  

### 10. Sorting Arrays 🛠️  

```python  
a = np.array([50, 40, 10, 20, 30])  
print(np.sort(a))    # Output: [10 20 30 40 50]  

b = np.array([[50, 40, 30], [20, 10, 90]])  
print(np.sort(b, axis=0))  # Sorting by column  
print(np.sort(b))          # Sorting by row  
```  

---  

### 11. Random Operations 🛠️  

#### Random Integer and Shuffle  
```python  
x = np.random.randint(1, 5, 10)  # Random integers between 1 and 4  
print(np.unique(x))               # Find unique values  
np.random.shuffle(x)              # Shuffle array  
```  

#### Clip Values  
```python  
x = np.random.randint(1, 10, 10)  
print(np.clip(x, 5, 6))  # Clip values between 5 and 6  
```  

---  

## Pandas 📘  

### 1. Installing Pandas 🛠️  
To get started, install Pandas using pip:  
```bash  
pip install pandas  
```  

---  

### 2. Reading and Inspecting Data 📊  

#### Loading Data  
```python  
import pandas as pd  

# Load the dataset  
df = pd.read_excel("list_Marks.xlsx")  
print(df.head())  # Show first few rows  
```  

#### Inspecting Data  
```python  
print(df.info())  # Get info about the dataframe  
print(df.describe())  # Summary statistics  
```  

---  

### 3. Data Cleaning 🧼  

#### Handling Missing Values  
```python  
df.dropna(inplace=True)  # Remove rows with missing values  
df.fillna("MISSING", inplace=True)  # Fill missing values  
```  

---  

### 4. Data Selection and Manipulation 🔍  

#### Selecting Columns and Rows  
```python  
# Select a specific column  
print(df['Maths'])  

# Select specific rows  
print(df.loc[0])  # First row  
print(df.iloc[0])  # First row by position  
```  

#### Filtering Data  
```python  
# Filter rows where marks in Maths > 50  
filtered_df = df[df['Maths'] > 50]  
```  

---  

### 5. Grouping and Aggregation 🛠️  

#### Grouping by Subject and Aggregating  
```python  
grouped = df.groupby('Subject').mean()  # Mean marks by subject  
print(grouped)  
```  

#### Summarizing Data  
```python  
print(df['Maths'].mean())  # Mean of Maths marks  
```  

---  

### 6. Exporting Data 🖨️  

#### Saving to Excel  
```python  
df.to_excel("cleaned_data.xlsx", index=False)  # Save cleaned data to a new Excel file  
```  

---  

## Conclusion 🏁  

This guide covered fundamental operations, array creation, manipulation, and statistical functions using NumPy and Pandas. By mastering these libraries, you’ll be able to handle numerical computations and structured data efficiently in Python. Let me know if you need further help or clarifications! 
