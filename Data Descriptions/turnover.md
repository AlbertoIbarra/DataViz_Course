## The Turnover Model

### Introduction

**Attrition** in business can mean the reduction in staff and employees in a company through normal means, such as retirement and resignation, the loss of customers or clients to old age or growing out of the company’s target demographic.The cause of attrition may be either voluntary or involuntary. Each industry has its own standards for acceptable attrition rates, and these rates can also differ between skilled and unskilled positions.

However, there is more to attrition than a shrinking workforce. As employees leave an organization, they take with them much-needed skills and qualifications that they developed during their tenure. On the other hand, junior professionals with promising qualifications can then succeed into higher level positions or business owners can introduce more diversity in experience or expertise. Due to the expenses associated with training new employees, any type of employee attrition is typically seen to have a monetary cost.

Although it is possible for a company to use employee attrition to its benefit in some circumstances, such as relying on it to control labor costs without issuing mass layoffs, in general, relatively high attrition is problematic for companies. HR professionals often assume a leadership role in designing company **compensation programs**, work culture and motivation systems that help the organization retain top employees.

There has been a great deal of talk for a couple decades now about the need for HR to be more strategic. Aside from any philosophical discussions of the true nature of 'strategy' and strategic thinking, what this normally means is that business leaders want HR to be more like their marketing departments - analytical, results-oriented, and able to directly tie their activities to the firm's desired outcomes (more money!). Marketing firms today rely quite heavily on predictive analytics and data mining/data science. The future of HR likely lies along this same road. 

In this project, we explore one potential problem such an analytical 'strategic' HR practicioner might reasonably expect to wrestle with, using data from a Health Care company. We try to analyse what factors lead to **employee retention** in companies, and what factors influence them the most. How and why are they quitting their jobs? Is it because of short monthly wages, or excess distance from home, or poor performance ratings? 

### The data set

The data set contains information about 1,470 employees. The variables are:

* `EmployeeNumber`, the employee's ID.

* `Turnover`, taking values 'No' and 'Yes'.

* `Age`, the employee's age, in years.

* `BusinessTravel`, with values "Non-Travel", "Travel_Frequently" and Travel_Rarely".

* `Department`, with values "Human Resources", "Research & Development" and "Sales".

* `DistanceFromHome`, the distance from home to the workplace, in miles.

* `Education` (ordinal), with values 1 (Below College), 2 (College), 3 (Bachelor) 4 (Master) and 5 (Doctor).

* `EducationField`, with values "Human Resources", "Life Sciences", "Marketing", "Medical" and "Other Technical Degree".

* `EnvironmentSatisfaction`, with values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `Gender`, with values "Female" and "Male".

* `JobInvolvement` (ordinal), with values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `JobRole`, the job role, which can take the following values: 'Healthcare Representative', 'Human Resources', 'Laboratory Technician', 'Manager', 'Manufacturing Director', 'Research Director', 'Research Scientist', 'Sales Executive' and 'Sales Representative'.

* `JobSatisfaction` (ordinal), with values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `MaritalStatus`, the marital status, either 'Divorced', 'Married' and 'Single'.

* `Wages`, the monthly gross wages in US dollars.

* `NumCompaniesWorked`, the number of companies for which the employee has previously worked .

* `OverTime`, whether the employee works overtime, with values 'No' and 'Yes'.

* `PercentSalaryHike`, the percentage change in salary from 2016 vs 2015.

* `PerformanceRating` (ordinal), taking values 1 (Low), 2 (Good), 3 (Excellent) and 4 (Outstanding).

* `RelationshipSatisfaction` (ordinal), taking values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `StockOptionLevel` (ordinal), how much company stocks you own, taking values 0, 1, 2 and 3.

* `TotalWorkingYears`.

* `TrainingTimesLastYear`.

* `WorkLifeBalance`, with values 1 (Bad), 2 (Good), 3 (Better) and 4 (Best).

* `YearsAtCompany`.

* `YearsInCurrentRole`.

* `YearsSinceLastPromotion`.

* `YearsWithCurrManager`.

### Source

Kaggle.
