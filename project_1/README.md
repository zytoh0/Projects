# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Standardized Test Analysis

### Overview

Our first module in DSI covers:
- Basic statistics and probability
- Many Python programming concepts
- Programmatically interacting with files and directories
- Visualizations
- EDA
- Working with Jupyter notebooks for development and reporting

You might wonder if you're ready to start doing data science. While you still have **tons** to learn, there are many aspects of the data science process that you're ready to tackle. Project 1 aims to allow you to practice and demonstrate these skills.

For our first project, we're going to take a look at aggregate SAT and ACT scores and participation rates in the United States. We'll seek to identify trends in the data and combine our data analysis with outside research to address our problem statement.

The SAT and ACT are standardized tests that many colleges and universities in the United States require for their admissions process. This score is used along with other materials such as grade point average (GPA) and essay responses to determine whether or not a potential student will be accepted to the university.

The SAT has two sections of the test: Evidence-Based Reading and Writing and Math ([*source*](https://www.princetonreview.com/college/sat-sections)). The ACT has 4 sections: English, Mathematics, Reading, and Science, with an additional optional writing section ([*source*](https://www.act.org/content/act/en/products-and-services/the-act/scores/understanding-your-scores.html)). They have different score ranges, which you can read more about on their websites or additional outside sources (a quick Google search will help you understand the scores for each test):
* [SAT](https://collegereadiness.collegeboard.org/sat)
* [ACT](https://www.act.org/content/act/en.html)

Standardized tests have long been a controversial topic for students, administrators, and legislators. Since the 1940's, an increasing number of colleges have been using scores from sudents' performances on tests like the SAT and the ACT as a measure for college readiness and aptitude ([*source*](https://www.minotdailynews.com/news/local-news/2017/04/a-brief-history-of-the-sat-and-act/)). Supporters of these tests argue that these scores can be used as an objective measure to determine college admittance. Opponents of these tests claim that these tests are not accurate measures of students potential or ability and serve as an inequitable barrier to entry.

### Problem Statement

The state of California has many school counties. This project aims to identify the counties that have the worst overall student performance on the SAT tests so the state can recommend programs and allocate resources to these counties in need.
---

### Datasets

* [`act_2017.csv`](./data/act_2017.csv): 2017 ACT Scores by State
* [`act_2018.csv`](./data/act_2018.csv): 2018 ACT Scores by State
* [`act_2019.csv`](./data/act_2019.csv): 2019 ACT Scores by State
* [`act_2019_ca.csv`](./data/act_2019_ca.csv): 2019 ACT Scores in California by School
* [`sat_2017.csv`](./data/sat_2017.csv): 2017 SAT Scores by State
* [`sat_2018.csv`](./data/sat_2018.csv): 2018 SAT Scores by State
* [`sat_2019.csv`](./data/sat_2019.csv): 2019 SAT Scores by State
* [`sat_2019_by_intended_college_major.csv`](./data/sat_2019_by_intended_college_major.csv): 2019 SAT Scores by Intended College Major
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California by School
* [`sat_act_by_college.csv`](./data/sat_act_by_college.csv): Ranges of Accepted ACT & SAT Student Scores by Colleges
---

#### Additional Data

* [`sat_2017_ca.csv`](./data/sat_2017_ca.csv): 2017 SAT Scores in California
* [`sat_2018_ca.csv`](./data/sat_2018_ca.csv): 2018 SAT Scores in California
* [`sat_2019_ca.csv`](./data/sat_2019_ca.csv): 2019 SAT Scores in California
---

### Data Import and Cleaning

1. Import, drop rows with na and remove %
2. Lowercase all columns
3. Drop additional columns in preparation for merging
4. Merge dataframes
5. Export merged dataframes to csv

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|column name|int/float/object|ACT/SAT|This is an example| 
|CDS|float|SAT|County/District/School Code|
|CCode|float|SAT|County Code|
|CDCode|float|SAT|District Code|
|SCode|float|SAT|School Code|
|RType|str|SAT|Record Type: C=County, D=District, S=School, X=State|
|SName|str|SAT|School Name|
|DName|str|SAT|District/LEA Name|
|CName|str|SAT|County Name|
|Enroll12|float|SAT|Enrollment of Grade 12|
|NumTSTTakr12|float|SAT|Number of Test Takers Grade 12|
|NumERWBenchmark12|str|SAT|The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 12|
|PctERWBenchmark12|str|SAT|The percent of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 12|
|NumMathBenchmark12|str|SAT|The number of students who met or exceeded the benchmark for the New SAT math test format as of March 2016 for Grade 12|
|PctMathBenchmark12|str|SAT|The percent of students who met or exceeded the benchmark for SAT Math test for Grade 12.|
|Enroll11|float|SAT|Enrollment of Grade 11|
|NumTSTTakr11|float|SAT|Number of Test Takers Grade 11|
|NumERWBenchmark11|str|SAT|The number meeting the Evidence-Based Reading & Writing (ERW) benchmark established by the College Board based on the New 2016 SAT test format as of March 2016 for Grade 11|
|PctERWBenchmark11|str|SAT|The percent of students who met or exceeded the benchmark for Evidence-Based Reading & Writing (ERW) test for Grade 11|
|NumMathBenchmark11|str|SAT|The number of students who met or exceeded the benchmark for the New SAT math test format as of March 2016 for Grade 11|
|PctMathBenchmark11|str|SAT|The percent of students who met or exceeded the benchmark for SAT Math test for Grade 11.|
|TotNumBothBenchmark12|str|SAT|The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.|
|PctBothBenchmark12|str|SAT|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 12.|
|TotNumBothBenchmark11|str|SAT|The total number of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.|
|PctBothBenchmark11|str|SAT|The percent of students who met the benchmark of both Evidence-Based Reading & Writing (ERW) and Math Grade 11.|
|Year|str|SAT|The SAT test administraion year.|
---

### Exploratory Data Analysis
![GitHub Logo](/images/SAT vs ACT Participation.png)
Format: ![Alt Text](url)