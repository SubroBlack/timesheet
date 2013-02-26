Timesheet Script
================

The script to be integrated in Git for creating time sheet.

## Installation

In case of Ubuntu :

1. Open the terminal.
2. Open the file .gitconfig in Home directory using your favorite text editor. (e.g. gedit, vim, vi)
3. Add the script in the alias block as shown below.

    ```
      [alias]
        timesheet = ! <PATH_TO_SCRIPT_FILE>/timesheet

    ```

## Usage

Once you are done with the installation part. Just open new terminal and follow steps:

1. Move to Git respository using "cd" command.
2. Enter command "git timesheet". The output will be something like as shown below:
    ```bash

       531d1e1 Puneet[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.
    ```
3. Enter command `git timesheet <DAY_OF_CURRENT_MONTH>`. This command will show all the git commits after 10th of current month.

    **NOTE**: *DAY_OF_CURRENT_MONTH* must be of two digits. eg: logs 01.

4. Enter the command `git timesheet <START_DAY> <END_DAY>`. This command will show all the git commits after first parameter DAY of the current month and before sencond parameter DAY of the current month.

    **NOTE**: The second parameter day's commits are excluded.

5. Enter the command `git timesheet <DATE>`.  This command will show all the commits after specified date.
    
    **NOTE**: The Parameter DATE must in format yyyy-mm-dd, for example: 2012-02-12.

6. Enter the command `git timesheet <START_DATE> <END_DATE>`. This command will show all the commits between the specified dates.

7. Enter the command `git timesheet <AUTHOR_NAME>`. This command will show all the commits for the specified author.

8. Enter the command `git timesheet <START_DAY> <AUTHOR_NAME>`. This command will show all the commits for the specified author after a specified day of current month. 

9. Enter the command `git timesheet <START_DAY> <END_DAY> <AUTHOR_NAME>`. This command will show all the commits for the specfied author between the specified days of the current month. 

10. Enter the command `git timesheet <START_DATE> <AUTHOR_NAME>`. This command will show all the commits for the specified author after the specified date.

11. Enter the command `git timesheet <START_DATE> <END_DATE> <AUTHOR_NAME>`. This command will show all the commits for the specified author between the specified dates.

    **NOTE**: The <AUTHOR_NAME> could be an abbrivation, for example puneet behl as pun.

## Examples

* ###git timesheet
   ```bash

    2dfd305 Puneet[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.

    8646c71 Puneet[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
   ```
* ###git timesheet abhi
   ```bash

    2dfqw1e Abhishek[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```      
* ###git timesheet 10
   ```bash

    ec8d7e3 Puneet[2013-02-12] Lorem ipsum dolor sit amet, consectetur adipiscing.

    8646c71 Puneet[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.

   ```
* ###git timesheet 10 abhi
   ```bash

    efdfd7e Abhishek[2013-02-12] Lorem ipsum dolor sit amet, consectetur adipiscing.

   ```
* ###git timesheet 05 07
    ```bash

    19dc09b Puneet[2013-02-06] Lorem ipsum dolor sit amet, consectetur adipiscing.

    617bec4 Puneet[2013-02-05] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
* ###git timesheet 05 07 abhi
    ```bash

    19dcdsb Abhishek[2013-02-06] Lorem ipsum dolor sit amet, consectetur adipiscing.

    d17bec4 Abhishek[2013-02-05] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
* ####git timesheet 2012-12-31
    ```bash

    b1c849c Puneet[2013-01-01] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    dfddafc Puneet[2012-12-31] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
* ####git timesheet 2012-12-31 abhi
    ```bash

    b1c849d Abhishek[2013-01-01] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    dfddafs Abhishek[2012-12-31] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
* ###git timesheet 2012-12-16 2012-12-20
   ```bash

    8726f84 Puneet[2012-12-16] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    cfaf06c Puneet[2012-12-18] Lorem ipsum dolor sit amet, consectetur adipiscing.

    38304ee Puneet[2012-12-19] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
  ```
* ###git timesheet 2012-12-16 2012-12-20 abhi
   ```bash

    8726f81 Abhishek[2012-12-16] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    cfaf0b4 Abhishek[2012-12-18] Lorem ipsum dolor sit amet, consectetur adipiscing.

    38304e2 Abhishek[2012-12-19] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
