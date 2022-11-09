
https://app.datacamp.com/workspace/w/9e59f442-f125-4f47-b3af-d1167fe6151d


Data Analyst Associate Case Study Submission
To begin we will import packages for analysis and visulaizations, then we can load our data.

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df = pd.read_csv('pet_sales.csv')
df
product_id
product_category
sales
price
vendor_id
pet_size
pet_type
rating
re_buy
0
5040
Equipment
$123,000
94.81
VC_1605
small
fish
7
1
1
4567
Toys
$61,000
120.95
VC_1132
small
cat
10
0
2
4237
Toys
$218,000
106.34
VC_802
small
hamster
6
0
3
4364
Snack
$69,000
241.27
VC_929
large
dog
1
1
4
4184
Supplements
$138,000
133.68
VC_749
large
dog
10
0
5
4609
Bedding
$183,000
51.6
VC_1174
large
cat
10
0
6
4380
Toys
$79,000
175.75
VC_945
extra_small
dog
8
0
7
4389
Bedding
$205,000
170.01
VC_954
large
cat
9
0
8
4697
Supplements
$116,000
178.11
VC_1262
small
cat
10
0
9
4238
Medicine
$141,000
248.07
VC_803
medium
dog
10
1
Data Validation
This sales data includes a unique product and its features. The data has been grouped by product ID already and we can assume sales data has been aggregated over some period of time.

Data validation is one of the first steps in analysis because it sets us on the right track to gain insights into the data we expect to be working with.

Given the instructions, we know what each column of data is suppose to be. The following table shows what was done to best fit the instructions and my ability to analyze the data.

Column Name	Data Type	Validation Process
Product ID	Character	converted ID data into string format from integer.
Product Category	Character	confirmed every string was one of 11 product category values.
Sales	Numeric	using regex, filtered $000,000 format to remove '$' and ',' symbols before converting to a numeric data type.
Price	Numeric	confirmed the price was in numeric(float) format which is best for analysis.
Vendor ID	Character	confirmed the data was in string format
Pet Size	Character	validated that all record contain 1 of 5 sizes
Pet Type	Character	removed the records containing pet types other than “cat”, “dog”, “fish”, “bird”.
Rating	Numeric	confirmed all values were between 1-10
Rebuy	Binary	confirmed binary nature of all values, they were kept 0 or 1 to allow for further analysis
Validation Tasks
Correcting data types
# product id into string
df.product_id = df['product_id'].astype(str)

# sales into number
df['sales'] = df.sales.replace({'\$':'',',':''},regex=True).astype(float)

df.info()

# FIXED: Now our data is in the correct data type
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 879 entries, 0 to 878
Data columns (total 9 columns):
 #   Column            Non-Null Count  Dtype  
---  ------            --------------  -----  
 0   product_id        879 non-null    object 
 1   product_category  879 non-null    object 
 2   sales             879 non-null    float64
 3   price             879 non-null    float64
 4   vendor_id         879 non-null    object 
 5   pet_size          879 non-null    object 
 6   pet_type          879 non-null    object 
 7   rating            879 non-null    int64  
 8   re_buy            879 non-null    int64  
dtypes: float64(2), int64(2), object(5)
memory usage: 61.9+ KB
Removing unwanted pets
# create unwanted subset
unwanted = ['hamster', 'rabbit']

# filter out unwanted subset and return values and frequency
df = df[df.pet_type.isin(unwanted) == False]
df.pet_type.value_counts()

# FIXED: removed the records containing pets other than “cat”, “dog”, “fish”, “bird”.
cat     347
dog     347
fish     70
bird     69
Name: pet_type, dtype: int64
Check data for accidental duplicates
For example, a value may be misspelled and incorrectly counted as a different value ('smell' instead of 'small')

This could happen to numbers too

We will check categorical columns because they must only contain a certain set of expected values unlike ID or sales data.

# creat subset for categorical columns
dup_check = [ 'product_category',  'pet_size', 'pet_type', 'rating']

# loop through categorical columns to check if real values match our expectation
for col in df[dup_check]:
  print(col, f'has {df[col].unique().size} values:', df[col].unique())
product_category has 11 values: ['Equipment' 'Toys' 'Snack' 'Supplements' 'Bedding' 'Medicine' 'Housing'
 'Food' 'Clothes' 'Accessory' 'Grooming']
pet_size has 5 values: ['small' 'large' 'extra_small' 'medium' 'extra_large']
pet_type has 4 values: ['fish' 'cat' 'dog' 'bird']
rating has 10 values: [ 7 10  1  8  9  3  6  5  4  2]
Looks good!

How many products are being purchased more than once?
This requires a simple count of the values (1 or 0) in our re_buy column

Data Discovery
Key Business Insights
390 (47%) of the products are being purchased more than once. The majority are purchased only once.

On average, products purchased again sell for more. However, one time purchased products generate more total sales.

In order, the products most likely to be purchased again are as follows: fish housing, dog bedding, cat food and bird accessories

This is how I approached the business questions that I answered above...

print(df['re_buy'].value_counts())
0    443
1    390
Name: re_buy, dtype: int64
# pie chart to visualize number of products purchased more than once
dfr = pd.DataFrame(df.groupby(['re_buy'])['product_id'].count())
colors = sns.color_palette('colorblind')[0:33]

plt.pie(dfr.product_id, labels = ['One Time - 443', 'Re Buy - 390'], colors = colors, autopct='%.0f%%')
plt.show()

Within our data, 390 products (47%) are purchased more than once. Most are purchased only once (53%).
Business Questions cont.
Do the products being purchased again have better sales than others?
Initially, my hypothesis is that something that is repeatedly purchased must be driving up the sales higher as people buy it. I think they should make more money than products purchased only once.

I will begin by analyzing sales total: re-buy vs once

# grouping by re-buy, returning the total sales for each
df_sales_sum = pd.DataFrame(df.groupby(['re_buy'])['sales'].sum())

print(df_sales_sum)
             sales
re_buy            
