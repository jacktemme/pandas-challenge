# pandas-challenge


school_spending_df["Per Student Budget"] = school_spending_df["Per Student Budget"].str.replace('[\$,]', '', regex=True).astype(float)

silence warning By adding observed=False within the groupby() function call, you explicitly specify the behavior for the observed parameter, thus silencing the FutureWarning
