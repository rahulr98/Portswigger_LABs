## Lab Description

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/0b7f602f-e430-4aaa-9edd-a0d830860c49)

### Solution

  -  Consider a shopping application that displays images of items for sale.
  -  Next, we have to change the filename of the application using Burp Suite.
  -  We can see the _filename_ parameter, change the default value to `../../../etc/passwd`.
  -  When this change get executed, it goes back to the parant directory and gets access to the root `/etc/passwd`.

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/480866bc-cc30-4c0f-b27b-5f2b2e5fcdee)
