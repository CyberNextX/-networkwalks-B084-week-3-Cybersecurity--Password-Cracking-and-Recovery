<div align="center">

# 🔐 PENETRATION TESTING REPORT

### 🌐 FOOTPRINTING & NETWORK SCANNING PHASES

**🎯 W2-PM-FINAL** &nbsp; | &nbsp; **🛡️ CYBERSECURITY** &nbsp; | &nbsp; **🎓 NETWORKWALKS**

---------------------------------------------------------------------------------------------

</div>

<br/>

<table width="75%" align="center" border="1" cellpadding="12" cellspacing="0">
<tr>
<th width="40%" align="center">FIELD</th>
<th width="60%" align="center">DETAIL</th>
</tr>
<tr>
<td><strong>Pentester Name</strong><br/>(Cybersecurity Professional)</td>
<td><strong>Brian Simpande</strong></td>
</tr>
<tr bgcolor="#0969DA">
<td><strong><font color="#FFFFFF">Programme/Batch</font></strong></td>
<td><font color="#FFFFFF">B084 – NetworkWalks</font></td>
</tr>
<tr bgcolor="#0969DA">
<td><strong><font color="#FFFFFF">Date</font></strong></td>
<td><font color="#FFFFFF">20 November 2026</font></td>
</tr>
<tr bgcolor="#0969DA">
<td><strong><font color="#FFFFFF">Modules completed</font></strong></td>
<td><font color="#FFFFFF">W3-PM1 – Password Cracking with JTR)<br/>W3-PM2 – Password Cracking with NetworkWalks Tools)</font></td>
</tr>
<tr bgcolor="#0969DA">
<td><strong><font color="#FFFFFF">Client/Target</font></strong></td>
<td><font color="#FFFFFF">1. NetworkWalks<br/>2. NetworkWalks training lab</font></td>
</tr>
<tr bgcolor="#0969DA">
<td><strong><font color="#FFFFFF">Permission secured from client?</font></strong></td>
<td><font color="#FFFFFF">Yes</font></td>
</tr>
<tr bgcolor="#0969DA">
<td><strong><font color="#FFFFFF">Area covered</font></strong></td>
<td><font color="#FFFFFF"><strong>Phase 3:</strong> Password security and password recovery<br/><strong></font></td>
</tr>
</table>

</div>
---
<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/%20Brian%20BSC-C00000?style=flat-square" />
</p>


**NETWORKWALKS | PRACTICAL ACTIVITIES**

---

## ⚠️ Disclaimer

All activities documented in this report were conducted for educational and research purposes under the NetworkWalks Cybersecurity and Ethical Hacking training programme. Testing was limited to the PDF file supplied for the authorised practical exercise.
Use password-recovery tools only on files that you own or have explicit permission to assess. 
Unauthorised access to protected information may constitute a criminal offence.
The author, instructor and NetworkWalks are not responsible for misuse of this information. All actions remain the sole responsibility of the individual.
---

## 📖 1. Introduction

This report documents practical activities undertaken during Week 3 of the NetworkWalks Cybersecurity and Ethical Hacking training programme.

The exercises covered two main areas:

The exercises focused on recovering the password of an encrypted PDF document using two different approaches:
W3-PM1 – Password Cracking with JTR: Using John the Ripper (JTR) and its graphical interface, Johnny, on a Windows computer.
W3-PM2 – Password Cracking with NetworkWalks Tools: Using the NetworkWalks Hash Calculator and Password Cracker through a web browser.
Both exercises used the training document titled `My Locked PDF1.pdf`.

The activities demonstrated how a password hash can be extracted from a protected PDF and submitted to a password-recovery tool. Each practical section records the procedure, observations and supporting screenshots.

---

## 🎯 2. Project Objectives

The main objectives of these practical exercises were to:

- ✅ Install and configure John the Ripper on Windows.
- ✅Install and configure Johnny as the graphical interface for John the Ripper.
- ✅Extract a password hash from an encrypted PDF.
- ✅Save the extracted hash in a text file for use with John the Ripper.
- ✅Use John the Ripper to attempt password recovery.
- ✅Use the NetworkWalks Hash Calculator to extract a PDF hash.
- ✅Use the NetworkWalks Password Cracker to attempt password recovery.
- ✅Compare a locally installed tool with browser-based tools.
- ✅Record the procedures and results using screenshots.
- ✅Understand the importance of strong passwords and secure document handling.
- --

## 🛠️ 3. Tools and Technologies Used

| Tool | Purpose |
|---|---|
| 🖥️ Windows PC | Main operating environment for the password-cracking practicals |
| 🔐 John the Ripper (JTR) | Password-hash cracking and recovery |
| 🪟 Johnny GUI | Graphical interface for managing John the Ripper attacks |
| ⚙️ `john.exe` | John the Ripper executable configured in Johnny |
| 🌐 Online PDF Hash Extractor | Extracting password hashes from the encrypted PDF |
| 📝 Notepad | Creating and saving the extracted hash in a text file |
| 🔢 NetworkWalks Hash Calculator | Generating the PDF password hash for W3-PM2 |
| 🔓 NetworkWalks Password Cracker | Attempting to recover the PDF password using the extracted hash |
| 🌍 Web Browser | Accessing online hash extraction and password-cracking tools |
| 📄 `My Locked PDF1.pdf` | Encrypted PDF file supplied for the practical exercises |

---

# 🔎 4. Activities Performed

🔐 4. Practical activities
🔐 4.1 W3-PM1 – Password cracking with John the Ripper
The first practical used John the Ripper and Johnny GUI on a Windows computer to attempt to recover the password of the encrypted PDF supplied for the exercise.
⚙️ Task 1: Download John the Ripper
🎯 Objective: Download John the Ripper for use on a Windows computer.

📝 Procedure:
1. Visit the official John the Ripper website:
   https://www.openwall.com/john/
2. Alternatively, use the download repository provided in the lab instructions:
   https://distro.ibiblio.org/openwall/projects/john/1.9.0/
3. Download the appropriate package for Windows.
4. Extract the downloaded archive.
5. Locate the run folder. It contains the John the Ripper executable required later in the practical.
📸 Evidence:
<img width="3772" height="1750" alt="Downloading John the Ripper" src="https://github.com/user-attachments/assets/eaca440b-156f-44f5-bd5f-316132f4a4e3" />

⚙️ STEEP 1: Download and configure Johnny GUI

🎯 Objective: Install Johnny and connect it to the John the Ripper executable.

📝 Procedure:
1. Visit the Johnny project page:
   https://openwall.info/wiki/john/johnny
2. Download and install Johnny using the available installer.
3. Open Johnny after installation.
4. Open Settings.
5. Browse to the John the Ripper run folder.
6. Select the john.exe file.
7. Confirm the selection so that Johnny can use John the Ripper.
🔍 Observation: Johnny provides a graphical interface for working with John the Ripper. It must be pointed to the correct john.exe file for the two programs to work together.

⚙️ Task 2: Download and configure Johnny GUI
🎯 Objective: Install Johnny and connect it to the John the Ripper executable.

📝 Procedure:
1. Visit the Johnny project page:
   https://openwall.info/wiki/john/johnny
2. Download and install Johnny using the available installer.
3. Open Johnny after installation.
4. Open Settings.
5. Browse to the John the Ripper run folder.
6. Select the john.exe file.
7. Confirm the selection so that Johnny can use John the Ripper.
🔍 Observation: Johnny provides a graphical interface for working with John the Ripper. It must be pointed to the correct john.exe file for the two programs to work together.

⚙️ Task 3: Extract the PDF password hash
🎯 Objective: Extract the password hash from the encrypted PDF file.

📝 Procedure:
1. Download My Locked PDF1.pdf from the training material.
2. Open the Online PDF Hash Extractor:
   https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php
3. Browse for the encrypted PDF file on the computer.
4. Upload the file using the tool's upload option.
5. Allow the tool to process the document.
6. Copy the hash displayed by the tool.
⚠️ Important: The lab instructions specify that the extracted hash should begin with $pdf$. Check that the complete hash has been copied. If extra characters such as b' appear before the hash, remove them so that the saved value follows the expected format.

⚙️ Task 4: Save the hash in a text file
🎯 Objective: Prepare the extracted hash as an input file for John the Ripper.

📝 Procedure:
1. Open Notepad.
2. Paste the copied PDF hash into the blank document.
3. Check that the hash is complete and begins with $pdf$.
4. Select File → Save As.
5. Save the file as hash1.txt.
6. Remember where the file is saved so that it can be located in Johnny.
🔍 Observation: The hash file provides John the Ripper with the password-hash data to be processed during the exercise.

⚙️ Task 5: Load the hash and start the attack in Johnny
🎯 Objective: Load the saved hash file into Johnny and initiate the password-recovery attempt.

📝 Procedure:
1. Open Johnny.
2. Select Open Password File.
3. Browse to the location where hash1.txt was saved.
4. Select the file and open it.
5. Confirm that the hash has been loaded.
6. Select Start New Attack.
7. Allow the process to run and observe the results displayed by Johnny.
🔍 Analysis: John the Ripper attempts to identify a password that matches the supplied hash. The time required can vary depending on the password, the attack method and the processing capability of the computer.

⚙️ Task 6: Verify the recovered password
🎯 Objective: Check whether the password identified during the exercise opens the original PDF.

📝 Procedure:
1. Locate the password displayed by Johnny after the recovery attempt, if one is returned.
2. Open My Locked PDF1.pdf.
3. Enter the recovered password when prompted.
4. Check whether the document opens.
🔍 Analysis: If the document opens successfully, this confirms that the recovered password matches the password protecting the PDF.

🌐 4.2 W3-PM2 – Password cracking with NetworkWalks tools
The second practical used two browser-based NetworkWalks tools to extract the password hash and attempt to recover the password of the same encrypted PDF document.

Unlike the first exercise, which required installing John the Ripper and configuring Johnny on Windows, this activity was carried out through a web browser.
⚙️ Task 1: Download the encrypted PDF
🎯 Objective: Obtain the PDF document supplied for the NetworkWalks practical.

📝 Procedure:
1. Open the NetworkWalks project task page:
   https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/
2. Locate the supplied My Locked PDF1.pdf file.
3. Download the file to the computer.
📸 Evidence: Insert a screenshot showing the downloaded PDF, if available.
<p align="center">
  <img src="screenshots/W3-PM2-Task-1-PDF-Download.png" width="750" alt="Downloaded encrypted PDF">
</p><p align="center"><em>Figure 7: Encrypted PDF downloaded from the training material.</em></p>⚙️ Task 2: Open the NetworkWalks Hash Calculator
🎯 Objective: Access the tool used to extract the PDF password hash.

📝 Procedure:
1. Open a web browser.
2. Visit the NetworkWalks Hash Calculator:
   https://networkwalks.com/hash-calculator/
3. Wait for the tool to load.
📸 Evidence:
<p align="center">
  <img src="<img width="3705" height="1915" alt="image" src="https://github.com/user-attachments/assets/b99df1a9-2f5c-47e7-aec6-171aba4707ee" />
>
</p><p align="center"><em>Figure 8: NetworkWalks Hash Calculator interface.</em></p>⚙️ Task 3: Extract the PDF hash
🎯 Objective: Generate the password hash from the encrypted PDF.

📝 Procedure:
1. Use the upload option in the Hash Calculator.
2. Browse to the location of My Locked PDF1.pdf.
3. Select the PDF file.
4. Allow the tool to process it.
5. Locate the generated hash.
6. Confirm that the hash begins with $pdf$.
📸 Evidence:
<p align="center">
  <img src="<img width="3610" height="1735" alt="image" src="https://github.com/user-attachments/assets/5138b9b5-92fb-445a-a440-e1b636a241f0" />
">
</p><p align="center"><em>Figure 9: PDF hash generated by the NetworkWalks Hash Calculator.</em></p>⚙️ Task 4: Copy the complete hash
🎯 Objective: Prepare the extracted hash for submission to the Password Cracker.

📝 Procedure:
1. Select the generated hash.
2. Copy the complete value.
3. Check that no characters have been left out.
4. Keep the copied hash ready for the next step.
⚠️ Important: The lab instructions emphasise copying the complete hash, beginning with $pdf$.
⚙️ Task 5: Open the NetworkWalks Password Cracker
🎯 Objective: Access the tool used to attempt password recovery.

📝 Procedure:
1. Open a new browser tab.
2. Visit:
   https://networkwalks.com/password-cracker/
3. Wait for the Password Cracker interface to load.
📸 Evidence:
<p align="center">
  <img src="<img width="3655" height="1652" alt="image" src="https://github.com/user-attachments/assets/b9c5f444-8fbe-42dd-bdd8-aa504acde16a" />
">
</p><p align="center"><em>Figure 10: NetworkWalks Password Cracker interface.</em></p>⚙️ Task 6: Submit the hash and start the attack
🎯 Objective: Use the extracted hash to initiate the password-recovery process.

📝 Procedure:
1. Locate the hash input field.
2. Paste the complete PDF hash copied from the Hash Calculator.
3. Check that the hash has been entered correctly.
4. Start the password-cracking process using the tool's provided control.
5. Allow the tool to run.
🔍 Analysis: The Password Cracker attempts to identify a password matching the submitted hash. The time taken depends on the password and the tool's available processing resources.

📸 Evidence:
<p align="center">
  <img src="screenshots/W3-PM2-Task-6-Cracking-Process.png" width="750" alt="NetworkWalks password-cracking process">
</p><p align="center"><em>Figure 11: Submitting the PDF hash to the NetworkWalks Password Cracker.</em></p>⚙️ Task 7: Review the password-cracking result
🎯 Objective: Establish whether the tool identified a matching password.

📝 Procedure:
1. Allow the tool to complete its process.
2. Examine the result displayed on the screen.
3. If a password is returned, record it for the verification step.
4. If no password is returned, record that outcome accurately.
📌 Result: <img <img width="3795" height="1670" alt="image" src="https://github.com/user-attachments/assets/34abc425-84b6-4c11-9fbb-2ffc4b694740" />
 />

📸 Evidence:
<p align="center">
  <img src="screenshots/W3-PM2-Task-7-Recovery-Result.png" width="750" alt="NetworkWalks password-cracking result">
</p><p align="center"><em>Figure 12: Result returned by the NetworkWalks Password Cracker.</em></p>

⚙️ Task 8: Verify the recovered password
🎯 Objective: Confirm whether the password identified by the NetworkWalks tool opens the original PDF.

📝 Procedure:
1. Open My Locked PDF1.pdf.
4. Enter the password returned by the Password Cracker, if one was recovered.
5. Check whether the PDF opens successfully.
🔍 Analysis: Opening the original document provides a practical check that the recovered password matches the password protecting the file.
NOTE: Reapeat for: My Locked PDF2.pdf and My Locked PDF3.pdf.

📸 Evidence: 

Results 01
<img width="2062" height="1645" alt="pdf01" src="https://github.com/user-attachments/assets/651c37ce-ded3-4854-8214-e23c6077691e" />

Results 02
<img width="2045" height="1485" alt="pdf02" src="https://github.com/user-attachments/assets/07c20ad4-dad7-40e8-ab7b-04b881f5484a" />

Results 03
<img width="2085" height="1570" alt="pdf03" src="https://github.com/user-attachments/assets/54768534-6986-4ec6-ba3e-80448ea5dfe6" />

## ⚠️ 5. Risk Analysis and Impact

The practical exercises highlighted several password-security considerations associated with encrypted PDF documents.

| No. | Risk / Finding | Observation | Potential Impact | Indicative Risk |
|:---:|---|---|---|:---:|
| 1 | Weak PDF passwords | Password-recovery tools can test password guesses against an extracted hash. | Weak passwords may be easier to recover. | 🟠 Medium |
| 2 | Password-hash exposure | The extracted hash can be used in password-recovery attempts. | An exposed hash may enable offline password attacks. | 🟠 Medium |
| 3 | Predictable passwords | Common words and simple combinations are easier to guess. | Unauthorised access to protected documents. | 🟠 Medium |
| 4 | Insecure document handling | Protected documents and their passwords may be shared without adequate safeguards. | Exposure of confidential information. | 🟠 Medium |
| 5 | Third-party online processing | Browser-based services may require users to submit document data. | Potential confidentiality and privacy concerns. | 🟠 Medium |

### 📌 Risk Assessment Notes

- The risks above are general security considerations demonstrated by the practical exercises. They should not be interpreted as confirmed vulnerabilities in the NetworkWalks tools or the supplied PDF document.
- Extracting a password hash does not automatically mean that the original password can be recovered. Recovery depends on factors such as password strength, the attack method and available computing resources.
- 
## 🛡️ 6. Recommendations

Based on the practical exercises, the following security measures are recommended:

| Recommendation | Security Measure |
|:---|:---|
| 🔐 **Use strong and unique passwords** | Protect sensitive PDF documents with long passwords that are difficult to guess. |
| 🚫 **Avoid predictable passwords** | Do not use common words, personal information or simple number combinations. |
| 🔄 **Change exposed passwords** | If a password may have been exposed, replace it and re-secure the document. |
| 📄 **Protect confidential documents** | Apply appropriate encryption and share sensitive files only with authorised recipients. |
| 🌐 **Be cautious with online tools** | Avoid uploading confidential documents to third-party services unless their privacy and data-handling practices have been assessed. |
| 🔍 **Conduct authorised password-security assessments** | Organisations should periodically review password strength using approved testing procedures. |
| 🛡️ **Adopt secure password-management practices** | Use password managers and appropriate organisational password policies. |
| ⚖️ **Maintain authorised testing boundaries** | Password-cracking tools should only be used on files and systems that the tester owns or has permission to assess. |



---

## 🎯 7. Conclusion

During Week 3 of the NetworkWalks Cybersecurity and Ethical Hacking training programme, I successfully completed practical exercises on password recovery using John the Ripper and NetworkWalks browser-based tools.

In **W3-PM1**, I used John the Ripper and Johnny GUI on a Windows computer. The exercise involved installing and configuring the tools, extracting the password hash from an encrypted PDF, saving it in a text file and initiating a password-recovery attempt. The password was successfully recovered and verified by opening the protected PDF document.

In **W3-PM2**, I used the NetworkWalks Hash Calculator and Password Cracker to extract the PDF hash and perform password recovery through a web browser. The password was also successfully recovered and verified by opening the encrypted PDF.

The two exercises provided practical experience with different password-recovery approaches, including locally installed software and browser-based tools. They also strengthened my understanding of password hashes and how weak or predictable passwords can increase the risk of unauthorised access to protected documents.

Overall, the practical sessions reinforced the importance of using strong passwords, protecting sensitive documents, handling password hashes securely and ensuring that password-cracking tools are used responsibly within an authorised testing environment.

---

---

## 👨‍💻 Author

**Brian Simpande**

🔗 **LinkedIn:** [Brian Simpande](https://www.linkedin.com/in/brian-simpande/)

---

## 📋 Project Details

| **Field** | **Details** |
|---|---|
| 📌 **Programme** | Cybersecurity and Ethical Hacking – NetworkWalks |
| 📅 **Week** | 02 |
| 🔐 **Project** | Footprinting and Network Scanning |
| 💻 **Platform** | GitHub |
| 🎓 **Batch** | B084 – NetworkWalks |

---

</div>
