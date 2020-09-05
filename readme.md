
1.First enter the below deatils in mysql backup script

:: Name of the database user with rights to all tables
set dbuser=root

:: Password for the database user
set dbpass=

:: Error log path - Important in debugging your issues
set errorLogPath="C:\mysqlbackups\dumperrors.txt"

:: MySQL EXE Path
set mysqldumpexe="C:\Program Files\MySQL\mysql 5.6\bin\mysqldump.exe"

:: Error log path
set backupfldr=C:\mysqlbackups\backupfiles\

:: Path to data folder which may differ from install dir
set datafldr="C:\ProgramData\MySQL\MySQL Server 5.6\data"

:: Path to zip executable
set zipper="C:\mysqlbackups\zip\7za.exe"

:: Number of days to retain .zip backup files 
set retaindays=5

:: DONE WITH SETTINGS

2.edit backup s3 script and fill source and detination paths.

3.create 2 tasks in taskschduler windows.
	1.run the mysql script
	2.10 mins interval run s3 sync script