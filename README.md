# LPSOPG-VIRUSES
LPSOPG VIRUSES
Using the sandbox, I found that his loader created two executable files, and then closed ![image](https://github.com/user-attachments/assets/95d55c01-838e-4e5f-a72e-76d85a6da77c)
If earlier the old loader just dropped the Vac Bypass.exe and the miner, now the "new" loader has slightly changed the content that drops to the user 
![image](https://github.com/user-attachments/assets/a9e3d877-0a12-4a19-88c1-1c407fd71276)
Let's analyze the role of each of the processes
1. cli_gui.exe - An ordinary loader that weighs absolutely nothing, for some reason has a primitive debugger check and generally plays the role of an LLA injector with the NtOpenFile patch.
![image](https://github.com/user-attachments/assets/f9a68ef0-c40d-4828-ad68-61d563937898)
2. updater.exe - A miner that is presented as a Microsoft Edge Updater with a browser icon and a Microsoft signature.

Updater.exe it also completes the same services as the miner of the previous patient, it is not difficult to guess that both patients use the same paste, but with different settings.

For example, the miner of the second patient uses the Process Hollowing technique (What is process hollowing? (techtarget.com )) in a frozen system process dialer.exe , and is already mining there.

(Funny fact, but on some LTSC builds there is no such system process, and the miner, not knowing this, tries to create a process, and fails miserably.)

Special attention should be paid to how exactly the patient crypts the strings, the screenshots are taken from his old loader with the Inuria crack:
![image](https://github.com/user-attachments/assets/053d4df5-4e99-4bd8-9df0-2749e49acd24)

guys dont download it!
