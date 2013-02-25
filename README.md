Timesheet Script
================

The script to be integrated in git for creating time sheet.

## Install

In case of Ubuntu :

1. Open the terminal.
2. Open the file ..gitconfig in Home directory using your favorite text editor. (e.g. gedit, vim, vi)
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

       531d1e1 Puneet[2013-02-11] Added Lorem ipsum in JobBrowserExistenceRule bootstrap.
    ```
3. Enter command `git timesheet <DAY_OF_CURRENT_MONTH>`. This command will show all the git commits after 10th of current month.

    **NOTE**: *DAY_OF_CURRENT_MONTH* must be of two digits. eg: logs 01.

4. Enter the command `git timesheet <DAY> <DAY>`. This command will show all the git commits after first parameter DAY of the current month and before sencond parameter DAY of the current month.

    **NOTE**: The second parameter day's commits are excluded.

5. Enter the command `git timesheet <DATE>`.  This command will show all the commits after specified date.
    
    **NOTE**: Parameter DATE must in format ```yyyy-mm-dd```. Example: 2012-02-12.

6. Enter the command `git timesheet <DATE> <DATE>`. This command will show all the commits after the first date parameter and before the second date parameter.

## Examples

* ###git timesheet
   ```bash

    2dfd305 Puneet[2013-02-11] Fixed mozRankRequestUrlString problem in MozRankCountRule.

    8646c71 Puneet[2013-02-11] Modified scaffold template code.
    
    ```
* ###git timesheet 10
   ```bash

    ec8d7e3 Puneet[2013-02-12] Code generalized in NativeCareerAppLinkExistenceRule and also impl...

    8646c71 Puneet[2013-02-11] Modified scaffold template code.

   ```
* ###git timesheet 05 07
    ```bash

    19dc09b Puneet[2013-02-06] Code refactored & implemented test cases for AssessmentExistenceRule.

    617bec4 Puneet[2013-02-05] Code refactored in SearchExistenceRule & SocialExistenceRule.
    
    ```
* ####git timesheet 2012-12-31
    ```bash

    b1c849c Puneet[2013-01-01] Migration scripts updated.
    
    dfddafc Puneet[2012-12-31] Validation modified.
    
    ```
* ###git timesheet 2012-12-16 2012-12-20
   ```bash

    8726f84 Puneet[2012-12-16] Code refactored in gsps.
    
    cfaf06c Puneet[2012-12-18] Date error fiixed in defaultDate tag.

    3ddec23 Puneet[2012-12-18] Error messages code added in message.properties

    38304ee Puneet[2012-12-19] Fixed creating new user error in UserService.groovy
    
    ```
