# jizhicms-file-upload
The user avatar upload section in ZhiJi CMS contains a file upload vulnerability, allowing attackers to upload PDF files or other malicious files. For example, attackers can upload PDF files containing malicious XSS code to steal cookies and impact the system.
First, register a user, then go to the user information section.
![image](https://github.com/user-attachments/assets/864d7579-e9b9-4ed4-85f4-4648fd6318af)
select pdf file to upload
![image](https://github.com/user-attachments/assets/c2fd3c6b-de44-43c0-99f3-530933d5994d)
An attacker can upload a PDF file containing malicious XSS code.
![image](https://github.com/user-attachments/assets/b340b83b-c005-4954-bb19-0df45eb2a054)
We found that the upload was successful.
![image](https://github.com/user-attachments/assets/e8a38e63-bd26-4efd-95e8-4d00346da16a)
We can view the returned path; for example, in my local environment:
http://qwertg:82/static/upload/user/head_1.pdf
![image](https://github.com/user-attachments/assets/315e1c35-8620-476f-921b-32d7247330bd)
It can be found that the XSS vulnerability is triggered, causing a pop-up window. It can be found in the website directory that there are malicious files.
![image](https://github.com/user-attachments/assets/c7783886-89b9-4046-953a-9dc5cd6c2ebc)





