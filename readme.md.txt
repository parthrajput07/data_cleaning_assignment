Data Cleaning Assignment Summary

For this assignment I have used Python and Pandas library to perform tasks on Combined_Dataset.csv ecommerse dataset.

1. Imported the pandas library using - import pandas as pd

2. I then loaded the dataset into a Pandas DataFrame using - 
   df = pd.read_csv("Combined_dataset.csv")
   This also aloowed the CSV data to be processed in tabular form.

3. I explored the dataset using -
df.head()
df.shape
df.columns
df.dtypes
df.info()
Using these functions my understanding of the data became clear.

4. I then identified missing values using - df.isnull().sum() 
This showed me number of null values present in each column.

5. Then I created a copy using df_clean = df.copy to ensure that any change in the dataset does not affect the original dataset. 

6.Then missing values were filled using function fillna() 

7.Then I check for any duplicate records using df_clean.dupliacted().sum()
In my dataset no duplicate value was found

8.Then I performed basic operations like selecting specific columns and filtering basic records on some conditions.

9.Then I created a derived column named discount_amount using - 
  df_clean["discount_amount"] = (
      df_clean["initial_price"] * df_clean["discount"] / 100
  )
  This calculated the discount value for each product.

10. Then the cleaned dataset is saved as a new CSV file using- 
    df_clean.to_csv("cleaned_ecommerce_dataset.csv", index=False)

 

 
