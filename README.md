# Kaggle Competition - Mercedes-Benz Greener Manufacturing 
<img src="https://github.com/saptakbhadra/mercedesbenzKgle/blob/master/MercedesKaggle.PNG" alt=".." title="Mercedes Benz"/>
[Official Website](https://www.kaggle.com/c/mercedes-benz-greener-manufacturing/overview)

### Model Used : XGBRegressor

#### **My Contribution** :

Used ***Correlation*** for the reduction of Varibles.
```
columns = np.full((corr.shape[0]), True, dtype=bool)
for i in range(corr.shape[0]):
    for j in range(i+1, corr.shape[0]):
        if corr.iloc[i,j] >= 0.9: //If any two columns are coorelated by 90% we consider it redundant and remove it.
            if columns[j]:
                columns[j] = False
selected_columns = final_df.columns[columns]
final_df = final_df[selected_columns]
```
***My Public Score : 0.54854***
