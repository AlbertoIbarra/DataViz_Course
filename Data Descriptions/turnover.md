## Predicting Employee Turnover

### Introduction

**Employee turnover** in a company can come through normal means, such as retirement and resignation, the loss of customers to old age or growing out of the company’s target demographic. The cause can be either voluntary or involuntary. Each industry has its own standards for acceptable turnover rates, and these rates can also differ between skilled and unskilled positions.

However, there is more to employee turnover than a shrinking workforce. As employees leave an organization, they take with them skills which they developed during their tenure. Due to the expenses associated with training new employees, any type of employee attrition is typically seen to have a monetary cost.

Although it is possible for a company to use employee turnover to its benefit in some circumstances, such as relying on it to control labor costs without issuing mass layoffs, in general, relatively high attrition is problematic for companies. HR professionals often assume a leadership role in designing company **compensation programs**, work culture and motivation systems that help the organization retain top employees.

Human Resources (HR) managers are expected to take care of all this. There has been a great deal of talk for a couple decades now about the need for HR to be more strategic. Aside from any philosophical discussions of the true nature of 'strategy' and strategic thinking, what this normally means is that business leaders want HR to be more like their marketing departments - analytical, results-oriented, and able to directly tie their activities to the firm's desired outcomes. Nowadays, marketing firms today rely quite heavily on predictive analytics and data mining/data science. The future of HR likely lies along this same road. 

In this project, we explore one potential problem such an analytical 'strategic' HR practicioner might reasonably expect to wrestle with, using data from a Healthcare company. We wish to learn what factors lead to employee turnover. Is it because of short monthly wages, or excess distance from home, or poor performance ratings? 

### The data set

The data set contains information about 1,470 employees. The variables are:

* `EmployeeID`, the employee's ID.

* `Turnover`, taking values 'No' and 'Yes'.

* `Age`, the employee's age, in years.

* `BusinessTravel`, taking values 'Non-Trave, 'Travel_Frequently' and 'Travel_Rarely.

* `Department`, taking values 'Human Resources', 'Research & Development' and 'Sales'.

* `DistanceFromHome`, the distance from home to the workplace, in miles.

* `Education`, education level, taking values 1 (Below College), 2 (College), 3 (Bachelor), 4 (Master) and 5 (Doctor).

* `EducationField`, education field, taking values 'Human Resources', 'Life Sciences', 'Marketing', 'Medical' and 'Other Technical Degree'.

* `EnvironmentSatisfaction`, satisfaction with work environment, taking values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `Gender`, taking values 'Female' and 'Male'.

* `JobInvolvement`, the degree to which the employee is involved in his/her job, taking values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `JobRole`, the job role, taking values 'Healthcare Representative', 'Human Resources', 'Laboratory Technician', 'Manager', 'Manufacturing Director', 'Research Director', 'Research Scientist', 'Sales Executive' and 'Sales Representative'.

* `JobSatisfaction`, the employee's satisfaction with his/her job, taking values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `MaritalStatus`, the employee's marital status, either 'Divorced', 'Married' and 'Single'.

* `Wages`, the employee's monthly gross wages in US dollars.

* `CompaniesWorked`, the number of companies for which the employee has previously worked.

* `OverTime`, whether the employee works overtime, taking values 'No' and 'Yes'.

* `SalaryHike`, the percentage change in salary from 2016 vs 2015.

* `PerfoRating`, the employee's performance, taking values 1 (Low), 2 (Good), 3 (Excellent) and 4 (Outstanding). Reported by the employee's manager.

* `StockOption`, whether the employee owns company stock, taking values 'No' and 'Yes'.

* `TotalWorkingYears` the total number of years that the employee has worked, across companies.

* `TrainingLastYear`, the number of training activities in which the employee has participated during the last year.

* `WorkLifeBalance`, taking values 1 (Bad), 2 (Good), 3 (Better) and 4 (Best).

* `YearsAtCompany`, the number of years that the employee has been working for the company.

* `YearsInCurrentRole`, the number of years the employee has worked in his/her actual role.

* `YearsSinceLastPromotion`, the number of years since the employee's last promotion.

* `YearsWithCurrManager`, the number of years the employee has been working with his/her current manager.

### Source

Kaggle.
