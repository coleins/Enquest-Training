# TIME AND ATTENDANCE TRAINING

At the start of the meeting **share the link to the server** with the trainees. The link should have ip address and not local host if the server and client are on the same network.

## DASHBOARD

Overview of what you are going to expect in the system

### Total Head Count

active number of employees in the organization

### Present

total number of employees present as of today

### Absent

total number of employees absent as of today, reason may be failure to clock in, or those on leave and information has not been updated in the system, those who are on their weekly off but their info is not updated in the system

### Late in

indidcates the number of employees who have clocked in late as of the start time of their shift.

### Early Out

employees have clocked out earlier than the end of the shift as of today

### On Leave

Indicates the number of employees on leave as of today. if the leave is captured corerectly it will show on leave card. if not it will appear on the absent card.

### Weely Off

is when employees are on their resting day. indicates the number the number of employees whose weekly off is the present day. if the weekly off is captured corerectly it will show on weekly off card. if not it will appear on the absent card.

### Holiday

the system allows the user to add and customize holidays. the holiday in the dashboard therefore indicates the number of employees who have clocked in during the holiday. The system will indicate the hours that the employees are entitled to be paid for working during holidays. if there are employees whose shift is schedule to include the holidays will be marked as present if the clock in and absent is if they fail to clock in.

### Compensatory Off/ C-Off

This captures the information for employees who have been assigned compensatory off. that is, if they have worked on their weekly off or during the holidays if asked by management.

### Contract expired

if employees are under contract. those whose contract has expired as of the present day are displayed on the dashboard.

## MASTERS

similar to the old TA, Used to adding new or edit existing entries.

### Placement Masters-

#### To add a department

when you click on department it shows the existing departments. The systems has an ADD BUTTON that is BLUE in color.
The fields with a red asteric are mandatory fields.

#### To edit the department

that has been created you click on the department edit to your liking and select the UPDATE BUTTON that is GREEN in color.

#### To delete a department

click on the department and select the DELETE BUTTON that is RED in color.

**same logic goes to the other fileds(Sub department, designation, category, class, position, master one, master two, location)**

### Shift

Used to define the shifts that the employess are assigned.

#### To define a shift

in the new system, you need to select shift type- normal
shift code can be same as shift name so that once the shift has been allocated to an employee you can be able to understand the shift better and different the different shift allocated to that particular employee.
The best practice is to use the shift name and in brackets the start and end time of the shift. e.g NORMAL SHIFT(07:30 to 16:45)

#### To define the break

click on Add a new record
e.g Lunch break Start time 13:00 End Time 14:00
Applicable on - set the days which the shift will be applicable

#### Time Range

depending on how the employees clock, any employees who clock between the time set is allocated the shift.

### Time Off Reason

When you want to give an employee a time off you can define the reason for the time off in the masters section.

### Company Structure

#### Holiday

This is where you define the holidays that the company recognizes. If holidays arenot defined in the system and employees don't clock the system picks absent.
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
**To add a new clocking card number** just click the add button and enter the start number that you want to use. the system will auto generate the rest of the digits to give 10 digits
When you search the card in the card list the card status shows available
**on the last column on status click on assign** and search the employee and input the allocation date (the date that the employee started to clock, if you dont remember input the date of joining)

## EMPLOYEE

### Employee Separation

#### In the old system

you had to return card and then separate the employee.

#### In the new system

there is a setting to automatically return card upon separation.
On the card replacement reason there should be a reason defined e.g Resigned, Terminated

#### general setup- configurations- employee setting- separation setting

on the separation setting check the auto surrender icard on Employee Separation option

#### employee-separation-request type

To separate an employee select request type being the reason for the separation.

#### employee-separation-request

select employee payroll number, request type, enter date, and all the red asterics to be field.

The difference between the new and old system is that when employee is separated their details is greyed when you search the employee but in the new system, the employee wont be visible unless you check the separated(red icon) on the employee details
on the old system there was no separate list for the separated employees

#### employee-rejoining employment

The system has the option to rejoin the employee in future after termination. enter name and the new rejoining date and remarks(reason for joining)
NB: You cannot delete an employee in the system. The employee history is important if they are to be rejoined

## LEAVE

### Setup

#### Leave Master

This is where the leaves are defined
click on the add button and enter the leave information as defined in the old system

#### Leave Assignment

**how to apply leave**
Is the process of making an employee eligible for a leave
select payroll number, select leave name, click the checkbox at the top of the entry created at the bottom to select all then save at the bottom.

#### Opening

##### opening balance

The essence of giving leave opening balances to an employee lies in ensuring accurate and fair tracking of their entitled time off from the very beginning of their employment or a new leave cycle.
If an employee is entitled to 24 days of annual leave per year, their opening balance at the start of the year would be 24 days. If they are hired mid-year, the opening balance might be prorated, e.g., 12 days for 6 months.

### Leave Transaction

This is where you do the leave application. In the sytem you cannot be able to apply a leave for an employee if they are not leave appplicable under leave assignment and have opening balances in Masters

#### leave application

select employee payroll number, request date(date that you are applying the leave), leave name, from date,and to date
leave days will auto generate
you can adjust if it it a half day leave and which half it will take effect.
In this system there is the option to attach a document

when you save and come back to the leave appplication module, you'll see the leave that has been applied.

#### leave adjustment

Applicable in the case whereby an employees leave has been approved but you need the employee back to work. if you had applied leave for an employee for 25 days and you need to adjust the leave by 10 days so that they can report back to work for the 5 days, enter the payroll number, leave type, leave adjustment date() and click the drop down button to reveal deduct and enter 5 on the input field.

#### leave Encashment

Applicable for instance if an employees has a leave balance of 15 days and there is an agreement that they go for 5 days and are paid for the remeinder of the days instead.

## Time and Attendance

### Shift Schedule Management

Select the shift schedule type to be either employee wise or bulk update
For either all employees or specific employees, click on shift management at the bottom(blue button) then choose the shift, day type and duration applicable.
For weekly offs and compensatory offs/ c-off if an employee is supposed to be on a weekly of on the first and last friday of the month,

### Out Station Visit

Refers to an employee's work-related travel to a location outside their usual workplace.
Rather than marking them as present manually, you can assign them an outstation visit which will mark them as present with a remark of outstation visit.

click on add and fill all the info that is required
Entry Date is the date when the employee is eligible for the out station visits(you can input present day if not advised). Can only be approved using admin account.

### Time Off

Time off is a period of time where an employee is not working. The employee may use this time to rest, travel, or take care of personal matters.

### Process Attendance Data

In the old system you used to go to the commaster software, and download data and come to the TA and download again before processing
In the new system, you download data in the commaster software only, in the new system it is auto downloaded
and auto process the data.
You only come to check reports
NB: IF THE REPORT IS NOT VISIBLE YOU CAN PROCESS MANUALLY

### Attendance Register

when you enter the payroll number of the employee you want to view their attendance, it displays the shift, shift time, in time, out time, clocked hours, pay hours, status whether present or absent.
On the description column it will show the remarks for the present ones who are on out station visits

### Pass Data to Payroll

If the employee passes ot1, ot2, lost hours or absenteeism data to payroll, check the checkbox at the bottom. Ensure to adjust the input fields accordingly.
