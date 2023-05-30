## Lab Description
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/cc5e7b82-fc46-49c0-a39c-cb7cdc41d568)

### Solution

  - Here, TrackingID parameter is vulnerable. This is a blind SQL injection since response is not diplayed back.We can perform a SQL injection on trackingID parameter

`SELECT trackingId FROM someTable WHERE trackingId = '<COOKIE-VALUE>' AND 1=1-- '`

  - There maybe 2 results - TrackinID does/does not exist. **Condition(1=1) = TRUE -> Welcome back message is shown**.

 `SELECT trackingId FROM someTable WHERE trackingId = '<COOKIE-VALUE>' AND 1=1-- '`
 
![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/2d5ebb6f-b7b3-4286-bf6e-61b3c713d77a)

  - **Condition(1=2) = FALSE -> Welcome back message is not shown**.

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/d77c54e6-b1fa-4bb6-ad0d-5ba4a68768f4)

  - To determine how many characters are in the password of the administrator user. To do this, change the value to, 
  - And send a series of follow-up values to test different password lengths. Send:

`TrackingId=xyz' AND (SELECT 'a' FROM users WHERE username='administrator' AND LENGTH(password)>1)='a`.

![3](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/fada31b8-7927-4f02-a58b-729e8ccbd37e)

  - This confirm that the password is greater than 2, Now we can send the value 50.

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/7b86a97d-2e40-4d11-b847-fd7351f54215)

  - We don't get any message which means the password should be lesser than 50.
  - 
