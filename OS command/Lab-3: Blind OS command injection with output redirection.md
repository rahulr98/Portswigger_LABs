##  Lab Description

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/dfa0c979-ddd5-46e3-b8a5-f6176acd8a63)

### Solution

  -  Consider a shopping application that contains a blind OS command injection vulnerability in the feedback function.
  -  The application executes a shell command containing the user-supplied details. The output from the command is not returned in the response. However, we can use output redirection to capture the output from the command.

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/dcc76834-838f-49cb-b7cb-cb884a189d08)

  -  The application serves the images for the product catalog from this location. We can redirect the output from the injected command to a file in this folder, and then use the image loading URL to retrieve the contents of the file. We now give the command 'whomai' and save it as a file.
  -  We now give the saved file as the filename.

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/992914e5-55a7-4c3b-9c07-80b193d6041c)
![2023-06-06_06-51](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/081576ee-0dfe-4145-a048-14d94ecb425d)
