# Python_DataScience
# Learning Matplotlib and Seaborn libraries.


Convert number string with commas to float object
        https://thispointer.com/python-convert-string-float/
        
For choropleth, make sure the data type of z parameter - when its string, covert it to float:

1. If column is number with commas in between:
        df1['Column_Name'].apply(lambda x : x.replace(',','') ).astype(float)
2. If not, simply convert the data type to float:
        df1['Column_Name'].astype(float)
Or, can use (if column has numbers , but there are some random strings as well):
        pd.to_numeric(df1['Column_Name'], errors = 'coerce')     
        # adding errors = 'coerce' will convert strings to NaN.
        # and, later NaN can be replaced using replace(np.nan,0)
        
    

