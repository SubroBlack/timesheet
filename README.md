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

1. Move to git respository using "cd" command.
2. Enter command "git timesheet". The output will be something like as shown below:
    ```bash

       531d1e1 Puneet[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.
    ```
3. Enter command `git timesheet <DAY_OF_CURRENT_MONTH>`. This command will show all the git commits after 10th of current month.

    **NOTE**: *DAY_OF_CURRENT_MONTH* must be of two digits. eg: logs 01.

4. Enter the command `git timesheet <START_DAY> <END_DAY>`. This command will show all the git commits after first parameter DAY of the current month and before sencond parameter DAY of the current month.

    **NOTE**: The second parameter day's commits are excluded.

5. Enter the command `git timesheet <DATE>`.  This command will show all the commits after specified date.
    
    **NOTE**: Parameter DATE must in format ```yyyy-mm-dd```. Example: 2012-02-12.

6. Enter the command `git timesheet <START_DATE> <END_DATE>`. This command will show all the commits after the first date parameter and before the second date parameter.

## Examples

* ###git timesheet
   ```bash

    2dfd305 Puneet[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.

    8646c71 Puneet[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
* ###git timesheet 10
   ```bash

    ec8d7e3 Puneet[2013-02-12] Lorem ipsum dolor sit amet, consectetur adipiscing.

    8646c71 Puneet[2013-02-11] Lorem ipsum dolor sit amet, consectetur adipiscing.

   ```
* ###git timesheet 05 07
    ```bash

    19dc09b Puneet[2013-02-06] Lorem ipsum dolor sit amet, consectetur adipiscing.

    617bec4 Puneet[2013-02-05] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
* ####git timesheet 2012-12-31
    ```bash

    b1c849c Puneet[2013-01-01] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    dfddafc Puneet[2012-12-31] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
* ###git timesheet 2012-12-16 2012-12-20
   ```bash

    8726f84 Puneet[2012-12-16] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    cfaf06c Puneet[2012-12-18] Lorem ipsum dolor sit amet, consectetur adipiscing.

    38304ee Puneet[2012-12-19] Lorem ipsum dolor sit amet, consectetur adipiscing.
    
    ```
