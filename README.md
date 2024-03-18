This respository contains student and school data for an entire district, which are both found in the Resources folder. A Jupyter Notebook file was coded with Python and the Pandas Library to analyze this data in the PyCitySchools.ipynb file found in the PyCitySchools folder. The Starter code was also included in this folder as it was a code reference, but none of the final coding is in this file. After the analysis was completed, a written report of the findings was laid out in the Pandas_Challenge_Analysis.docx. 


Chat GPT was utiilized to help with certain errors that popped up and the specific code needed to fix it. The first being an error in the pd.cut function due to the formatting of a column as a string. This code was utilized to turn the column to a float for accurate results:

    school_spending_df["Per Student Budget"] = school_spending_df["Per Student Budget"].str.replace('[\$,]', '',  
    regex=True).astype(float)


Then Chat GPT Also gave the code for how to fix a warning error in the groupby function of a binned column by giving this suggestion.

  Silence warning By adding observed=False within the groupby() function call, you explicitly specify the behavior for the   
  observed parameter, thus silencing the FutureWarning


The Starter code was also utilized for merging the csv files, formating columns, indexing the school name data, and overall structure of the analysis:

  Merging: 
    school_data_complete = pd.merge(student_data, school_data, how="left", on=["school_name", "school_name"])
    school_data_complete.head()

  Column Formating: 
    per_school_summary["Total School Budget"] = per_school_summary["Total School   Budget"].map("${:,.2f}".format)
    per_school_summary["Per Student Budget"] = per_school_summary["Per Student Budget"].map("${:,.2f}".format)

  Indexing :
      school_types = school_data.set_index(["school_name"])["type"]

