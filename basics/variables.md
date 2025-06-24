 - When referring to or reading a variable we place a $ sign before the variable name.
 - When setting a variable we leave out the $ sign.

### SPECIAL VARIABLES 
There are a few other variables that the system sets for you to use as well.

- $0 - The name of the Bash script.
- $1 - $9 - The first 9 arguments to the Bash script. (As mentioned above.)
- $# - How many arguments were passed to the Bash script.
- $@ - All the arguments supplied to the Bash script.
- $? - The exit status of the most recently run process.
- $$ - The process ID of the current script.
- $USER - The username of the user running the script.
- $HOSTNAME - The hostname of the machine the script is running on.
- $SECONDS - The number of seconds since the script was started.
- $RANDOM - Returns a different random number each time is it referred to.
- $LINENO - Returns the current line number in the Bash script.


## SETTING OUR OWN VARIABLES
We may also set our own variable 

variables may be set by many ways  (such as part of the execution of a command) but the basic form follows this pattern:
variable=value

INPUT : ![Screenshot from 2025-06-24 11-21-41](https://github.com/user-attachments/assets/40f4c5f9-aa2b-410a-8781-863a2c4cf042)


OUTPUT:![image](https://github.com/user-attachments/assets/6293a05f-9448-464a-a8b2-f67a52480693)


When we enclose our content in quotes we are indicating to Bash that the contents should be considered as a single item
**WE** may use single quotes ( ' ) or double quotes ( " ).
Single quotes will treat every character literally.
Double quotes will allow you to do substitution (that is include variables within the setting of the value).

![image](https://github.com/user-attachments/assets/c2981b88-793f-403b-a1c9-989a5fb7a81b)


- variable=$( command )
Save the output of a command into a variable
*** here we noticed that formatting and case sensitiveness is their in variables *** 
- exporting variables
variables are limited to the process they were created in
for instance, a script may run another script as one of its commands. If we want the variable to be available to the second script then we need to export the variable.


## USER INPUT 
for inputing the user we use read , the command takes the input and will save it to the variable 
![image](https://github.com/user-attachments/assets/83eb469a-15e8-4072-980d-1c483f4bd816)

![image](https://github.com/user-attachments/assets/0b14eb90-58ad-48e9-94dc-25a88fefb202)

-- **echo is here to print the statement**


**we can also use -p and -sp which is also inside read for further functionalities ,-p means prompt ,-sp means silent input**
![Screenshot from 2025-06-24 12-01-13](https://github.com/user-attachments/assets/b43313f5-89de-44b9-adcc-8350d3e956d7)
![image](https://github.com/user-attachments/assets/077f50c5-a3db-4726-95cb-4ac268f1b180)


**cat is used to show the file**

### ARITHMETIC 
let is a builtin function of Bash that allows us to do simple arithmetic ,It follows the basic format:
let <arithmetic expression>
![image](https://github.com/user-attachments/assets/e6f28843-3604-4063-90d2-27bcc6cafd99)
![image](https://github.com/user-attachments/assets/503d2c30-6dfb-453b-a412-5e234d9ad744)

- length of a variable
  we can use echo $(#varname)
  



