This respository contains student and school data for an entire district, which are both found in the Resources folder. Using python and the Pandas Library, this data was analyzed in the PyCitySchools.ipynb jupter notebook found in the PyCitySchools folder. The Starter code was also included in this folder as it was a code reference, but none of the final coding is in this file. After the analysis was completed, a written report of the findings was laid out in the pandas_challenge_analysis.docx. 



Chat GPT was utiilized to help with certain errors that popped up and the specific code needed to fix it. The first being an error in the pd.cut function due to the formatting of a column as a string. This code was utilized to turn the column to a float for accurate results:

  school_spending_df["Per Student Budget"] = school_spending_df["Per Student Budget"].str.replace('[\$,]', '',  
  regex=True).astype(float)


Then Chat GPT Also gave the code for how to fix an unusual error in the groupby function by giving this suggestion.

  Silence warning By adding observed=False within the groupby() function call, you explicitly specify the behavior for the   
  observed parameter, thus silencing the FutureWarning


The Starter code was also utilized for merging the csv files, indexing the school name data, and overall structure of the analysis:

  merging: 
    school_data_complete = pd.merge(student_data, school_data, how="left", on=["school_name", "school_name"])
    school_data_complete.head()

  indexing:
    

  indexing :
