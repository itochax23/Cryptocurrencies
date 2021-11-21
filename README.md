# Cryptocurrencies

## Heading

## Heading
1. thing
```
# Use get_dummies() to create variables for text features.
crypto = pd.get_dummies(df_crypto['Algorithm'])
dummy = pd.get_dummies(df_crypto['ProofType'])
combined = pd.concat([crypto,dummy],axis =1)
X_df = df_crypto.merge(combined,left_index = True,right_index = True)
X_df = X_df.drop(['Algorithm','ProofType'],axis = 1)
X_df.head()
```

3. thing
4. thing
5. thing

## Heading
