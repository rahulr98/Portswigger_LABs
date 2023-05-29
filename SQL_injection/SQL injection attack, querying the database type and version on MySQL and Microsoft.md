## Lab Description
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/bc3372da-eba2-49da-a53d-73318a0bbcae)

### Solution
- Determine the number of columns that are being returned by the query and which columns contain text data. 

- Use the following payload to display the database version:

`'+UNION+SELECT+@@version,+NULL#`

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/591b231e-65c9-450f-a9aa-f6e5c5abdfe8)

The database type and version are displayed.

![3](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/63259223-d3d9-419c-83db-b10dc469b6b9)

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/d0a091be-4f7e-41c4-9a07-bbb657b6cdfc)
