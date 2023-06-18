## Lab Description

![image](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/d6579e86-e73d-42a7-bad0-efbc1cff0d1c)

### Solution

  - Consider a shopping application with file path traversal vulnerability in the display of product images.
  - The application transmits the full file path via a request parameter, and validates that the supplied path starts with the expected folder. Now we edit the filename of the application.
  - Since the application has implemented a rule to strictly add the file path of the images, we give a special techniques.

![2023-06-14_18-06](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/2ecb33db-a6ec-457a-88b8-ef9a7f35bc1f)
