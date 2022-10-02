# <p align="center"> Log Tampering

Logs are our friends since they are the breadcrumbs that we have to follow in order to understand what happened and if the need arrives catch the actors.
* One of the most important steps of every actor is to clean the crime scene, that’s why it is important to understand how they mess with the logs.
* Disable Auditing: This is the first thing they do as soon as they can, this way none of their actions are being logged. For windows the command is “Auditpot” from here one can suppress all the logs or just the ones that will get on the actor’s way. It is also important to go to Event Viewer and make sure to get rid of the event mentioning the disabling of auditing. 
* Clearing Logs: Another obvious step is to clear all the logs or the ones that prove their intrusion.
	* Clearlogs.exe is a file that will clear all the security logs by running “clearlog.exe -sec”, this can be verified on event viewer, obviously the file needs to be erased.
	* Meterpreter is a payload that will clear all the windows logs and present a confirmation window, “meterpreter > clearev”
	* Now in the case of Linux, one needs to use the Shred tool “Shred -vfzu auth.log” will shred and erase the log file.
* Modifying Logs: It is a good idea to change the location of the logs, this way the actor’s job to clean their steps will become harder.
* Deleting Commands: Once a command like bash has been entered, it can be recalled, so the history of the commands can store the data unless it has been cleared (even the shred command) this can be cleared with “~/.bash_history”
* This info is so one can have a glimpse at the actor’s perspective and can be aware of their practices. SIEM is good solution to centrally store the system’s logs.

