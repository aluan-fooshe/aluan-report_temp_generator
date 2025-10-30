# aluan-report_temp_generator
#### ```**⚠️ Note: This README belongs to the aluan-report_temp_generator repository.**```
Python scripts and windows powershell scripts that automatically generate MLA/APA reports and essays for most classes. 

## Important Notes & Updates

----
#### 1. Incorrect documentation for another repository

The contents that are listed here below was misplaced in the ```aluan-daily_log_entries/README.md```!

- [aluan-daily_log_entries README.md](https://github.com/aluan-fooshe/aluan-daily_log_entries/blob/main/README.md)
- [aluan-daily_log_entries repository](https://github.com/aluan-fooshe/aluan-daily_log_entries/)
#### 2. UTF-8 vs UTF-16

The encoding of the ".txt file" is very important to list in this function in Filelist_workbook.py;

    def import_dictionary(self, filename):
        dictionary = {}
        item0 = []

        try:
            f = open(filename, 'r', encoding='utf-16')
            list = f.readlines()
            for item in list:
                item = item.strip('\n')
                item0.append(item)

**Problem:** The `.txt` file is saved in UTF-16 encoding, but Python's default file reading uses UTF-8 encoding. This mismatch causes garbled text with visible byte order marks (ÿþ) and extra spaces between characters.

**Solution:** Explicitly specify the encoding when opening the file:

    f = open(filename, 'r', encoding='utf-16')

**Note:** Always match the encoding parameter to how the file was actually saved. Common Windows programs may save files in UTF-16, while most modern systems default to UTF-8.

**Documentation worth citing ↓**

---
4.7. UTF-8 mode
Added in version 3.7.

Windows still uses legacy encodings for the system encoding (the ANSI Code Page). Python uses it for the default encoding of text files (e.g. locale.getencoding()).

This may cause issues because UTF-8 is widely used on the internet and most Unix systems, including WSL (Windows Subsystem for Linux).

You can use the Python UTF-8 Mode to change the default text encoding to UTF-8. You can enable the Python UTF-8 Mode via the -X utf8 command line option, or the PYTHONUTF8=1 environment variable. See PYTHONUTF8 for enabling UTF-8 mode, and Python install manager for how to modify environment variables. [1]

---
Hello giriv_1210,

Good day! Thank you for bringing this to our Microsoft Community Forum.

I understand how frustrating it can be when the same .txt file behaves differently across different systems and versions of Outlook. Let’s work through this together.

The issue you’ve described seems to be related to how Outlook on Windows 11 interprets the encoding of .txt file attachments, defaulting to UTF-16 LE instead of UTF-8. This can cause the file to appear unreadable if the system or application isn’t set to interpret UTF-16 correctly. [2]

----
## C.A.R.T. - Carry Assist Robotic Transport
### ECE 129A CAPSTONE Project Proposal (Fall 2025)

  Project 10  
  C.A.R.T. - Carry Assist Robotic Transport (Robotic Cart)  
  Project Brief: [Carry_Assist_Robotic_Transport__ProjectBrief.pdf](Carry_Assist_Robotic_Transport__ProjectBrief.pdf)  
  Presentation: [Carry_Assist_Robotic_Transport__Slideshow.pdf](Carry_Assist_Robotic_Transport__Slideshow.pdf)

<img src="CART__ProjectBrief_thmbnl.png" width="385px" align="center">

If you are.... 
- a classmate of mine in **S.C. Petersen**'s class
- part of a **STEM-affiliated club**
  - Slugbotics
  - Rocket Team
  - etc.
- a professor from the **University of California, Santa Cruz** 
- interested in *becoming a stakeholder* for this project pitch idea

and are interested in reaching out to me and add yourselves to my stakeholders list, email me for further interest;

aluan@ucsc.edu

<img src="robotic-cart.png" width="385px" align="center">

----
### References

[1] Python Software Foundation, "Built-in Functions", Python 3.14.0 Documentation. 
[Online]. Available: https://docs.python.org/3/library/functions.html#open. 
[Accessed: Oct. 25, 2025].

[2] Microsoft Ignite, "Same .txt file opens in utf-8 encoding in windows 10 outlook and utf-16 le unreadable format on windows 11 outlook", by Anonymous. 
[Online]. Available: https://learn.microsoft.com/en-us/answers/questions/4661269/same-txt-file-opens-in-utf-8-encoding-in-windows-1. 
[Accessed: Oct. 25, 2025].

[3] CodeTwo, "Non-Latin or accented characters are displayed incorrectly in emails". [Online]. Available: https://www.codetwo.com/kb/incorrect-characters-in-emails/

