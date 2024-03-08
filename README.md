# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
## Data cleaning
<table>
  <tr>
    <td width=50%>

### 1) Read and display DataFrame
```Python
import pandas as pd
df=pd.read_csv("/content/SAMPLEIDS.csv")
df
```
  </td>
  <td>
              
#### OUTPUT:

![ee1](https://github.com/silambarasan2004/exno1/assets/119559917/183060b7-b837-4c62-96cb-1099c4836c5e)




</td>
</tr>
<tr>
  <td width=50%>
              
### 2) Display head
```Python
df.head(3)
```
  </td>
  <td>

              
#### OUTPUT:

![e1](https://github.com/silambarasan2004/exno1/assets/119559917/48941fad-c506-4ef0-9bae-a562124a33e1)


</td>
</tr>
<tr>
  <td width=50%>

### 3) Display tail
```Python
df.tail(3)
```
  </td>
  <td>
              
#### OUTPUT:

![e2](https://github.com/silambarasan2004/exno1/assets/119559917/cdbf2fab-f1dd-4e13-819b-6069757f68fc)


</td>
</tr>
<tr>
  <td width=50%>

### 4) Info of datafram
```Python
df.info()
```
  </td>
  <td>
              
#### OUTPUT:

![e3](https://github.com/silambarasan2004/exno1/assets/119559917/a186d673-2c43-4feb-b585-a100e2dc4244)



</td>
</tr>
<tr>
  <td width=50%>

### 5) Describe about the dataframe
```Python
df.describe()
```
  </td>
  <td>
              
#### OUTPUT:

![e4](https://github.com/silambarasan2004/exno1/assets/119559917/4529ad5b-e4dc-4820-a3a2-cca559af6fb4)



</td>
</tr>
<tr>
  <td width=50%>

### 6) Shape of the datafram
```Python
df.shape
```
  </td>
  <td>
              
#### OUTPUT:

![e5](https://github.com/silambarasan2004/exno1/assets/119559917/0f5dae52-3ff7-4b16-839a-d36c5346a976)


</td>
</tr>
<tr>
  <td width=50%>

### 7) Checking tha NUll values
```Python
df.isnull().sum()
```
  </td>
  <td>
              
#### OUTPUT:

![e6](https://github.com/silambarasan2004/exno1/assets/119559917/17c18e4d-e987-41d2-b5be-730ab8c49517)


</td>
</tr>
<tr>
  <td width=50%>

### 8) Drop the Null values
```Python
df.nunique()

```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-03-08 110722](https://github.com/silambarasan2004/exno1/assets/119559917/1e56d410-8fe5-4a68-b5cf-8c46504535a2)


</td>
</tr>
<tr>
  <td width=50%>

### 9) Finding the mean value
```Python
mn=df.TOTAL.mean()
mn
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-03-08 110804](https://github.com/silambarasan2004/exno1/assets/119559917/ce60b3c7-c6c0-4080-81fa-907abab8d05c)



</td>
</tr>
<tr>
  <td width=50%>

### 10) Fill Null value with Mean value
```Python
df.TOTAL.fillna(mn,inplace=True)
df
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-03-08 110834](https://github.com/silambarasan2004/exno1/assets/119559917/c8aeb491-0d32-4ed5-9633-2d818cf76120)



</td>
</tr>
<tr>
  <td width=50%>
    
### 11) Finding minimum value
```Python
mn=df.M3.min()
mn
```
  </td>
  <td>
              
#### OUTPUT:


![Screenshot 2024-03-08 111152](https://github.com/silambarasan2004/exno1/assets/119559917/75ab6384-6d91-4e7b-a84e-404e612b8161)




</td>
</tr>
<tr>
  <td width=50%>

### 12) Printing only Date of Birth
```Python
df['cd']=pd.to_datetime(df['DOB'])
df['cd']
```
  </td>
  <td>
              
#### OUTPUT:

![Screenshot 2024-03-08 111323](https://github.com/silambarasan2004/exno1/assets/119559917/c09aa757-5bd6-4425-ae05-bfd87a976985)




</td>
</tr>
<tr>
  <td width=50%>

# Result:
  Thus the program for data cleaning using python has executed successfully.
