#inProgress 


## If-else Statement
```SQL
SELECT *, if(CourseCode="BSIT", "BS Information Technology", "BS Computer Science") as "Course Description" FROM student_record;
```

## Nested If-else Statement
```SQL
SELECT *, if(YearCode=1, "Freshmen", if(YearCode=2, "Sophomore", if(YearCode=3, "Junior", "Senior"))) as "Year Description" FROM student_record;
```

In a more easily readable manner
```SQL
SELECT *, 
	if(YearCode=1, "Freshmen", 
		if(YearCode=2, "Sophomore", 
			if(YearCode=3, "Junior", "Senior")
		)
	) as "Year Description" 
FROM student_record;
```


## Case Statement
See [freecodecamp's](https://www.freecodecamp.org/news/case-statement-in-sql-example-query/) sample and [this](https://www.sqlshack.com/case-statement-in-sql/)
```sql
SELECT *,
  CASE
    WHEN score >= 94 THEN "A"
    WHEN score >= 90 THEN "A-"
    WHEN score >= 87 THEN "B+"
    WHEN score >= 83 THEN "B"
    WHEN score >= 80 THEN "B-"
    WHEN score >= 77 THEN "C+"
    WHEN score >= 73 THEN "C"
    WHEN score >= 70 THEN "C-"
    WHEN score >= 67 THEN "D+"
    WHEN score >= 60 THEN "D"
    ELSE "F"
  END AS grade
FROM students_grades;
```