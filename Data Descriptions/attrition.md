## Attrition and Performance Analysis

### Introduction

Attrition in business can mean the reduction in staff and employees in a company through normal means, such as retirement and resignation, the loss of customers or clients to old age or growing out of the company’s target demographic.The cause of attrition may be either voluntary or involuntary. Each industry has its own standards for acceptable attrition rates, and these rates can also differ between skilled and unskilled positions.

However, there is more to attrition than a shrinking workforce. As employees leave an organization, they take with them much-needed skills and qualifications that they developed during their tenure. On the other hand, junior professionals with promising qualifications can then succeed into higher level positions or business owners can introduce more diversity in experience or expertise.Due to the expenses associated with training new employees, any type of employee attrition is typically seen to have a monetary cost.

Although it is possible for a company to use employee attrition to its benefit in some circumstances, such as relying on it to control labor costs without issuing mass layoffs, in general, relatively high attrition is problematic for companies. HR professionals often assume a leadership role in designing company compensation programs, work culture and motivation systems that help the organization retain top employees.

In this project, we try to analyse what factors lead to employee retention in companies, and what factors influence them the most. We use a dataset that is published by the Human Resource department of IBM. here has been a great deal of talk for a couple decades now about the need for HR to be more strategic. Aside from any philosophical discussions of the true nature of 'strategy' and strategic thinking, what this normally means is that business leaders want HR to be more like their marketing departments - analytical, results-oriented, and able to directly tie their activities to the firm's desired outcomes (more money!!). Marketing firms today rely quite heavily on predictive analytics and data mining/data science. The future of HR likely lies along this same road. This kernel explores one potential problem such an analytical 'strategic' HR practicioner might reasonably expect to wrestle with.

### The data set

The data set contains information about 1,470 employees. The variables are:

* `EmployeeNumber`, the employee's ID.

* `Attrition`, with values "No" and "Yes".

* `Age`, the employee's age, in years.

* `BusinessTravel`, with values "Non-Travel", "Travel_Frequently" and Travel_Rarely".

* `DailyRate`.

* `Department`, with values "Human Resources", "Research & Development" and "Sales".

* `DistanceFromHome`.

* `Education`, with values 1 (Below College), 2 (College), 3 (Bachelor) 4 (Master) and 5 (Doctor).

* `EducationField`, with values "Human Resources", "Life Sciences", "Marketing", "Medical" and "Other Technical Degree".

* `EnvironmentSatisfaction`, with values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `Gender`, with values "Female" and "Male".

* `HourlyRate`.

* `JobInvolvement`, with values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `JobLevel` with values 1, 2, 3 and 4.

* `JobRole`, with "Healthcare Representative", "Human Resources", "Laboratory Technician", "Manager", "Manufacturing Director", "Research Director", "Research Scientist", "Sales Executive", "Sales Representative".

* `JobSatisfaction`, with values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `MaritalStatus`, with values "Divorced", "Married" and "Single".

* `MonthlyIncome`, monthly income in US dollars.

* `MonthlyRate`.

* `NumCompaniesWorked`, the number of companies for which the employees has previously worked .

* `OverTime`, whether the employee works overtime, with values "No" and "Yes".

* `PercentSalaryHike`.

* `PerformanceRating, with values 1 (Low), 2 (Good), 3 (Excellent) and 4 (Outstanding).

* `RelationshipSatisfaction`, with values 1 (Low), 2 (Medium), 3 (High) and 4 (Very High).

* `StockOptionLevel`.

* `TotalWorkingYears`.

* `TrainingTimesLastYear`.

* `WorkLifeBalance`, with values 1 (Bad), 2 (Good), 3 (Better) and 4 (Best).

* `YearsAtCompany`.

* `YearsInCurrentRole`.

* `YearsSinceLastPromotion`.

* `YearsWithCurrManager`.

### Source

Kaggle and Krushna Metha.
