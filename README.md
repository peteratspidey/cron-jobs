# cron-jobs
cron job using cron tabs for particular task
## to check current cron jobs
```bash
cron  -l
```
> it will open a file and check for any line starting with * or any number. this line will be the cron job 

## create a bash to get execute
> ex:- to save a file every ten min
```bash
gedit save.sh
```
## add lines this to in .sh file
```bash
#!/bin/bash
cp <file_name_withfile_path> <new_filename_with_path>
```
> save this as save.sh
## make it executable
```bash
chmod +x save.sh
```
## open a cron tab
```bash
cron -e
```
## add cron job in the end of the crontab
```bash
10 * * * * ./save.sh
```
> save this and done !
> this will run this command every ten min
1. is for the min
2. is for the hours (time)
3. is for the day(1-30 , 1,3,4)
4. is for the month (which month =1-4 jan to april)
5. is for the days of the month (monday-wed = 1-3, mon,tue = 1,2)
