In this exercise we are providing you an example of financial data (all numbers are fictional).
**Deadline** is 10 days after you received this test.

## Task 1

* You need to create an algorithm that can find outliers in this data by one column / several columns. E.g. some members have extremely high costs in the current month and your solution should be able to detect such records
* Think about features and how you would explain it to business people
* All financial columns contain $ sign

Please provide a Jupyter notebook describing your approach as a result of this task.

## Task 2

* Create a web dashboard prototype in Python that allows users to:
	* Create slicers and dicers
	* Filters by date range / ...
	* Show data both in table and plotted formats
Use paid_amount column for analysis and other columns for filters
Don’t worry about UI and design, just provide very simple functionality
You are free to use Flask / FastAPI / plotly / bokeh / etc.
Normalize text values in columns. Please, provide your approach to do it in the automatic way as Jupyter notebook. Think about it as you need to update this dashboard monthly and do not have time to normalize values manually
Columns:
member_unique_id - member's ID	
gender - member's gender
dob - member's date of birth
eligible_year - year
eligible_month - month
affiliation_type - doctor's type
pbp_group - health plan group
plan_name - health plan name
npi - doctor's ID
line_of_business - health plan type
esrd - True if patient is on dialysis
hospice - True if patient is in hospice
Please provide this task as a python project. You can send it as a zip archive / Git repository / Docker



<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIxMDE2MzkzODFdfQ==
-->