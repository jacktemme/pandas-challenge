# pandas-challenge


school_spending_df["Per Student Budget"] = school_spending_df["Per Student Budget"].str.replace('[\$,]', '', regex=True).astype(float)
