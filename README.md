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
