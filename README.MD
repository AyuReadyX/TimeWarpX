
                                  TimeWarpX v1.0 




GUI USAGE:(TimeWarpX.exe) Basically Like RunAsDate, set date & browse for exe and click Run/Inject

 
CMD USAGE: .\timewarp.exe [-x32|-x64] YYYY-MM-DD HH:MM [App] [Wildcards...]
            <-------------------Mandatory------------------>  <-Optional->

   Ex: .\timewarp.exe -x64 2017-09-24 09:30 testdate64.exe
   Ex: .\timewarp.exe -x32 2025-05-11 06:00 testdate32.exe App2 App3
   Ex: .\timewarp.exe -x64 2019-02-19 18:00 "C:\Program Files\testdateapp\testdate64.exe" App2 App3
OR       
           .\timewarpx32.exe YYYY-MM-DD HH:MM TestDate32.exe [Wildcards...]
            <-------------------Mandatory------------------>  <-Optional->
           .\timewarpx64.exe YYYY-MM-DD HH:MM TestDate64.exe [Wildcards...]
            <-------------------Mandatory------------------>  <-Optional->

Powershell One Liner:Startup
All exe's included accept arguments and run standalone

Ex.
Start-Process -FilePath ".\timewarp.exe" -ArgumentList "-x64", "2024-05-11", "12:00", "C:\Program Files\testdateapp\testdate64.exe", "AppChildProcess1" , "AppChildProcess2" -WindowStyle Hidden


Note: The first argument that is an exe should be the absolute path, unless timewarp is located in
the target exe's directory .

Note: TestApp folder contains 2 calendar apps for testing, 32 and 64 bit

timewarpx.exe: can be used from the CMD/Powershell as well as double clicked to access GUI

timewarp.exe: CMD and PowerShell only, good for autostart with a vbs/powershell script


FALSE POSITIVE:

timewarp.exe(NO GUI) passes all AV , but the GUI definitely triggers AV's, about 19 of them lol
good thing is you dont have to use the GUI at all, all exe's without a GUI is clean on virustotal
timewarpx.exe(GUI) pretty much has all the other exe's baked into it, ill redo the GUI someday but 
im tired lol , too strict . as is its perfect for the use and personally i dont even use the GUI
starts automatically via powershell script at startup . the GUI is just for people who maybe dont
know cmd and powershell 


VIRUSTOTAL:

timewarpx.exe(GUI)
https://www.virustotal.com/gui/file/fe9f27f050d086efeb62fcb99d0bf137e6b246ea2fbbe9695858fbc2fab27432

timewarp.exe(NOGUI)
https://www.virustotal.com/gui/file/c13ba4c17736dea32c29a255b12e78854805764cd05383b146b6c48750f6d935
