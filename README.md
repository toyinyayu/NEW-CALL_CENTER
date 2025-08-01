# Call Center Analysis

## Description
This is a call center analysis

### Project Overview
- Clean Data
- Tranform it
- Analyse
- Recommendation

### Total Calls

``` SQL
SELECT COUNT(id) AS Total_Calls
  FROM [call_center].[dbo].[call_center]
```

### Average Satisfactory Score

```   SQL
SELECT 
    ROUND(AVG(NULLIF(csat_score, 0) * 1.0), 2) AS Avg_Satisfactory_Call
FROM call_center.dbo.call_center
WHERE csat_score IS NOT NULL;

```

### Average Call Duration in Mins

``` SQL
SELECT 
    ROUND(AVG(call_duration * 1.0), 2 )
	AS Call_Duration_In_Min
FROM call_center.dbo.call_center
WHERE call_duration IS NOT NULL;

```
