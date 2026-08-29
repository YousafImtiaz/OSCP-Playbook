Upload the report from your Kali Linux VM to prevent possible issues that may occur.

> Use 7z to create a zip file with the PDF:

```
7z a OSCP-OS-xxxxxxxx-Exam-Report.7z OSCP-OS-xxxxxxxx-Exam-Report.pdf
```

> Generate md5sum for the zip file:

```
sudo md5sum OSCP-OS-xxxxxxxx-Exam-Report.7z  
```

> After uploading the report to the upload portal use the python script below to verify that the md5sum we generated and the one from the upload portal matches before you submit:

Tool here: https://github.com/YousafImtiaz/SumCheck

```
python3 sumcheck.py
```


