#BigData Group4 Colleges
Comparing the US Dept. of Education: College Scorecard dataset against the World University Rankings dataset.
College Scorecard: https://www.kaggle.com/kaggle/college-scorecard
World University Rankings: https://www.kaggle.com/mylesoneill/world-university-rankings

1. How does the ranking of the university correspond with admission rate?
2. Is there a correlation between cost of tuition and university ranking?
3. What is the correlation between average SAT score and admission rate?

##Script Instructions
###Pubic Universities Only Analysis
1. Open the `public_universities_only_analysis.ipynb` notebook in a **jupyter** shell. This an R notebook that is just a modified script of the `collegeRankingScript.r` script, which only executes the code on public universities. 

###Original Analysis
1. Open the **collegeRankingScript.r** file in Rstudio and execute. 

###Side Note
**Untitled.ipynb** has the work of combining the datasets and creating the condensed datasets used in the **collegeRankingScript.r** file.


##What was Changed?
The original `collegeRankingScript.r` was an analysis answering the three above question on both private and public universities.  The modified script tightened the analysis down to only investigate these questions on public universities only. The following code was used in order to subset on public universities. 

```original_TIMES_SCORE = read.csv("TIMES_SCORE.csv", encoding="UTF-8")```

```original_CWUR_SCORE = read.csv("CWUR_SCORE.csv", encoding="UTF-8")```

```TIMES_SCORE = subset(original_TIMES_SCORE, NPT4_PUB >0 )```

```CWUR_SCORE = subset(original_CWUR_SCORE, NPT4_PUB >0)```