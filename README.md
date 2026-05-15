#EX.NO:1
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
```
     import pandas as pd
     df=pd.read_csv('D:Data_set (1).csv')
     print(df)
     print(data)   
     
     df.describe()
     
     df=pd.DataFrame(df)
     print(df.isnull())
     
     import pandas as pd
     data = pd.read_csv("C:/Users/acer/Downloads/Data_set (1).csv")
     df = pd.DataFrame(data)
    dfd = df.dropna()
    print("AFTER DROPNA")
    print(dfd)

     dfd = df.dropna(axis=1)
     print("AFTER DROPNA")
     print(dfd)

     dfd=df.dropna(axis=1,inplace=True)

     print("AFTER DROPNA") dfd=df.dropna(axis=0)
     print("AFTER DROPNA")
     print(dfd)

     import pandas as pd
     # Read the dataset
     data = pd.read_csv("C:/Users/acer/Downloads/Data_set (1).csv")
     # Convert into DataFrame
     df = pd.DataFrame(data)
     # Fill missing values using forward fill method
     dfd = df.fillna(method="ffill")
     # Display output
     print("AFTER FILLNA")
     print(dfd)

     import pandas as pd
     import matplotlib.pyplot as plt
     import numpy as np
     data = pd.read_csv("C:/Users/acer/Downloads/iris.csv")
      df = pd.DataFrame(data)
     print(df)
     x = df["petal_length"]
     y = df["sepal_length"]
     plt.hist(x)
    plt.show()
    plt.hist(y)
    plt.show()

    import pandas as pd
    import matplotlib.pyplot as plt
    import numpy as np
    data = pd.read_csv("iris.csv")
    df = pd.DataFrame(data)
    print(df)
    x = df["petal_length"]
    y = df["sepal_length"]
    plt.xlabel('X-axis')
    plt.ylabel('Y-axis')
    plt.plot(x, y)
    plt.show()

    import pandas as pd
    import matplotlib.pyplot as plt
    import numpy as np
    # Read dataset
    data = pd.read_csv("iris.csv")
     # Convert into DataFrame
    df = pd.DataFrame(data)
    # Display dataset
     print(df)
     # Create boxplot
     dff = plt.boxplot(df["petal_width"])
     # Display graph
     plt.show()
     print(dff)

     \import pandas as pd
     import numpy as np
     from scipy import stats
    data = pd.read_csv("iris.csv")
    df = pd.DataFrame(data)
    z_scores = np.abs(stats.zscore(df.select_dtypes(include=[np.number])))
    df_cleaned = df[(z_scores < 3).all(axis=1)]
    print(df_cleaned)

    import pandas as pd
    import numpy as np
    data = pd.read_csv("C:/Users/acer/Downloads/iris (1).csv")
    df = pd.DataFrame(data)
    Q1 = df["sepal_width"].quantile(0.25)
    Q3 = df["sepal_width"].quantile(0.75)
    IQR = Q3 - Q1
    lower_bound = Q1 - 1.5 * IQR
    upper_bound = Q3 + 1.5 * IQR
    print("The Original DataSet")
    print(df)
    outliers = df[
    (df['sepal_width'] < lower_bound) |
    (df['sepal_width'] > upper_bound)
    ]
    print("The Outliers")
    print(outliers)
    df_clean = df[
    (df['sepal_width'] >= lower_bound) &
    (df['sepal_width'] <= upper_bound)
    ]
    print("The Dataset after removing the outliers")
    print(df_clean)
    ```
```
<img width="609" height="661" alt="image" src="https://github.com/user-attachments/assets/ba1a10f0-4b06-4ab3-957f-35fc5976992a" />

<img width="609" height="236" alt="image" src="https://github.com/user-attachments/assets/1adbe2b2-132b-4079-9d1a-17b44496a60d" />

<img width="672" height="449" alt="image" src="https://github.com/user-attachments/assets/cedb25e6-c14c-4f8c-b45d-a484179de58f" /> 

<img width="702" height="674" alt="image" src="https://github.com/user-attachments/assets/f42db5c1-6bea-4021-8c06-4c93acd7f592" />

<img width="471" height="254" alt="image" src="https://github.com/user-attachments/assets/67ab9c97-7383-4237-80ea-cc3ff5a4fb02" />

<img width="635" height="59" alt="image" src="https://github.com/user-attachments/assets/8fa4dadc-060b-495b-b682-7dd1f55be09a" />

<img width="806" height="397" alt="image" src="https://github.com/user-attachments/assets/69bd8701-97a4-4e81-abc5-745351cd26ae" />
<img width="426" height="264" alt="image" src="https://github.com/user-attachments/assets/a82620f8-d46a-4f82-ab97-c0117fefb103" /> 

<img width="698" height="671" alt="image" src="https://github.com/user-attachments/assets/2aeb2fb7-50b4-40f8-9426-d065a1368519" /> 

<img width="565" height="882" alt="image" src="https://github.com/user-attachments/assets/8a457d27-4394-43ac-b9c5-83b85704bb7c" />

<img width="604" height="580" alt="image" src="https://github.com/user-attachments/assets/71bc77d7-b4e4-436d-b5d0-853cf2a902d2" />

<img width="916" height="643" alt="image" src="https://github.com/user-attachments/assets/d6b31f89-69d2-43f7-a717-1f398eeb6381" />

<img width="608" height="217" alt="image" src="https://github.com/user-attachments/assets/29a18aff-a01e-451f-b601-6d757649f5a6" />

<img width="605" height="521" alt="image" src="https://github.com/user-attachments/assets/f4e04c31-bc98-4824-af1d-2ec144caee88" />
            
# Result
THUS DATA CLEANING IS PERFORMED
