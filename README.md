#Form Grabber

Form grabber is a method of capturing web form data. 
This project is the result of a school research project and a proof of concept.

It should not be used for malicious purposes !

Happy learning.

## How it works

0. The form grabber is hidden on a corrupted and malicious PDF file.
1. The user opens the PDF file on a windows machine.
2. His machine gets infected : Hidden code on the PDF file is exectued.
3. The malicious code injects some code on the firefox process by using the well known CreateRemoteThread & WriteProcessMemory technique

   a. It injects a "POST parser" on the firefox's PR_Write method.
   This parser detects when a HTTP POST command is sent and grabs login and passwords.
   
   b. It sends the information to a remote server
   
 This proof of concept offers some similar functionnalities to those offered by the zeus trojan : http://www.secureworks.com/research/threats/zeus/