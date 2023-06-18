## Lab Description

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/5acbb5cb-a143-439e-a031-ebef8a7bd7e2)

### Solution

  - Consider a shopping application which contains a blind OS command injection vulnerability in the feedback function.
  - The application executes a shell command containing the user-supplied details. The command is executed asynchronously and has no effect on the application's response. It is not possible to redirect output into a location that you can access. However, you can trigger out-of-band interactions with an external domain.
  - Now in this application we give a nslookup command with a burp created website.

![2023-06-14_18-06](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/9f8a17c2-2a31-4b60-a0d0-25c4feab6848)
