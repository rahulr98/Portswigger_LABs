## Lab Description

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/5acbb5cb-a143-439e-a031-ebef8a7bd7e2)

### Solution

  - Consider a shopping application that contains a blind OS command injection vulnerability in the feedback function.
  - The application executes a shell command containing user-supplied product and store IDs, and returns the raw output from the command in its response.
  - Now we are going to add commands in the storeID of the application.

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/c367c1d6-25b9-4d23-99ba-ecade1bbc7c1)

  -  Both the commands get executed and it shows the whoami.

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/93f36de1-3f87-4d5f-9c8a-c92455abc295)
