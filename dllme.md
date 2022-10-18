# How to manually register a DLL or OCX file
A DLL file is a module containing certain functions that can be used by multiple programs as long as it is registered. Please follow the steps below to manually register a DLL file. 

## Answer:

* NOTE 1: Users need to be logged in as a [Local Administrator](https://kb.blackbaud.com/knowledgebase/articles/Article/79900) to register files. 

* NOTE 2: A DLL created in .NET will need to be registered using the REGASM utility. For example: "C:\Windows\Microsoft.NET\Framework\v4.0.30319\regasm" "C:\Program Files (x86)\Blackbaud\The Raisers Edge 7\Plugins\[name of plugin].dll" /codebase /tlb

## Windows Server 2012,  Windows 8, Windows Server 2012 R2, Windows 8.1, or Windows 10:
The Start button is hidden in these versions of Windows.  To see the Start button, move and hover your cursor over the lower left corner of  the desktop where the Start button was in previous versions of Windows.
Right-click on the Start button that appears, you will see a menu. Select Command Prompt (Admin).
You will see the command prompt window open with the wording "Administrator: Command Prompt" at the top of the Window.
At the command prompt, enter: REGSVR32 "PATH TO THE DLL FILE" 
~~~
           Example: How to register the RE7Outlook.dll file: 
           REGSVR32 "C:\Program Files\Blackbaud\The Raisers Edge 7\DLL\RE7Outlook.dll"
           If using a 64-bit operating system, then the command would be:  
           C:\Windows\SysWOW64\REGSVR32 "C:\Program Files (x86)\Blackbaud\The Raisers Edge 7\DLL\RE7Outlook.dll" 
~~~
* Note:  Be sure to include the quotation marks if the path contains any spaces. 
  
## Windows 7, Windows Server 2008 or Windows Server 2008 R2:

If User Account Control (UAC) is enabled, then you will need to register the DLL file from an elevated Command prompt by completing the following steps:
Click Start > All Programs > Accessories and right-click on "Command Prompt" and select "Run as Administrator" OR in the Search box, type CMD and when cmd.exe appears in your results, right-click on cmd.exe and select "Run as administrator"
At the command prompt, enter: REGSVR32 "PATH TO THE DLL FILE" 
           Example: How to register the RE7Outlook.dll file:
~~~
          REGSVR32 "C:\Program Files\Blackbaud\The Raisers Edge 7\DLL\RE7Outlook.dll"
           If using a 64-bit operating system, then the command would be:  
           C:\Windows\SysWOW64\REGSVR32 "C:\Program Files (x86)\Blackbaud\The Raisers Edge 7\DLL\RE7Outlook.dll" 
           Note:  Be sure to include the quotation marks if the path contains any spaces.
~~~

If User Account Control (UAC) is disabled, then complete the following:
Press and hold the Windows key then press R. 
Enter cmd in the Run line and click OK. 

At the command prompt, enter: REGSVR32 `"PATH TO THE DLL FILE"`
 
Example 1: How to register the RE7Outlook.dll file: 
~~~
REGSVR32 "C:\Program Files\Blackbaud\The Raisers Edge 7\DLL\RE7Outlook.dll"
If using a 64-bit operating system, then the command would be:
C:\Windows\SysWOW64\REGSVR32 "C:\Program Files (x86)\Blackbaud\The Raisers Edge 7\DLL\RE7Outlook.dll"
~~~
* Note:  Be sure to include the quotation marks if the path contains any spaces.

Example 2: How to register a system file:
~~~
REGSVR32 C:\Windows\System32\example.dll
~~~
If using a 64-bit operating system, then the command would be:
~~~
C:\Windows\SysWOW64\REGSVR32 C:\Windows\SysWOW64\example.dll
 ~~~
Click `OK`. 
OR 
Click `Start`, Run or press and hold the `Windows key` then press `R`. 
Type `REGSVR32` in the Run line 
Press the `Space` button on the keyboard
From the file location of the `.dll` file, select/highlight the pertinent `.dll` file
Drag and drop the selected/highlighted `.dll` file into the Run line after the space (Sample command: `REGSVR32 "C:\Program Files (x86)\Blackbaud\The Raisers Edge 7\DLL\RE7Outlook.dll"`) 
* Note:  Be sure to include the quotation marks if the path contains any spaces.
Click `OK `
 
### Additional Information:
* To unregister DLL files, refer to [`48728`](https://kb.blackbaud.com/knowledgebase/articles/Article/48728).
 
* To register all DLL files for The Raiser's Edge, refer to [`How to download and run the REREGISTER utility`](https://kb.blackbaud.com/knowledgebase/articles/Article/37558).

# How to download and run the REREGISTER utility
The REREGISTER utility is used to register all Raiser's Edge files. 

To run `REREGISTER.EXE`:

Browse to the folder that was created during the extraction of the installation file download from [Blackbaud.com](https://kb.blackbaud.com/knowledgebase/) or the Deploy folder ([How to locate the Deploy folder](https://kb.blackbaud.com/knowledgebase/articles/Article/38496)) and open the "Tools" folder.
Right-click the `REREGISTER.EXE` file and select Run as Administrator. 
On the "REREGISTER - The Raiser's Edge 7" screen, click `Start`.
* Note: To manually register a DLL file, review [How to manually register a DLL or OCX file (18569)](https://kb.blackbaud.com/knowledgebase/articles/Article/48280). To unregister a DLL file, review [How to manually unregister a DLL file](https://kb.blackbaud.com/knowledgebase/articles/Article/48728) (13323).

This file has been downloaded from https://www.dllme.com.