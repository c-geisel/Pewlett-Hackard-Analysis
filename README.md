# Pewlett Hackard Analysis
[Link to Pewlett Hackard Queries](https://github.com/c-geisel/Pewlett-Hackard-Analysis/blob/main/Queries/Employee_Database_challenge.sql)

## Overview of the analysis
Pewlett Hackard is an old company that is having a wave of employees who will reach their retirement qualifications in the near future. The company is beginning to consider how man and which positions need to be filled. There are two desired outcomes in this analysis, the first deliverable is to determine the number of employees that will be retiring based on their most recent job title. The second deliverable is to create a table that will include the employees who are eligible to participate in a mentorship program if in a position for a certain period of time. 

## Results 
Four tables were created in order to find the desired outcomes. Three tables were made to find the answer to the first outcome and one was created for the second outcome. The first deliverable is to find the number of employees retiring grouped by job title.
1.  To begin deliverable one, a table is created with general employee information as well as job titles. This is done by joining columns from the employees and titles table. This data is filtered so that only employees born within a certain range (those eligible to retire) can be seen. 
![retirement_titles.png](Images/retirement_titles.png)

2. After creating the retirement_titles table it can be seen that employees appear in multiple rows with different job titles at different dates. This occurs because employess may have changed jobs within the company throughout their career. To resolve this issue, a DISTINCT ON statement is use to retrieve the first occurence of each persons name. Each employees name and title is then pulled from the retirement table creates and put into a unique_titles table that lists each employees first title. 
![unique_titles.png](Images/unique_titles.png)

3. The final task needed to complete deliverable one is to retrived the number of employees by most recent title that are about to retire. This is done by counting the number of titles in the unique_titles table created above and placing the information into a new table called retiring_titles.
![retiring_titles.png](Images/retiring_titles.png)

4. The outcome of deliverable two is to create a table of employees who would be eligibile to mentor new employees for the company. To begin, employee information is retrieved from the employees, titles, and dept. employees tables. The data was then filtered to ensure all the employees listed were born within a certain year to ensure retirement eligibility and also filtered to ensure they still were working with the company. 
![mentorship_eligibility.png](Images/mentorship_eligibility.png)


## Summary 
Provide high-level responses to the following questions, then provide two additional queries or tables that may provide more insight into the upcoming "silver tsunami."

How many roles will need to be filled as the "silver tsunami" begins to make an impact?

Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
