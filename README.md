# Pewlett-Hackard-Analysis

## Overview of the Analysis: 

A very large company, Pewlett-Hackard, is reviewing their workforce data in order to determine two major things: 1) The number of retiring employees per job title and 2) The employees that meet the eligibility criteria to participate in a mentorship program. 

## Resources

- Six csv files of Pewlett-Hackard employment data
- PostgreSQL 11 within pgAdmin 4 software.

# Results: 

Structured Query Language (SQL) was used to generate queries to answer P-H's questions. for preliminary conclusions, see the five bullet points below divided between the particular analysis that they apply to.

## Retiring Employees

Two csv files were merged together with inner join (employees and titles). The results were filtered by birth date to create a preliminary results table. Then, redundant employee records as well as employees that have since left the company were removed from the data set via SELECT DISTINCT ON. Finally, the employees were aggregated by job title. From the resulting table, we learn that:

- The table includes employees’ titles and their sum.
- The job title with the most retiring employees is Senior Engineer (25916).
- The job title with the fewest retiring employees is Manager (2).

## Mentorship Program

Three csv files (employees, titles, and dept_emp) were merged together with inner join. The results were filtered by birthdate and current employment status. The resulting table tells us that: 

- The table contains employee number, first name, last name, birth date, from date, to date and title.
- 1549 employeees are eligible for the mentorship program.

# Summary: 

Our analyses have answered Pewlett-Hackard's questions.

## How many roles will need to be filled as the "silver tsunami" begins to make an impact?

According to our table, 72,458 employees are meeting the retirement criteria and thus will need their roles filled in the upcoming years across the various job titles. This is quite a sum! A table showing job applicant data would be helpful to see if the incoming workforce can match the outgoing one.

## Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

Considering the retirement eligibility age range was three years while the mentorship eligibility age range was just one year, it makes sense that there are more than enough mentors for the program. What would be helpful is a table of current employees for multiple cohorts (other years or combination of years) to see if the mentorship program can be expanded further.

## Limitations

Overall the analyses were a success. There was no missing data to complicate table generation. In addition, we were able to deal with redundancies in the data with the right query commands.