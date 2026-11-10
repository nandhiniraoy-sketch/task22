# Task 22 -- GroupBy Fundamentals

## Objective

Learn Pandas `groupby()` to summarize data.

## Program

``` python
import pandas as pd

data={
"Department":["IT","HR","Finance","IT","HR","Finance","IT","HR"],
"Employee":["A","B","C","D","E","F","G","H"],
"Salary":[50000,40000,60000,55000,45000,65000,70000,48000],
"Experience":[2,3,5,4,2,6,7,3]
}
df=pd.DataFrame(data)
print(df)

print(df.groupby("Department")["Salary"].sum())
print(df.groupby("Department")["Salary"].mean())
print(df.groupby("Department")["Employee"].count())
print(df.groupby("Department")["Salary"].min())
print(df.groupby("Department")["Salary"].max())
print(df.groupby(["Department","Experience"])["Salary"].sum())
print(df.groupby("Department")["Salary"].agg(["sum","mean","count","min","max"]))
```

## Concepts

-   groupby()
-   sum()
-   mean()
-   count()
-   min()
-   max()
-   agg()

## Conclusion

GroupBy helps summarize data category-wise and is essential for
exploratory data analysis.

## Author

Jessie
