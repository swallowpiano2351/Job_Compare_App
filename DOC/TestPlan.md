# Test Plan

**Author**: \<Team 60\>

## 1 Testing Strategy

### 1.1 Overall strategy

Our testing strategy includes integration testing and system testing. The project will be completed as a joint effort of different programmers. Therefore, manual testing will be employed by each programmer to ensure the functionality of each part (e.g. interface, database, main codes and etc.) while integration testing will be performed by all programmers when each single part are put together to check the interaction among each component. Finally, system testing will be included to test the application as a whole from a user's perspective. In addition, as the project grows, we might also include regression testing to make sure any newly added functions are compatible with the existing ones.

### 1.2 Test Selection

For integration testing and system testing, we will use black-box/functional testing techniques to test each functionality of the system including User Interface, Database and functionality of the Application Under Test. This will mainly be done by the category-partition method that use different test cases to test for desired outputs. All testing will be performed manually via the user interface. All test will be performed in various Pixel devices.

### 1.3 Adequacy Criterion

For integration testing and system testing, the functional coverage or statement coverage will be employed to ensure each specification of the requirement statement is satisfied.

### 1.4 Bug Tracking

Bugs and enhancement requests will be tracked using documents within the repository in github.

### 1.5 Technology

Sqlite will be used to query the database.

## 2 Test Cases

| TC ID | Purpose | step | expected result | actual result | pass/fail | note |
|:-----:|:--------|:-----|:----------------|:--------------|:---------:|:-----|
|#1|Verify CurrentJob page can be accessed| Invoke Manage Current Job button in Main Menu | Successful access|Successful access|Pass||
|#2|Verify JobOffer page can be accessed| Invoke Enter Job Offer button in Main Menu | Successful access|Successful access|Pass||
|#3|Verify Comparison page can be accessed| Invoke Compare Job Offers button in Main Menu | Successful access to Job List page|Worked|Pass||
|#4|Verify Comparison Setting page can be accessed| Invoke Comparison Settings button in Main Menu | Successful access|Successful|Pass||
|#5|Verify CurrentJob page is blank if no current job information exists| Invoke Manage Current Job button in Main Menu | Blank table displayed |As expected - Blank table|Pass||
|#6|Verify CurrentJob page is filled with corresponding information if current job information exists| Invoke Manage Current Job button in Main Menu | Current Job Information retrieved and filled table displayed |Worked as expected|Pass||
|#7|Verify current job information can be saved| Enter current job information and invoke Save button in Manage Current Job page | Information written to database |Worked as expected|Pass||
|#8|Verify return from Manage Current Job page to Main Menu| Enter information and invoke Exit button in Manage Current Job page | Information not written to database and application page return to Main Menu|Worked as expected|Pass||
|#9|Verify job offer information can be saved| Enter job offer information and invoke Save button in Enter Job Offer page | Information written to database |Database updated successfully|Pass||
|#10|Verify return from Enter Job Offer page to Main Menu| Enter information and invoke Exit button in Enter Job Offer page | Information not written to database and application page return to Main Menu| Per expected | Pass ||
|#11|Verify new job offer can be added| Invoke Add New button in Enter Job Offer page | New blank page to enter job information displayed |Yes|Pass||
|#12|Verify comparison between newly added job offer and current job can be compared| Invoke Compare button in Enter Job Offer page | Comparison result between newly added job offer and current job displayed |Worked as expected|Pass||
|#13|Verify comparison performed for selected job offers| Select two jobs and invoke Compare button in Job List page | Comparison Result page accessed and table displayed |Worked as expected|Pass||
|#14|Verify return from Job List page to Main Menu| Invoke Main Menu button in Job List page | Return to Main Menu|Yes|Pass||
|#15|Verify return from Comparison Result page to Job List for new comparison| Invoke Job List button in Comparison Result page | Return to Job List|Yes|Pass||
|#16|Verify return from Comparison Result page to Main Menu| Invoke Main Menu button in Comparison Result page | Return to Main Menu|worked as expected|Pass||
|#17|Verify comparison setting can be saved| Enter comparison weights and invoke Save button in Comparison Settings page | Weights information saved to database. |per expected|pass||
|#18|Verify return from Comparison Setting page to Main Menu| Enter comparison weights and invoke Exit button in Comparison Settings page | Weights information not saved to database and return to Main Menu |Per Expected|Pass||
|#19|Verify correct calcuation for job score without customized comparison setting| Enter job information and execute getScore() method | Score calculation by hand (equal weight) |Score gotten from UI comparison result match score calculated manually|Pass||
|#20|Verify correct calcuation for job score with customized comparison setting| Enter job information, comparison settings and execute getScore() method | Score calculation by hand (customized weight) |Score gotten from UI comparison result match score calculated manually|Pass||
|#21|Check for invalid (non-numerical) input in current job| Enter job information with alphabetical input in cost of living in Manage Current Job page | Invalid input mark displayed |Error displayed as expected|Pass||
|#22|Check for invalid (non-numerical) input in current job| Enter job information with alphabetical input in Yearly Salary in Manage Current Job page | Invalid input mark displayed |Error displayed as expected|Pass||
|#23|Check for invalid (non-numerical) input in current job| Enter job information with alphabetical input in Yearly Bonus in Manage Current Job page | Invalid input mark displayed |Error displayed as expected|Pass||
|#24|Check for invalid (non-numerical) input in current job| Enter job information with alphabetical input in Telework Days in Manage Current Job page | Invalid input mark displayed |Worked as expected|Pass||
|#25|Check for invalid (non-numerical) input in current job| Enter job information with alphabetical input in Retirement Benefits in Manage Current Job page | Invalid input mark displayed |Error displayed as expected|Pass||
|#26|Check for invalid (non-numerical) input in current job| Enter job information with alphabetical input in Leave Time in Manage Current Job page | Invalid input mark displayed |Error displayed as expected|Pass||
|#27|Check for invalid (out-of-bound) input in current job| Enter 8 in Telework Days in Manage Current Job page | Invalid input mark displayed |Error displayed as expected|Pass||
|#28|Check for invalid (out-of-bound) input in current job| Enter 101 in Retirement Benefits in Manage Current Job page | Invalid input mark displayed |Yes|Pass||
|#29|Check for invalid (out-of-bound) input in current job| Enter 367 in Leave Time in Manage Current Job page | Invalid input mark displayed |Yes|Pass||
|#30|Check for empty input in current job| Leave Company blank in Manage Current Job page and click Save | Invalid input mark displayed |Yes|Pass||
|#31|Check for invalid (non-numerical) input in job offer| Enter job information with alphabetical input in cost of living in Manage Job Offer page | Invalid input mark displayed |Error displayed as expected|Pass||
|#32|Check for invalid (non-numerical) input in job offer| Enter job information with alphabetical input in Yearly Salary in Job Offer page | Invalid input mark displayed |Error displayed as expected|Pass||
|#33|Check for invalid (non-numerical) input in job offer| Enter job information with alphabetical input in Yearly Bonus in Job Offer page | Invalid input mark displayed |Yes|Pass||
|#34|Check for invalid (non-numerical) input in job offer| Enter job information with alphabetical input in Telework Days in Job Offer page | Invalid input mark displayed |Yes|Pass||
|#35|Check for invalid (non-numerical) input in job offer| Enter job information with alphabetical input in Retirement Benefits in Job Offer page | Invalid input mark displayed |Error displayed as expected|Pass||
|#36|Check for invalid (non-numerical) input in job offer| Enter job information with alphabetical input in Leave Time in Job Offer page | Invalid input mark displayed |Successfully display|Pass||
|#37|Check for invalid (out-of-bound) input in job offer| Enter 8 in Telework Days in Manage Job Offer page | Invalid input mark displayed |Yes|Pass||
|#38|Check for invalid (out-of-bound) input in job offer| Enter 101 in Retirement Benefits in Job Offer page | Invalid input mark displayed |Yes|Pass||
|#39|Check for invalid (out-of-bound) input in job offer| Enter 367 in Leave Time in Job Offer page | Invalid input mark displayed |Yes|Pass||
|#40|Check for empty input in job offer| Leave Company blank in Job Offer page and click Save | Invalid input mark displayed |Per Expected|Yes||
|#41|Check for invalid selection in Job List| Select 3 jobs in Job List page | Invalid mark displayed |No Erro display, but not able to compare|Pass||
|#42|Check for invalid selection in Job List| Select 1 job in Job List page | Invalid mark displayed |No Erro display, but not able to compare|Pass||
|#43|Check for invalid comparison if no current job exist| Select current job in database and click Compare button in Job Offer page | No reaction and "no comparison" message shown |Error displayed as expected|Pass||
|#44|Check for invalid (non-numerical) input in comparison setting| Enter a in Yearly Salary in Comparison Settings page | Invalid input mark displayed |Not able to enter|Pass||
|#45|Check for invalid (non-numerical) input in comparison setting| Enter + in Yearly Bonus in Comparison Settings page | Invalid input mark displayed |Not able to enter|Pass||
|#46|Check for invalid (non-numerical) input in comparison setting| Enter # in Telework Days/Week in Comparison Settings page | Invalid input mark displayed |Not able to enter|Pass||
|#47|Check for invalid (non-numerical) input in comparison setting| Enter * in Retirement Benefits in Comparison Settings page | Invalid input mark displayed |Not able to enter|Pass||
|#48|Check for invalid (non-numerical) input in comparison setting| Enter - in Leave Time in Comparison Settings page | Invalid input mark displayed |Not able to enter|Pass||
