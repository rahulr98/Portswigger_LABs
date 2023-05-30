## Lab Description
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/aabfa816-e3b3-4be1-951e-434e39d452ea)

### Solution

  - Cause a 10 sec delay in response
  - Modify the TrackingId cookie, changing it to:

`TrackingId=x'||pg_sleep(10)--`

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/557511d5-0747-4fa5-a22f-122c8c038bec)

  - We get a response after 10 sec which confirms the SQL injection vulnerability.
  - SLEEP command differs for each type of databse, here we find it by trial & error method that it is a POSTgreSQL database

![2023-05-31_00-02](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/d53c886c-83e3-482c-b896-fa3e058464bf)

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/1ba8dbc6-4114-4bdc-a35f-dbc4632aad20)
