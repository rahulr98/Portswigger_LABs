##  Lab Description

![2023-06-18_15-46](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/6325218b-e908-4b16-8252-22a3249babcc)

### Solution

  - Consider an application which contains a file path traversal vulnerability in the display of product images.
  - This application validates that the supplied filename ends with the expected file extension.
  - If an application requires that the user-supplied filename must end with an expected file extension, such as .png, then it might be possible to use a null byte to effectively terminate the file path before the required extension.

![1](https://github.com/rahulr98/Portswigger_LABs/assets/116432525/3b40ead1-a082-42b5-8f5d-7ef968bfb528)
  
