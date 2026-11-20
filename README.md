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

📸 Evidence:

<img width="1550" height="692" alt="Johnny Configuration" src="https://github.com/user-attachments/assets/ac0334de-1758-4d68-bc73-e416bce247bf" />

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

📸 Evidence:

<img width="3840" height="2027" alt="File Attack Password" src="https://github.com/user-attachments/assets/9656c324-22e5-403e-a73a-073ea09a8329" />

🎯 Objective: Prepare the extracted hash as an input file for John the Ripper.

📝 Procedure:
1. Open Notepad.
2. Paste the copied PDF hash into the blank document.
3. Check that the hash is complete and begins with $pdf$.
4. Select File → Save As.
5. Save the file as hash1.txt.
6. Remember where the file is saved so that it can be located in Johnny.
🔍 Observation: The hash file provides John the Ripper with the password-hash data to be processed during the exercise.

📸 Evidence:
<p align="center">
  <img src="screenshots/W3-PM1-Task-4-Hash-Text-File.png" width="750" alt="PDF hash saved in Notepad">
</p><p align="center"><em>Figure 4: Extracted PDF hash saved as hash1.txt.</em></p>⚙️ Task 5: Load the hash and start the attack in Johnny
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

📸 Evidence:
<p align="center">
  <img src="<img width="3840" height="2027" alt="File Attack Password" src="https://github.com/user-attachments/assets/98ea80a2-505c-4aac-b0d2-3f6ba8deb47b" />
screenshots/W3-PM1-Task-5-JTR-Attack.png" width="750" alt="Johnny password recovery process">
</p><p align="center"><em>Figure 5: Loading the hash file and starting the password-recovery attempt.</em></p>⚙️ Task 6: Verify the recovered password
🎯 Objective: Check whether the password identified during the exercise opens the original PDF.

📝 Procedure:
1. Locate the password displayed by Johnny after the recovery attempt, if one is returned.
2. Open My Locked PDF1.pdf.
3. Enter the recovered password when prompted.
4. Check whether the document opens.
🔍 Analysis: If the document opens successfully, this confirms that the recovered password matches the password protecting the PDF.

📌 Result: [Insert the actual result observed during the exercise.]

📸 Evidence: Insert a screenshot showing the PDF password prompt or the successfully opened document, as appropriate.
<p align="center">
  <img src="screenshots/W3-PM1-Task-6-PDF-Verification.png" width="750" alt="Verification of the recovered PDF password">
</p><p align="center"><em>Figure 6: Verification of the recovered password against the original PDF.</em></p>🌐 4.2 W3-PM2 – Password cracking with NetworkWalks tools
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
  <img src="screenshots/W3-PM2-Task-2-Hash-Calculator.png" width="750" alt="NetworkWalks Hash Calculator">
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
  <img src="screenshots/W3-PM2-Task-3-Extracted-Hash.png" width="750" alt="PDF hash extracted using NetworkWalks">
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
  <img src="screenshots/W3-PM2-Task-5-Password-Cracker.png" width="750" alt="NetworkWalks Password Cracker">
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
📌 Result: [Insert the actual result observed during the exercise.]

📸 Evidence:
<p align="center">
  <img src="screenshots/W3-PM2-Task-7-Recovery-Result.png" width="750" alt="NetworkWalks password-cracking result">
</p><p align="center"><em>Figure 12: Result returned by the NetworkWalks Password Cracker.</em></p>⚙️ Task 8: Verify the recovered password
🎯 Objective: Confirm whether the password identified by the NetworkWalks tool opens the original PDF.

📝 Procedure:
1. Open My Locked PDF1.pdf.
2. Enter the password returned by the Password Cracker, if one was recovered.
3. Check whether the PDF opens successfully.
🔍 Analysis: Opening the original document provides a practical check that the recovered password matches the password protecting the file.

📌 Result: [Insert the actual verification result.]

📸 Evidence: Insert a screenshot showing the password prompt or the successfully opened PDF, as appropriate.
<p align="center">
  <img src="screenshots/W3-PM2-Task-8-PDF-Verification.png" width="750" alt="Verification of the recovered password">
</p><p align="center"><em>Figure 13: Verification of the password against the original PDF.</em></p>
---

# ⚠️ 5. Risk Analysis and Impact

Based on the observations collected during footprinting and network discovery, the following potential security considerations were identified.

| No. | Risk / Finding | Evidence / Observation | Potential Impact | Risk Level |
|---|---|---|---|---|
| 1 | Website technology information exposed | WhatWeb identified WordPress and a plugin | May assist further technology fingerprinting and software research | 🟠 Medium |
| 2 | Domain IP address identifiable | Nslookup resolved the domain to an IPv4 address | Provides information about the hosting infrastructure | 🟢 Low |
| 3 | HTTP technical information exposed | Curl returned response headers and REST API references | May assist further enumeration | 🟢 Low |
| 4 | WAF technology identifiable | Wafw00f detected ModSecurity | Reveals information about the web security architecture | 🟢 Low |
| 5 | DNS infrastructure information exposed | DNSRecon identified DNS, mail and service records | May help build a broader infrastructure profile | 🟠 Medium |
| 6 | Multiple active local hosts identified | Nmap discovered three active hosts | Unrecognised devices may require investigation | 🟠 Medium |

**Risk level key:**

- 🟢 **Low:** Limited observed exposure.
- 🟠 **Medium:** Warrants further review.
- 🔴 **High/Critical:** Requires urgent assessment where confirmed.

### 📌 Risk Assessment Notes

The risk levels above are indicative assessments of potential exposure, not confirmed vulnerability ratings.

The practical exercises primarily involved information gathering and host discovery. No exploitation or vulnerability validation was performed as part of these activities.

The presence of information such as a software version, IP address, DNS record or WAF technology does not by itself mean that a system is vulnerable. Further authorised security testing would be required to establish whether an actual vulnerability exists.

---

# 🛡️ 6. Recommendations

Based on the observations from the practical exercises, the following security improvements are recommended.

**1. 🔍 Review publicly exposed technology information**

Organisations should regularly review the information publicly visible about their web technologies, content management systems and plugins.

**2. 🔄 Keep software updated**

Content management systems, plugins and other web technologies should be updated regularly and checked against relevant security advisories.

**3. 🔐 Review HTTP response headers**

HTTP response headers should be assessed to determine whether unnecessary technical information is exposed and whether appropriate security policies are configured.

**4. 🌐 Review DNS records regularly**

DNS records should be checked periodically to ensure that only required information and services are publicly exposed.

**5. 🛡️ Review DNSSEC configuration**

Where appropriate, organisations should assess the implementation of DNSSEC to support DNS response authenticity.

**6. 🔥 Properly configure and monitor the WAF**

ModSecurity rules should be reviewed, maintained and monitored to ensure that the web application firewall is appropriately configured.

**7. 📡 Perform regular internal network discovery**

Organisations should periodically scan their own networks to identify active devices and maintain an accurate network inventory.

**8. 💻 Investigate unknown devices**

Unexpected devices discovered during network scanning should be investigated and verified.

**9. 🗺️ Maintain network documentation**

Network topology and device information should be documented and updated regularly.

**10. ⚖️ Conduct security testing with authorisation**

Reconnaissance and scanning should only be performed against systems and networks where appropriate authorisation has been obtained.

---

# 🎯 7. Conclusion

During Week 2 of the NetworkWalks Cybersecurity and Ethical Hacking training programme, I completed practical activities covering footprinting, reconnaissance and network discovery.

In the footprinting activity, I used six Kali Linux tools to collect information about the target domain. WHOIS provided domain registration information, WhatWeb identified website technologies, Nslookup resolved the domain name, Curl inspected HTTP response headers, Wafw00f detected a web application firewall, and DNSRecon provided additional DNS information.

In the network discovery activity, I used Windows `ipconfig` to examine the local network configuration and Nmap to identify active hosts. The scan examined 256 IP addresses and identified three active hosts.

The exercises demonstrated that information gathering is an important part of cybersecurity assessment. Before conducting deeper security testing, a practitioner can learn a considerable amount about a target environment by analysing publicly available information and network responses.

I also learned the importance of documenting technical findings accurately, interpreting observations carefully and distinguishing potential risks from confirmed vulnerabilities.

Finally, the exercises reinforced the importance of conducting reconnaissance and network scanning within an authorised scope.

---

## 📸 8. EVIDENCE COLLECTED

📂 **Evidence directory:** `screenshots/`

Screenshots and supporting evidence collected during the practical assessment are organised in the repository's `screenshots/` directory.

| **No.** | **Evidence** | **Filename** |
|:---:|---|---|

| **1** | 🔎 WHOIS lookup | <img width="2965" height="1510" alt="Task 1-WHOs Results" src="https://github.com/user-attachments/assets/fb23881c-8614-4a6b-8a8c-17467ee31340" />
 |

| **2** | 🛠️ WhatWeb results | <img width="2965" height="1495" alt="Task 2-WATWEB Results" src="https://github.com/user-attachments/assets/7618d98f-7ee3-4dda-be3f-05daccae3295" />
 |

| **3** | 🌐 Nslookup results | <img width="2972" height="1535" alt="Task 3- nslookup Results" src="https://github.com/user-attachments/assets/d1b9f51b-564b-4a0b-b194-7ce1d45f0eaa" />
 |

| **4** | 📡 Curl response headers | <img width="2965" height="1492" alt="Task 4- curl Results" src="https://github.com/user-attachments/assets/0cc05843-23f3-4cce-8c52-9c470b1780c6" />

 |

| **5** | 🛡️ Wafw00f results | <img width="2962" height="1515" alt="Task 5-WafW00f Results" src="https://github.com/user-attachments/assets/ddfa1641-44ba-46b7-b6f2-f6d590eb60fb" />
 |

| **6** | 🗂️ DNSRecon results |<img width="2972" height="1532" alt="Task 6-dnsrecon Results" src="https://github.com/user-attachments/assets/57c2fc26-778e-44ad-963b-e60409355c4a" />
 |

| **7** | 💻 Windows network configuration | <img width="3385" height="1800" alt="Task 02-Find local IP" src="https://github.com/user-attachments/assets/566c3ad7-da80-476e-ac94-527296f7f2e3" />
 |

| **8** | 🔍 Nmap host discovery | <img width="3375" height="1995" alt="Network discovery" src="https://github.com/user-attachments/assets/5d6ed419-04ef-4411-9816-2ce35ed53be0" />
 |

| **9** | 🖥️ Zenmap topology | <img width="3480" height="1980" alt="Task 07 Typology" src="https://github.com/user-attachments/assets/6bfb676f-7ced-4f97-a478-d1feb2f9508d" />
 |

| **10** | 📄 Exported network topology | [Task 07 Typology.pdf](https://github.com/user-attachments/files/34872621/Task.07.Typology.pdf)
 |
</div>

<div align="center">

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
