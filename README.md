# epf_ListOfNumbers_RequestByDates
Processing to fill the list with random numbers and remove non-negative ones, as well as obtaining data from two registers of information in one query based on dates.

External processing for managed 1C forms. The processing form contains two pages (Task 1 and Task 2).

On the first page there is a field for entering a number, the command "Fill in the list", a list for displaying numbers and the command "Delete unnecessary". 
Values in the range from 8 to 16 (inclusive) can be entered in the numeric field. 
The list contains one column for displaying numbers. 
The "Fill in the list" command generates N random numbers in the range from –(N^2) to N^2, (where N is the number entered by the user), and outputs them to the list in the same random order. 
The minimum value in the list is highlighted in red, the maximum value is highlighted in green. 
The "Delete unnecessary" command removes all non-positive values from the list. 
After deletion, the user is shown a message of the following type (deleted values are ordered in descending order): 
Deleted values: 7 (-4, -15, -62, -98, -135, -177, -201).

On the second page there is only a table of values that is filled in automatically when processing is opened. 
The source data is contained in two independent non-periodic configuration information registers: "Platforms" and "Responsible Entity". 
The PC "Platforms" has one dimension ("Name", type String (length - 150)) and one resource ("DataRelise", type Date (date composition – date only)). 
PC "Responsible Person" has two dimensions: "Dataprime" (Date type (date composition – date only)) and "FULL NAME" (String (length - 150)).
In the table of values, it is necessary to output the full name of the responsible person working at the time of release of each platform from the table. 
The entire logic of data collection must be implemented in a single query.
