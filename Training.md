# TIME AND ATTENDANCE TRAINING
At the start of the meeting **share the link to the server** with the trainees. The link should have ip address and not local host if the server and client are on the same network.

## DASHBOARD

overview of what you are going to expect in the system

__Total Head Count__ -active number of employees in the organization
Present- total number of employees present as of today
__Absent__ -total number of employees absent as of today, reason may be failure to clock in, or those on leave and information has not been updated in the system, those who are on their weekly off but their info is not updated in the system
__Late in__ - indidcates the number of employees who have clocked in late as of the start time of their shift.
__Early Out__- employees have clocked out earlier than the end of the shift as of today
__On Leave__- Indicates the number of employees on leave as of today. if the leave is captured corerectly it will show on leave card. if not it will appear on the absent card.
__Weely Off__ - is when employees are on their resting day. indicates the number the number of employees whose weekly off is the present day. if the weekly off is captured corerectly it will show on weekly off card. if not it will appear on the absent card.
__Holiday__ - the system allows the user to add and customize holidays. the holiday in the dashboard therefore indicates the number of employees who have clocked in during the holiday. The system will indicate the hours that the employees are entitled to be paid for working during holidays. if there are employees whose shift is schedule to include the holidays will be marked as present if the clock in and absent is if they fail to clock in.
__Compensatory Off/ C-Off__ -This captures the information for employees who have been assigned compensatory off. that is, if they have worked on their weekly off or during the holidays if asked by management.
__Contract expired__ -if employees are under contract. those whose contract has expired as of the present day are displayed on the dashboard.

## MASTERS

similar to the old TA, Used to adding new or edit existing entries.

### Placement Masters-

__To add a department__- when you click on department it shows the existing departments. The systems has an ADD BUTTON that is BLUE in color.
The fields with a red asteric are mandatory fields.
__To edit the department__ that has been created you click on the department edit to your liking and select the UPDATE BUTTON that is GREEN in color.
__To delete a department__- click on the department and select the DELETE BUTTON that is RED in color.

**same logic goes to the other fileds(Sub department, designation, category, class, position, master one, master two, location)**

### Shift

Used to define the shifts that the employess are assigned.
__To define a shift__ in the new system, you need to select shift type- normal
shift code can be same as shift name so that once the shift has been allocated to an employee you can be able to understand the shift better and different the different shift allocated to that particular employee.
The best practice is to use the shift name and in brackets the start and end time of the shift. e.g NORMAL SHIFT(07:30 to 16:45)

__To define the break__
click on Add a new record
e.g Lunch break Start time 13:00 End Time 14:00
Applicable on - set the days which the shift will be applicable
__Time Range__- depending on how the employees clock, any employees who clock between the time set is allocated the shift.

### Time Off Reason

When you want to give an employee a time off you can define the reason for the time off in the masters section.

### Company Structure

__Holiday__- This is where you define the holidays that the company recognizes. If holidays arenot defined in the system and employees don't clock the system picks absent.
in this new system if you check the repeat holiday checkbox and assign a date for the holiday, you'll not have to redefine the holiday the succeeding years.
If the holiday falls on a weekend and is pushed to a Monday, you'll have to recreate it manually and slect the monday date but do not select the repeat option.

## EMPLOYEE

### Employee Details

This section shows the list of employees and the information captured by the system
click the ADD BUTTON in BLUE TO capture new employee and their details.
**Fields with red asteric are mandatory.**
Save the info at the bottom of the page

**NB: EMPOYEES INFO CAN ONLY BE ADDED VIA TA instead of Paymaster. all other info can be added IN THE PAYMASTER OR TA**

To key in all other info other than the employee details click on the details icon on the top right of the screen you'll get the other data to be field( address, contact email, contact phone, national id, qualification, bank, statutory, contract, probation, renumeration, and any other info missing in the employee information)

on the employeee info if the **clocking card number is not assigned** you go to clocking card management

## CLOCKING CARD MANAGEMENT

Clocking card number is a unique identifier assigned to each employee that the system uses to track their working hours.

### Card List

Shows the details of the clocking card numbers assigned to particular employees and those are not assigned.
__To add a new clocking card number__ just click the add button and enter the start number that you want to use. the system will auto generate the rest of the digits to give 10 digits
When you search the card in the card list the card status shows available
__on the last column on status click on assign__ and search the employee and input the allocation date (the date that the employee started to clock, if you dont remember input the date of joining)

## EMPLOYEE

### Employee Separation

__In the old system__ you had to return card and then separate the employee.
__In the new system__ there is a setting to automatically return card upon separation.
On the card replacement reason there should be a reason defined e.g Resigned, Terminated
On the __general setup- configurations- employee setting- separation setting__ on the separation setting check the auto surrender icard on Employee Separation option
To separate an employee go to __employee-separation-request type__ select request type being the reason for the separation.
__employee-separation-request__ select employee payroll number, request type, enter date, and all the red asterics to be field.

The difference between the new and old system is that when employee is separated their details is greyed when you search the employee but in the new system, the employee wont be visible unless you check the separated(red icon) on the employee details
on the old system there was no separate list for the separated employees

The system has the option to rejoin the employee in future after termination.
__employee-rejoining employment__ enter name and the new rejoining date and remarks(reason for joining)
NB: You cannot delete an employee in the system. The employee history is important if they are to be rejoined

## LEAVE

### Setup

#### Leave Master

This is where the leaves are defined
click on the add button and enter the leave information as defined in the old system
#### Leave Assignment 
__how to apply leave__
__how to do leave assignment__
Is the process of making an employee eligible for a leave
select payroll number, select leave name, click the checkbox at the top of the entry created at the bottom to select all then save at the bottom.
#### Opening
**opening balance**
The essence of giving leave opening balances to an employee lies in ensuring accurate and fair tracking of their entitled time off from the very beginning of their employment or a new leave cycle.
If an employee is entitled to 24 days of annual leave per year, their opening balance at the start of the year would be 24 days. If they are hired mid-year, the opening balance might be prorated, e.g., 12 days for 6 months.
#### Leave Transaction 
This is where you do the leave application. In the sytem  you cannot be able to apply a leave for an employee if they are not leave appplicable under leave assignment and have opening balances in Masters
__leave application__
select employee payroll number, request date(date that you are applying the leave), leave name, from date,and to date
leave days will auto generate
you can adjust if it it a half day leave and which half it will take effect.
In this system there is the option to attach a document

when you save and come back to the leave appplication module, you'll see the leave tht has been applied.

__leave adjustment__
Applicable in the case whereby an employees leave has been approved but you need the employee back to work. if you had applied leave for an employee for 25 days and you need to adjust the leave by 10 days so that they can report back to work for the 5 days, enter the payroll number, leave type, leave adjustment date() and click the drop down button to reveal deduct and enter 5 on the input field.
__leave encachment__
