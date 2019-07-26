# NULL-AND-DUPLICATE-VALUES
CODE FOR NULL VALUES AND DUPLICATE ROWS

FOR SEEING NO OF NULL VALUES PRESENT IN A COLUMN
DF AND NULLD IS THE DATAFRAME

    df.isnull().sum()
  
 
    s=df.isnull().sum()
    s[s>0]
    
    
    nulld = df.isnull().sum()/len(df)
    nulld = nulld[nulld > 0]
    nulld.sort_values(inplace=True)
    nulld
    
 COLUMNS WHICH CONTAINS STRING AND DATATYPE IS OBJECT
    
    v=[f for f in df.columns if df.dtypes[f] == 'object']
    v
    
 CODE FOR SEEING COUNTS OF UNIQUE VALUES IN COLUMN FIREPLACE
 
    df['FireplaceQu'].value_counts()
   
 CODE FOR SEEEING ROWS WHICH ARE NULL IN COLUMN BSMTQUAL
    
    df[df['BsmtQual'].isnull()==True]
    
 FOR FILLING NULL VALUES WITH NO BASEMENT
    
    df["BsmtExposure"].fillna("No Basement", inplace = True) 
  
  FOR FILLING -1 VALUE WITH NAN VALUES
  
    df.replace(-1,np.nan,inplace=True)    
    
 FOR SEEING COLUMNS WHICH HAVE DATATYPE OBJECT
    
    col=df.select_dtypes(include=['object'])
    col.info()
    #col
    
RemoveS rows which had null values in all columns  

    df[df['Loan ID'].isnull()==True]

    
