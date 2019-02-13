# Data Science Immersive (DSI6) Project 1
## Katy Chow

### Problem Statement
We are trying to provide College Board with additional insights to increase participation rates in SAT testing. 


### Executive Summary
Given **2017 ACT and SAT** results by states in the US, we are trying to infer information about participation rates and different scores by exploring the 2017 ACT and SAT scores and 2018 ACT and SAT scores.

### Data Sources
- 2 Datasets Provided
    - [SAT 2017](https://reports.collegeboard.org/archive/sat-suite-program-results/2017/detailed-2017-reports)
        - 52 Observations (50 States, DC area, and National results)
        - Math, Verbal, Overall Scores
    - [ACT 2017](https://blog.prepscholar.com/act-scores-by-state-averages-highs-and-lows)
        - 51 Observations (50 States and the DC area)
        - Math, Reading, English, Science, Composite Scores
- 2 Datasets Scraped from Web/ Manually pulled into csv
    - [SAT 2018](https://reports.collegeboard.org/sat-suite-program-results/state-results)
        - 51 Observations (50 States and National results)
        - Math, Verbal, Overall Scores
    - [ACT 2018](http://www.act.org/content/dam/act/unsecured/documents/cccr2018/Average-Scores-by-State.pdf)
        - 51 Observations (50 States and National Results)
        - Composite Scores Only
        
### Data Dictionary

** Data within the jupyter notebook have prefixes of either 2017_SAT, 2017_ACT, 2018_SAT, or 2018_ACT to represent the year and standardize test the feature is referring to. **

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**sat_state**|*str*|SAT|Regional Marker| 
|**sat_participation**|*float*|SAT|Percentage of graduating class that participated in ACT/SAT Testing|
|**sat_evidence_based_reading_and_writing**|*int*|SAT|SAT reading and writing section score|
|**sat_math**|*int*|SAT|SAT math section score|
|**sat_total**|*int*|SAT|SAT total score - Summation of Math and Reading Scores| 
|**act_state**|*str*|ACT|Regional Marker| 
|**act_participation**|*float*|ACT|Percentage of graduating class that participated in ACT/SAT Testing|
|**act_english**|*float*|ACT|ACT English Score| 
|**act_math**|*float*|ACT|ACT Math Score| 
|**act_reading**|*float*|ACT|ACT Reading Score| 
|**act_science**|*float*|ACT|ACT Science Score| 
|**act_composite**|*float*|ACT|ACT Total (Composite) Score - Average of individual Scores|

### Conclusions & Next Steps

For myself, the key take aways are that you cannot always just rely on data to give you insights, but instead look at other factors that can drive the data to look a certain way.  Lots of low participation rates for exams are correlated with higher exam scores.  This is driven by two major factors.  The first being a self selection bias of students that are motivated to go to college.  The second is the state will also provide for the brightest students to take the exams.  Evidence can be found [here](https://blog.prepscholar.com/average-sat-and-act-scores-by-stated-adjusted-for-participation-rate).

For any of the states that have lower participation rates, College Board can work with the particular state to provide free exams once a year or free test preparations.  The [ACT](https://www.act.org/content/dam/act/unsecured/documents/cccr2017/CCCR_National_2017.pdf) seems to have working relationships with most states with the exception of Texas, the West coast, and the Northeastern region.  

Additional data that I would like to have would be demographic data along with county results for SAT and ACT testing.  I believe high test scores are more likely to be correlated with wealth due to the resource availability to study for exams and additionally pay for multiple exams.  

It would also be nice to normalize the data by grouping different participation rates together and comparing state results across similar participation groups.  A good example of why normalization is important is that [North Dakota](https://reports.collegeboard.org/pdf/2018-north-dakota-sat-suite-assessments-annual-report.pdf) has one of the highest average scores, but there are only 7800 students graduating and 148 students took the SATs in 2017.  If you compared those values to a state like [Florida](https://reports.collegeboard.org/pdf/2018-florida-sat-suite-assessments-annual-report.pdf), perhaps within one county that many students took the SATs.  