## LAB DESCRIPTION
![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/d550309b-9c9f-457f-81b3-e3bac59e81bf)

### Solution

  - Modify the category parameter, giving it the value '+UNION+SELECT+NULL--. Observe that an error occurs.
 
![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/7e080970-6033-4bc4-9a00-37bfe045ee4d)

  - Modify the category parameter to add an additional column containing a null value:'+UNION+SELECT+NULL,NULL--

![2](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/049ce3db-66e1-4c87-9a87-2249375c682f)
