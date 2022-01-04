# Job Comparison App User Manual

## 1 Overview of App

This Android app is a simple single-user App aimed to be used by graduates looking for a new job. The App gives the user the opportunity to compare the various job offers available to them and to choose the best job offer.
The Job comparison App also allow the user to easily add current job and job offers details, compare job offers with benefits in different location and compute job’s score as the weighted sum of some job details.

When the app is started, the main menu screen is displayed as shown in figure below:
![menu](images/manual/menu.png)

The following modules can be accessed from the main menu:

•	Manage Current Job: To enter or edit current job details.
•	Enter Job Offer:  To key-in the available job offers.
•	Compare jobs: To display ranked job offers and allow users to trigger comparison.
•	Comparison settings: To assign integer weight (equal weight if not customized).


## 2 Manage Current Job

If Manage Current Job Option is selected from the main menu, the user interface will be shown as figure below:
![current_job_blank](images/manual/current_job_blank.png)

All fields are left blank if no current job exists.

Enter current job information:

-	No field can be left blank.
-	Location should be expressed in the "City, State" format.
-	Cost of Living is expressed as an index between 0-999, refer to Expatistan's Cost of Living Map.
- Retirement benefit is expressed as percentage matched.
- Leave Time includes vacation days and holiday and/or sick leave, as a single overall number of days.

Save Button saves the information and returns to main menu.
Cancel Button returns to main menu without saving the information.

Current job can be edited as figure below if exists:
![current_job](images/manual/current_job.png)
   
 
## 3 Enter Job Offer

If the Enter Job Offer Option is selected from the main menu, a blank Job Offers page will be display as figure below:
![job_offer](images/manual/job_offer.png)

Enter job offer information:

-	No field can be left blank.
-	Location should be expressed in the "City, State" format.
-	Cost of Living is expressed as an index between 0-999, refer to Expatistan's Cost of Living Map.
- Retirement benefit is expressed as percentage matched.
- Leave Time includes vacation days and holiday and/or sick leave, as a single overall number of days.

Add New Button refreshes the page without saving the information.
Compare Button compares the job offer to current job. 
- Information needs to be saved before comparison.
- No comparison if no current job exists.
- Interface changes to Comparison Result if current job exists as figure below:
![compare_with_current](images/manual/compare_with_current.png)

Save Button saves the information and stays in current page.
Cancel Button returns to main menu without saving the information.


## 4 Compare Job Offers 

If Compare Job Offers Option is selected from the main menu, the user interface will be shown as figure below:
![compare_selection](images/manual/compare_selection.png)
   
- Jobs are ranked from highest score to lowest score.
- Current job is marked as current.
- Select only two jobs to compare.

Compare Button compares the selected jobs and displays result.
Cancel Button returns to main menu.

Comparison result will be displayed as figure below if triggered:
![compare_with_current](images/manual/compare_with_current.png)

- Salary and bonus are adjusted for cost of living.
- Job List Button returns to job list for another comparison.
- Main menu returns to main menu.


## 5 Comparison Settings 

If Comparison Settings Option is selected from the main menu, the user interface will be shown as figure below:
![setting](images/manual/setting.png)
   
- All weights are by default equal.
- Enter only numbers/integers.
- No field can left blank.

Save Button saves the information and returns to main menu.
Cancel Button returns to main menu without saving the information.
