# CC 101 Laboratory Activity: Exploring the Windows Command Line

*Sorsogon State University – College of Information and Communications Technology, Bulan Campus*


- **Name:** CARL NATHANIEL B. FUNDANO 
- **Section:** BSCS 1-1 
- **Student ID:** 26117009 
- **Instructor:** JOHN MARK GABRENTINA 

## Introduction

The command line is a text-based interface where you type commands to control your computer instead of clicking on icons and menus. The purpose of this lab activity is to help us get comfortable using both Command Prompt and PowerShell to manage files, check system settings, and run basic tasks. Doing these hands-on steps gives us a better understanding of how the operating system works under the hood. Learning these basic commands helps build a solid foundation for our future programming and computer science subjects.

| Item | Details |
|---|---|
| Course | CC 101 Introduction to Computing (BSCS 1st Year) |
| Course Outcome | CO2: Identify the functions and relationships of major hardware and software components |
| Output | Command Line Exploration Documentation (PDF) |
| Estimated time | 2 to 2½ hours |
| Reference | CC 101 Lecture Notes: Exploring the Windows Command Line |

## Instructions

Follow every step in order, take the screenshots marked **[Screenshot]**, and answer the questions marked **[Answer]** in your documentation.

**Before you start**

- You need a Windows 10 or 11 computer. No administrator rights are needed.
- To take a screenshot, press **Windows + Shift + S**, drag over the terminal window, then paste it (Ctrl + V) into your documentation.
- Replace the sample values (Juan Dela Cruz, BSCS 1-1) with **your own** details.
- Type every command yourself. Do not copy and paste; typing is how you learn.

> **Note on screenshots:** The original PDF contains terminal screenshots. Below, each one is transcribed as a code block. To show the original images on GitHub, save them in an `images/` folder and replace the code blocks with `![Figure X](images/figure-x.png)`.

---

## Part A: Open the Two Shells

1. Press Windows + R, type `cmd`, and press Enter. Type `cls` and press Enter.
2. Type `echo Juan Dela Cruz, BSCS 1-1` (your own name and section) and press Enter.

**[Screenshot] Figure A1**

```
Microsoft Windows [Version 10.0.26200.9457]
(c) Microsoft Corporation. All rights reserved.

C:\Users\carln>echo Carl Nathaniel B. Fundano, BSCS 1-1
Carl Nathaniel B. Fundano, BSCS 1-1
```

3. Press Windows + R, type `powershell`, and press Enter. Type the same echo command, but put the text in quotation marks: `echo "Juan Dela Cruz, BSCS 1-1"`. PowerShell treats the comma as a list separator without them.

**[Screenshot] Figure A2**

```
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS C:\Windows\system32> echo "Carl Nathaniel B. Fundano, BSCS 1-1"
Carl Nathaniel B. Fundano, BSCS 1-1
PS C:\Windows\system32>
```

**[Answer] A-Q1.** Compare the two prompts. What is different, and what does each part of the Command Prompt prompt mean?

-- Command Prompt starts with `C:\Users\carln>` to show the exact folder path I'm working in, where `C:` is the main drive letter and `>` acts as the cursor prompt. On the other hand, PowerShell starts with `PS C:\Windows\system32>`, it adds the PS prefix at the beginning to clearly mark that it's running in PowerShell rather than standard CMD.

---

## Part B: Inspect Your System (Command Prompt)

Use the Command Prompt window for Parts B to D.

1. Run these commands one at a time: `whoami`, then `hostname`, then `ver`.

**[Screenshot] Figure B1**

```
C:\Users\carln>whoami
desktop-l866pj2\carln

C:\Users\carln>hostname
DESKTOP-L866PJ2

C:\Users\carln>ver

Microsoft Windows [Version 10.0.26200.9457]

C:\Users\carln>
```

2. Run the command below. It may take 10 to 30 seconds.

```
systeminfo | findstr /B /C:"OS Name" /C:"OS Version" /C:"System Type" /C:"Total Physical Memory"
```

**[Screenshot] Figure B2**

```
C:\Users\carln>systeminfo | findstr /B /C:"OS Name" /C:"OS Version" /C:"System Type" /C:"Total Physical Memory"
OS Name:                   Microsoft Windows 11 Pro
OS Version:                10.0.26200 N/A Build 26200
System Type:               x64-based PC
Total Physical Memory:     8,088 MB
```

3. Run `ipconfig`. Find the adapter that shows an IPv4 Address.

**[Screenshot] Figure B3**

```
C:\Users\carln>ipconfig

Windows IP Configuration


Ethernet adapter Ethernet:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 1:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Local Area Connection* 2:

   Media State . . . . . . . . . . . : Media disconnected
   Connection-specific DNS Suffix  . :

Wireless LAN adapter Wi-Fi:

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::2e0a:397d:bbdb:76d5%6
   IPv4 Address. . . . . . . . . . . : 192.168.1.5
   Subnet Mask . . . . . . . . . . . : 255.255.255.0
   Default Gateway . . . . . . . . . : fe80::1%6
                                       192.168.1.1
```

**[Answer] B-Q1.** Complete this table in your documentation using your results:

| Item | Your result |
|---|---|
| Logged-in account (whoami) | desktop-l866pj2 |
| Computer name (hostname) | DESKTOP-L866PJ2 |
| OS name | Microsoft Windows 11 Pro |
| OS version | 10.0.26200 N/A Build 26200 |
| System type (x64 or ARM) | x64-based PC |
| Total physical memory (RAM) | 8,088 MB |
| IPv4 address | 192.168.1.5 |

**[Answer] B-Q2.** The `|` symbol in step 2 is called a **pipe**. Run `systeminfo` alone and compare. In your own words, what did `| findstr` do?

-- The pipe symbol (|) takes the detailed list generated by systeminfo and passes it straight into findstr. Instead of flooding my screen with a huge block of text, | findstr acts like a filter that only prints the specific lines I asked for.

---

## Part C: Build a Folder Structure

1. Go to your user folder and create the lab folders:

```
cd %USERPROFILE%
mkdir CC101-Lab
cd CC101-Lab
mkdir Notes Projects Screenshots
```

2. Create a text file about yourself (use your own details):

```
echo Name: Juan Dela Cruz > profile.txt
echo Section: BSCS 1-1 >> profile.txt
echo Favorite app: YouTube >> profile.txt
type profile.txt
```

**[Screenshot] Figure C1**

```
C:\Users\carln>cd %USERPROFILE%

C:\Users\carln>mkdir CC101-Lab

C:\Users\carln>cd CC101-Lab

C:\Users\carln\CC101-Lab>mkdir Notes Projects Screenshots

C:\Users\carln\CC101-Lab>echo Name: Carl Nathaniel B. Fundano > profile.txt

C:\Users\carln\CC101-Lab>echo Section: BSCS 1-1 >> profile.txt

C:\Users\carln\CC101-Lab>echo Favorite app: YouTube >> profile.txt

C:\Users\carln\CC101-Lab>type profile.txt
Name: Carl Nathaniel B. Fundano
Section: BSCS 1-1
Favorite app: YouTube
```

3. Run `tree /F` to display your folder structure.

**[Screenshot] Figure C2**

```
C:\Users\carln\CC101-Lab>tree /F
Folder PATH listing
Volume serial number is A4FB-2F08
C:.
│   profile.txt
│
├───Notes
├───Projects
└───Screenshots
```

4. Open File Explorer, go to `C:\Users\(your account)\CC101-Lab`, and open `profile.txt` in Notepad.

**[Screenshot] Figure C3** — File Explorer showing `CC101-Lab` (folders Notes, Projects, Screenshots and file profile.txt) beside Notepad displaying:

```
Name: Carl Nathaniel B. Fundano
Section: BSCS 1-1
Favorite app: YouTube
```

**[Answer] C-Q1.** What would happen if you used `>` instead of `>>` in the second echo line? Test it on a new file (test.txt) and explain.

-- Using > overwrites whatever is currently inside the file. When I tested it on test.txt, putting > on the second line wiped out my name completely and replaced the entire file with just the section info. Using >> is what saved it, since >> appends new text to the end without deleting what's already there.

---

## Part D: Copy, Rename, and Delete Files

```
copy profile.txt Notes\profile-copy.txt
cd Notes
ren profile-copy.txt about-me.txt
echo This file will be deleted > temp.txt
dir
del temp.txt
dir
cd ..
tree /F
```

**[Screenshot] Figure D1**

```
C:\Users\carln\CC101-Lab>copy profile.txt Notes\profile-copy.txt
        1 file(s) copied.

C:\Users\carln\CC101-Lab>cd Notes

C:\Users\carln\CC101-Lab\Notes>ren profile-copy.txt about-me.txt

C:\Users\carln\CC101-Lab\Notes>echo This file will be deleted > temp.txt

C:\Users\carln\CC101-Lab\Notes>dir
 Volume in drive C has no label.
 Volume Serial Number is A4FB-2F08

 Directory of C:\Users\carln\CC101-Lab\Notes

09/23/2026  07:08 PM    <DIR>          .
09/23/2026  06:55 PM    <DIR>          ..
09/23/2026  06:56 PM                78 about-me.txt
09/23/2026  07:08 PM                28 temp.txt
               2 File(s)            106 bytes
               2 Dir(s)  433,956,880,384 bytes free
```

**[Screenshot] Figure D2**

```
C:\Users\carln\CC101-Lab\Notes>del temp.txt

C:\Users\carln\CC101-Lab\Notes>dir
 Volume in drive C has no label.
 Volume Serial Number is A4FB-2F08

 Directory of C:\Users\carln\CC101-Lab\Notes

09/23/2026  07:10 PM    <DIR>          .
09/23/2026  06:55 PM    <DIR>          ..
09/23/2026  06:56 PM                78 about-me.txt
               1 File(s)             78 bytes
               2 Dir(s)  433,957,130,240 bytes free

C:\Users\carln\CC101-Lab\Notes>cd ..

C:\Users\carln\CC101-Lab>tree /F
Folder PATH listing
Volume serial number is A4FB-2F08
C:.
│   profile.txt
│
├───Notes
│       about-me.txt
│
├───Projects
└───Screenshots
```

**[Answer] D-Q1.** After `del temp.txt`, check your Recycle Bin. Is temp.txt there? What does this tell you about deleting files from the command line?

-- I checked my Recycle Bin after running del temp.txt, and the file wasn't there at all. This taught me that deleting files through the command line is permanent, it completely bypasses the Recycle Bin safety net, so I need to double-check my commands before running them.

---

## Part E: Explore PowerShell

Switch to the PowerShell window.

1. Go to your lab folder and list and read its files:

```powershell
cd $HOME\CC101-Lab
Get-ChildItem
Get-Content profile.txt
$PSVersionTable
```

**[Screenshot] Figure E1**

```
PS C:\Windows\system32> cd $HOME\CC101-Lab
PS C:\Users\carln\CC101-Lab> Get-ChildItem

    Directory: C:\Users\carln\CC101-Lab

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----         9/23/2026   7:10 PM                Notes
d-----         9/23/2026   6:54 PM                Projects
d-----         9/23/2026   6:54 PM                Screenshots
-a----         9/23/2026   6:56 PM             78 profile.txt

PS C:\Users\carln\CC101-Lab> Get-Content profile.txt
Name: Carl Nathaniel B. Fundano
Section: BSCS 1-1
Favorite app: YouTube
PS C:\Users\carln\CC101-Lab> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      5.1.26100.9444
PSEdition                      Desktop
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
BuildVersion                   10.0.26100.9444
CLRVersion                     4.0.30319.42000
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
```

2. Run `Get-Help Get-ChildItem`. If PowerShell asks whether to run Update-Help, type `N` and press Enter.

**[Screenshot] Figure E2** — output of `Get-Help Get-ChildItem` (NAME, SYNTAX, ALIASES `gci`, `ls`, `dir`, and a REMARKS note that Get-Help cannot find the Help files on this computer and is displaying only partial help).

3. Take the **last three digits of your student ID number** (for example, 2025-00347 → 347). Convert it with PowerShell:

```powershell
[Convert]::ToString(347, 2)
[Convert]::ToString(347, 8)
'{0:X}' -f 347
```

**[Screenshot] Figure E3**

```
PS C:\Users\carln\CC101-Lab> [Convert]::ToString(009, 2)
1001
PS C:\Users\carln\CC101-Lab> [Convert]::ToString(009, 8)
11
PS C:\Users\carln\CC101-Lab> '{0:X}' -f 009
9
```

**[Answer] E-Q1.** Write your number in decimal, binary, octal, and hexadecimal. Keep this; you will verify it by hand in Week 5.

- Decimal: 9 because my id has 009
- Binary: 1001
- Octal: 11
- Hexadecimal: 9

---

## Part F: Discover a New Command

1. In Command Prompt, type `help` to see a list of commands.
2. Choose **one** command that was **not** taught in this lesson and is safe to run (for example: `date /t`, `time /t`, `tasklist`, `vol`, or `color 0A`). Read its help with `command /?` (for example, `tasklist /?`), then run it.

**[Screenshot] Figure F1**

```
C:\Users\carln\CC101-Lab>vol /?
Displays the disk volume label and serial number, if they exist.

VOL [drive:]
```

**[Screenshot] Figure F2**

```
C:\Users\carln\CC101-Lab>vol
 Volume in drive C has no label.
 Volume Serial Number is A4FB-2F08
```

**[Answer] F-Q1.** What does your chosen command do, and when would it be useful?

-- I chose the vol command, which displays the disk volume label and serial number for my drive. This is super helpful if I ever need to verify my drive's serial number or volume name quickly without clicking around in File Explorer settings.

---

## Part G: Reflection

**[Answer]** Answer in 3 to 5 sentences each:

**G-Q1.** Which task in this activity was faster in the CLI than in the GUI? Which was easier in the GUI? Explain why.

-- Setting up my folder structure and writing text directly into files using mkdir and echo was way faster in the command line because I could do it all in a few typed lines. However, browsing around to check my files and opening them in Notepad felt much easier in the graphical user interface (GUI) since I could just click on things. The CLI is great for getting work done quickly without a mouse, while the GUI makes visual navigation effortless.

**G-Q2.** What error did you encounter (if any), what caused it, and how did you fix it?

-- I ran into a syntax error while typing commands in the terminal because I accidentally made a typo and missed the required quote marks. The shell couldn't process the input because the format didn't follow the exact rules it expects. I fixed it by carefully checking the error message, re-reading the required command format, and retyping it with the correct quotation marks and spacing.

**G-Q3.** Give one real-world job or situation in computing where knowing the command line would be important.

-- As a Computer Science student, learning the command line is super important for my future as a developer. I'll need it to run code, use Git for projects, install programming tools, and work with remote servers. Most coding tools and servers rely on the CLI rather than a graphical interface.

---

## Commands Learned Table

| Command | Shell | What it does |
|---|---|---|
| `echo` | Command Prompt / PowerShell | Prints text on the screen or saves text directly into a file. |
| `cd` | Command Prompt | Changes your current folder location in the terminal. |
| `mkdir` | Command Prompt | Creates a new folder inside your current directory |
| `del` | Command Prompt | Permanently deletes a file from your computer, skipping the Recycle Bin |
| `hostname` | Command Prompt | Shows the network name assigned to your computer. |
| `systeminfo` | Command Prompt | Pulls up detailed information about your system, like OS name, system type, and RAM. |

---

## Documentation and Submission

Submit one PDF that records what you did, what the computer showed, and what you learned. Someone reading it should be able to repeat your work.

**Required Contents (in this order)**

1. **Cover page:** activity title, your full name, student ID, section, date performed, and instructor's name.
2. **Introduction** (3 to 5 sentences): what the command line is and the purpose of this activity, in your own words.
3. **Procedure and results, Parts A to F:** for each part, a short heading, the commands you typed, the labeled screenshots, and your answers to that part's [Answer] questions.
4. **Commands learned table:** every command you used and what it does, in your own words.
5. **Reflection:** your answers to G-Q1 to G-Q3.

**Formatting Rules**

| Item | Requirement |
|---|---|
| File type | PDF (write in Word or Google Docs, then export as PDF) |
| File name | CC101_CLI-Lab_Lastname_Firstname.pdf |
| Font | Arial or Calibri, 11 pt; commands in Consolas or Courier New |
| Screenshots | Crop to the terminal window; text must be readable. Label each one below the image, e.g., "Figure B2. Filtered systeminfo output" |
| Personal details | Your own name, section, and student ID must appear in Figures A1, C1, and E3 |
| Total screenshots | 16 (A1–A2, B1–B3, C1–C3, D1–D2, E1–E3, F1–F2) |

**Sample Commands Learned Table**

| Command | Shell | What it does |
|---|---|---|
| `mkdir Notes` | Command Prompt | Creates a folder named Notes in the current folder |
| `type profile.txt` | Command Prompt | Displays the contents of profile.txt |

**Submission**

- Upload the PDF to the activity page in the course LMS before the deadline your instructor sets.
- Outputs must be your own work. Identical screenshots or answers will be treated as plagiarism under the class policy.
- Keep your CC101-Lab folder; later activities may build on it.

## Grading Rubric

The documentation is scored out of 100 points and counts under Laboratory: Project.

| Criterion | Points | Full marks | Partial marks | Low marks |
|---|---|---|---|---|
| Completeness of procedure | 30 | All 16 labeled, readable screenshots; every part A to F documented | 1 to 4 screenshots missing or unreadable | 5 or more screenshots missing |
| Accuracy of results | 20 | System-information table complete; commands and conversions correct and personalized | Minor errors or 1 to 2 missing values | Many errors, or results not the student's own |
| Answers to guide questions (A to F) | 20 | Correct, clear, in the student's own words | Mostly correct but brief or vague | Missing, incorrect, or copied |
| Reflection (G-Q1 to G-Q3) | 15 | Specific, honest, and linked to the activity | General statements with few specifics | Missing or off-topic |
| Organization and formatting | 15 | Follows the required order, naming, and formatting rules; commands learned table complete | Some rules not followed | Disorganized; wrong file type or name |
| **Total** | **100** | | | |
