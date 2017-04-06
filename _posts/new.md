



##Robocopy Lines
robocopy.exe <DRIVE>:UsersShares \<NEW_SERVER><NEW_DRIVE>$UsersShares /Z /R:5 /COPYALL /MIR /FP /LOG+:<DRIVE>:UserShares.log /TEE /XF UserShares.log 

(where DRIVE is drive letter, where shares are located, NEW_SERVER is the name of the new server and NEW_DRIVE is the destination drive letter on the new server).

Example: robocopy.exe C:UsersShares \My_NewServerD$UsersShares /Z /R:5 /COPYALL /MIR /FP /LOG+:C:UserShares.log /TEE /XF UserShares.log

robocopy.exe <DRIVE>:<OLD_FOLDER> \<NEW_SERVER><NEW_DRIVE>$<NEW_FOLDER> /Z /R:5 /COPYALL /MIR /FP /TEE /XF /LOG+:<DRIVE>:ShareLog.log 