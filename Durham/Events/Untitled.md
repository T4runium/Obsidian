```dataview
TABLE WITHOUT ID
  dateformat(date, "d/M/yy") AS Date,
  startTime + " - " + endTime AS Time,
  title AS Event,
  location AS Location
FROM "Timetable"
SORT date ASC, startTime ASC
```