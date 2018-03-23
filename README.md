# ICA-4
Work done at USF with SQL codes and corresponding graphs. 

## Description of datasets.sat_scores
Table contains SAT scores and hours studied for different schools, teachers, and students.

## Question #1
How does studying affect the Math SAT score?

```sql
Select sat_math, hrs_studied
From datasets.sat_scores
Where hrs_studied notnull
order by hrs_studied ASC
```

![ICA-4](Visualizations/Q1graph.png)

## Question #2
What are the average scores for all of the three scores? Average math, average writing, average verbal? Order by school.

```sql
Select school, Avg (sat_writing) as Avg_Writing, Avg (sat_math) as Avg_Math, Avg(sat_verbal) as Avg_Verbal
from datasets.sat_scores
group by school
```

![ICA-4] (Vizualizations/Q2graph.png)

## Question #3
What were each teachers average total score?

```sql
Select teacher, Avg (sat_writing) as Avg_Writing, Avg (sat_math) as Avg_Math, Avg(sat_verbal) as Avg_Verbal
from datasets.sat_scores
group by teacher
```

![ICA-4] (Vizualizations/Q3graph.png)
