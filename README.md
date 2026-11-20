<div align="center">🔐 NETWORKWALKS | WEEK 3 PRACTICAL ACTIVITIES
Cybersecurity and Ethical Hacking Training Programme
Batch B084

Project: Password Cracking and Recovery
</div>📋 Project details
Field	Details
Pentester name	Brian Simpande
Programme / Batch	B084 – NetworkWalks
Date	[Insert submission date]
Modules completed	W3-PM1 – Password Cracking with JTR
	W3-PM2 – Password Cracking with NetworkWalks Tools
Client / Target	NetworkWalks training lab
Permission	Yes – authorised educational lab exercise
Area covered	Password security and password recovery


⚠️ Disclaimer
All activities documented in this report were conducted for educational and research purposes under the NetworkWalks Cybersecurity and Ethical Hacking training programme. Testing was limited to the PDF file supplied for the authorised practical exercise.

Use password-recovery tools only on files that you own or have explicit permission to assess. Unauthorised access to protected information may constitute a criminal offence.

The author, instructor and NetworkWalks are not responsible for misuse of this information. All actions remain the sole responsibility of the individual.
📖 1. Introduction
This report documents practical activities undertaken during Week 3 of the NetworkWalks Cybersecurity and Ethical Hacking training programme.

The exercises focused on recovering the password of an encrypted PDF document using two different approaches:
- W3-PM1 – Password Cracking with JTR: Using John the Ripper (JTR) and its graphical interface, Johnny, on a Windows computer.
- W3-PM2 – Password Cracking with NetworkWalks Tools: Using the NetworkWalks Hash Calculator and Password Cracker through a web browser.
Both exercises used the training document titled My Locked PDF1.pdf.

The activities demonstrated how a password hash can be extracted from a protected PDF and submitted to a password-recovery tool. Each practical section records the procedure, observations and supporting screenshots.
🎯 2. Project objectives
The objectives of the practical exercises were to:
- Understand the role of password hashes in password recovery.
- Install and configure John the Ripper on Windows.
- Install and configure Johnny as the graphical interface for John the Ripper.
- Extract a password hash from an encrypted PDF.
- Save the extracted hash in a text file for use with John the Ripper.
- Use John the Ripper to attempt password recovery.
- Use the NetworkWalks Hash Calculator to extract a PDF hash.
- Use the NetworkWalks Password Cracker to attempt password recovery.
- Compare a locally installed tool with browser-based tools.
- Record the procedures and results using screenshots.
- Understand the importance of strong passwords and secure document handling.
🛠️ 3. Tools and technologies used
Tool / Technology	Purpose
Windows PC	Main operating environment for the JTR practical
John the Ripper (JTR)	Password-hash cracking and recovery tool
Johnny GUI	Graphical interface for John the Ripper
john.exe	John the Ripper executable configured in Johnny
Online PDF Hash Extractor	Extracting the PDF password hash for W3-PM1
Notepad	Saving the extracted hash in a text file
NetworkWalks Hash Calculator	Extracting the PDF hash for W3-PM2
NetworkWalks Password Cracker	Attempting password recovery using the extracted hash
Web browser	Accessing the browser-based tools
My Locked PDF1.pdf	Encrypted document supplied for the practical exercises


🔎 4. Activities performed
🔐 4.1 W3-PM1 – Password cracking with John the Ripper
The first practical involved using John the Ripper and Johnny GUI on a Windows computer to attempt to recover the password of the encrypted PDF supplied for the exercise.

The process involved installing the software, configuring Johnny, extracting the PDF hash, saving the hash in a text file and loading it into Johnny for a password-recovery attempt.
⚙️ Task 1: Download John the Ripper
🎯 Objective: Download John the Ripper for use on a Windows computer.

Procedure:
1. Visit the official John the Ripper website:
   https://www.openwall.com/john/
2. Alternatively, use the download repository provided in the lab instructions:
   https://distro.ibiblio.org/openwall/projects/john/1.9.0/
3. Download the appropriate package for the Windows computer.
4. Extract the downloaded archive.
5. Locate the run folder. This folder contains the John the Ripper executable used later in the practical.
📸 Evidence: Insert a screenshot showing the downloaded or extracted John the Ripper files.
<!-- Replace the filename below with the actual screenshot filename. -->
<p align="center">
  <img src="screenshots/W3-PM1-Task-1-JTR-Download.png" width="750" alt="John the Ripper download and extracted files">
</p>
<p align="center"><em>Figure 1: John the Ripper files on the Windows computer.</em></p>⚙️ Task 2: Download and configure Johnny GUI
🎯 Objective: Install Johnny and connect it to the John the Ripper executable.

Procedure:
1. Visit the Johnny project page:
   https://openwall.info/wiki/john/johnny
2. Download and install Johnny using the available installer.
3. Open Johnny after installation.
4. Open Settings.
5. Browse to the John the Ripper run folder.
6. Select the john.exe file.
7. Confirm the selection so that Johnny can use the John the Ripper program.
🔍 Observation: Johnny provides a graphical interface for working with John the Ripper. It must be pointed to the correct john.exe file for the two programs to work together.

📸 Evidence: Insert a screenshot showing Johnny's settings or the selected john.exe file.
<p align="center">
  <img src="screenshots/W3-PM1-Task-2-Johnny-Configuration.png" width="750" alt="Johnny configuration showing John the Ripper executable">
</p>
<p align="center"><em>Figure 2: Configuring Johnny to use john.exe.</em></p>⚙️ Task 3: Extract the PDF password hash
🎯 Objective: Extract the password hash from the encrypted PDF file.

Procedure:
1. Download My Locked PDF1.pdf from the training material.
2. Open the Online PDF Hash Extractor:
   https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php
3. Browse for the encrypted PDF file on the computer.
4. Upload the file using the tool's upload option.
5. Allow the tool to process the document.
6. Copy the hash displayed by the tool.
Important: The lab instructions specify that the extracted hash should begin with $pdf$. Check that the complete hash has been copied. If extra characters such as b' appear before the hash, remove them so that the saved value follows the expected format.

📸 Evidence: Insert a screenshot showing the PDF hash extraction result.
<p align="center">
  <img src="screenshots/W3-PM1-Task-3-PDF-Hash-Extraction.png" width="750" alt="Extracted PDF password hash">
</p>
<p align="center"><em>Figure 3: Password hash extracted from the protected PDF.</em></p>⚙️ Task 4: Save the hash in a text file
🎯 Objective: Prepare the extracted hash as an input file for John the Ripper.

Procedure:
1. Open Notepad.
2. Paste the copied PDF hash into the blank document.
3. Check that the hash is complete and begins with $pdf$.
4. Select File → Save As.
5. Save the file as:
   hash1.txt
6. Remember where the file is saved so that it can be located in Johnny.
🔍 Observation: The hash file provides John the Ripper with the password-hash data to be processed during the exercise.

📸 Evidence: Insert a screenshot showing the hash saved in Notepad.
<p align="center">
  <img src="screenshots/W3-PM1-Task-4-Hash-Text-File.png" width="750" alt="PDF hash saved in Notepad">
</p>
<p align="center"><em>Figure 4: Extracted PDF hash saved as hash1.txt.</em></p>⚙️ Task 5: Load the hash and start the attack in Johnny
🎯 Objective: Load the saved hash file into Johnny and initiate the password-recovery attempt.

Procedure:
1. Open Johnny.
2. Select Open Password File.
3. Browse to the location where hash1.txt was saved.
4. Select the file and open it.
5. Confirm that the hash has been loaded.
6. Select Start New Attack.
7. Allow the process to run and observe the results displayed by Johnny.
🔍 Analysis: John the Ripper attempts to identify a password that matches the supplied hash. The time required can vary depending on the password, the attack method and the processing capability of the computer.

📸 Evidence: Insert a screenshot showing the loaded hash file and the attack results.
<p align="center">
  <img src="screenshots/W3-PM1-Task-5-JTR-Attack.png" width="750" alt="Johnny password recovery process">
</p>
<p align="center"><em>Figure 5: Loading the hash file and starting the password-recovery attempt.</em></p>⚙️ Task 6: Verify the recovered password
🎯 Objective: Check whether the password identified during the exercise opens the original PDF.

Procedure:
1. Locate the password displayed by Johnny after the recovery attempt.
2. Open My Locked PDF1.pdf.
3. Enter the recovered password when prompted.
4. Check whether the document opens.
🔍 Analysis: If the document opens successfully, this confirms that the recovered password matches the password protecting the PDF.

Result: [Insert the actual result observed during the exercise.]

📸 Evidence: Insert a screenshot showing the PDF password prompt or the successfully opened document, as appropriate.
<p align="center">
  <img src="screenshots/W3-PM1-Task-6-PDF-Verification.png" width="750" alt="Verification of the recovered PDF password">
</p>
<p align="center"><em>Figure 6: Verification of the recovered password against the original PDF.</em></p>🌐 4.2 W3-PM2 – Password cracking with NetworkWalks tools
The second practical involved using two browser-based NetworkWalks tools to extract the password hash and attempt to recover the password of the same encrypted PDF document.

Unlike the first exercise, which required installing John the Ripper and configuring Johnny on Windows, this activity was carried out through a web browser.
⚙️ Task 1: Download the encrypted PDF
🎯 Objective: Obtain the PDF document supplied for the NetworkWalks practical.

Procedure:
1. Open the NetworkWalks project task page:
   https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/
2. Locate the supplied My Locked PDF1.pdf file.
3. Download the file to the computer.
📸 Evidence: Insert a screenshot showing the downloaded PDF, if available.
<p align="center">
  <img src="screenshots/W3-PM2-Task-1-PDF-Download.png" width="750" alt="Downloaded encrypted PDF">
</p>
<p align="center"><em>Figure 7: Encrypted PDF downloaded from the training material.</em></p>⚙️ Task 2: Open the NetworkWalks Hash Calculator
🎯 Objective: Access the tool used to extract the PDF password hash.

Procedure:
1. Open a web browser.
2. Visit the NetworkWalks Hash Calculator:
   https://networkwalks.com/hash-calculator/
3. Wait for the tool to load.
📸 Evidence: Insert a screenshot showing the Hash Calculator interface.
<p align="center">
  <img src="screenshots/W3-PM2-Task-2-Hash-Calculator.png" width="750" alt="NetworkWalks Hash Calculator">
</p>
<p align="center"><em>Figure 8: NetworkWalks Hash Calculator interface.</em></p>⚙️ Task 3: Extract the PDF hash
🎯 Objective: Generate the password hash from the encrypted PDF.

Procedure:
1. Use the upload option in the Hash Calculator.
2. Browse to the location of My Locked PDF1.pdf.
3. Select the PDF file.
4. Allow the tool to process it.
5. Locate the generated hash.
6. Confirm that the hash begins with $pdf$.
📸 Evidence: Insert a screenshot showing the extracted hash.
<p align="center">
  <img src="screenshots/W3-PM2-Task-3-Extracted-Hash.png" width="750" alt="PDF hash extracted using NetworkWalks">
</p>
<p align="center"><em>Figure 9: PDF hash generated by the NetworkWalks Hash Calculator.</em></p>⚙️ Task 4: Copy the complete hash
🎯 Objective: Prepare the extracted hash for submission to the Password Cracker.

Procedure:
1. Select the generated hash.
2. Copy the complete value.
3. Check that no characters have been left out.
4. Keep the copied hash ready for the next step.
Important: The lab instructions emphasise copying the complete hash, beginning with $pdf$.
⚙️ Task 5: Open the NetworkWalks Password Cracker
🎯 Objective: Access the tool used to attempt password recovery.

Procedure:
1. Open a new browser tab.
2. Visit:
   https://networkwalks.com/password-cracker/
3. Wait for the Password Cracker interface to load.
📸 Evidence: Insert a screenshot showing the Password Cracker interface.
<p align="center">
  <img src="screenshots/W3-PM2-Task-5-Password-Cracker.png" width="750" alt="NetworkWalks Password Cracker">
</p>
<p align="center"><em>Figure 10: NetworkWalks Password Cracker interface.</em></p>⚙️ Task 6: Submit the hash and start the attack
🎯 Objective: Use the extracted hash to initiate the password-recovery process.

Procedure:
1. Locate the hash input field.
2. Paste the complete PDF hash copied from the Hash Calculator.
3. Check that the hash has been entered correctly.
4. Start the password-cracking process using the tool's provided control.
5. Allow the tool to run.
🔍 Analysis: The Password Cracker attempts to identify a password matching the submitted hash. The time taken depends on the password and the tool's available processing resources.

📸 Evidence: Insert a screenshot showing the submitted hash and the process, where available.
<p align="center">
  <img src="screenshots/W3-PM2-Task-6-Cracking-Process.png" width="750" alt="NetworkWalks password-cracking process">
</p>
<p align="center"><em>Figure 11: Submitting the PDF hash to the NetworkWalks Password Cracker.</em></p>⚙️ Task 7: Review the password-cracking result
🎯 Objective: Establish whether the tool identified a matching password.

Procedure:
1. Allow the tool to complete its process.
2. Examine the result displayed on the screen.
3. If a password is returned, record it for the verification step.
4. If no password is returned, record that outcome accurately.
Result: [Insert the actual result observed during the exercise.]

📸 Evidence: Insert a screenshot showing the final result.
<p align="center">
  <img src="screenshots/W3-PM2-Task-7-Recovery-Result.png" width="750" alt="NetworkWalks password-cracking result">
</p>
<p align="center"><em>Figure 12: Result returned by the NetworkWalks Password Cracker.</em></p>⚙️ Task 8: Verify the recovered password
🎯 Objective: Confirm whether the password identified by the NetworkWalks tool opens the original PDF.

Procedure:
1. Open My Locked PDF1.pdf.
2. Enter the password returned by the Password Cracker.
3. Check whether the PDF opens successfully.
🔍 Analysis: Opening the original document provides a practical check that the recovered password matches the password protecting the file.

Result: [Insert the actual verification result.]

📸 Evidence: Insert a screenshot showing the password prompt or the successfully opened PDF, as appropriate.
<p align="center">
  <img src="screenshots/W3-PM2-Task-8-PDF-Verification.png" width="750" alt="Verification of the recovered password">
</p>
<p align="center"><em>Figure 13: Verification of the password against the original PDF.</em></p>⚠️ 5. Risk analysis and impact
The practical exercises highlighted several password-security considerations associated with encrypted PDF documents.
No.	Risk / Finding	Observation	Potential impact	Indicative risk
1	Weak PDF passwords	Password-recovery tools can test password guesses against an extracted hash.	Weak passwords may be easier to recover.	🟠 Medium
2	Password-hash exposure	The extracted hash can be used in password-recovery attempts.	An exposed hash may enable offline password attacks.	🟠 Medium
3	Predictable passwords	Common words and simple combinations are easier to guess.	Unauthorised access to protected documents.	🟠 Medium
4	Insecure document handling	Protected documents and their passwords may be shared without adequate safeguards.	Exposure of confidential information.	🟠 Medium
5	Third-party online processing	Browser-based services may require users to submit document data.	Potential confidentiality and privacy concerns.	🟠 Medium


📌 Risk assessment notes
The risks above are general security considerations demonstrated by the practical exercises. They should not be interpreted as confirmed vulnerabilities in the NetworkWalks tools or the supplied PDF document.

Extracting a password hash does not automatically mean that the original password can be recovered. Recovery depends on factors such as password strength, the attack method and available computing resources.

The exercises were conducted within the scope of the authorised training environment.
🛡️ 6. Recommendations
Based on the practical exercises, the following security measures are recommended:
1. 🔐 Use strong and unique passwords
   Protect sensitive PDF documents with long passwords that are difficult to guess.
2. 🚫 Avoid predictable passwords
   Do not use common words, personal information or simple number combinations.
3. 🔄 Change exposed passwords
   If a password may have been exposed, replace it and re-secure the document.
4. 📄 Protect confidential documents
   Apply appropriate encryption and share sensitive files only with authorised recipients.
5. 🌐 Be cautious with online tools
   Avoid uploading confidential documents to third-party services unless their privacy and data-handling practices have been assessed.
6. 🔍 Conduct authorised password-security assessments
   Organisations should periodically review password strength using approved testing procedures.
7. 🛡️ Adopt secure password-management practices
   Use password managers and appropriate organisational password policies.
8. ⚖️ Maintain authorised testing boundaries
   Password-cracking tools should only be used on files and systems that the tester owns or has permission to assess.
🎯 7. Conclusion
During Week 3 of the NetworkWalks Cybersecurity and Ethical Hacking training programme, I undertook practical exercises covering password recovery using John the Ripper and NetworkWalks browser-based tools.

In W3-PM1, I worked with John the Ripper and Johnny GUI on a Windows computer. The exercise involved installing and configuring the tools, extracting the password hash from an encrypted PDF, saving it in a text file and initiating a password-recovery attempt.

In W3-PM2, I used the NetworkWalks Hash Calculator and Password Cracker to extract the PDF hash and attempt password recovery through a web browser.

The two exercises provided practical exposure to different approaches to password recovery, highlighting the use of locally installed software and browser-based tools.

I also gained an understanding of the role of password hashes in security assessments and how weak or predictable passwords can increase the risk of unauthorised access to protected documents.

The exercises reinforced the importance of strong passwords, secure document handling and responsible use of password-cracking tools within an authorised testing environment.
📸 8. Evidence collected
Evidence directory: screenshots/

The screenshots supporting the practical exercises should be saved in the repository's screenshots/ directory. Replace the example image paths in this report with the exact filenames used in the repository.
No.	Evidence	Suggested filename
1	John the Ripper download / extracted files	W3-PM1-Task-1-JTR-Download.png
2	Johnny installation and configuration	W3-PM1-Task-2-Johnny-Configuration.png
3	PDF hash extraction	W3-PM1-Task-3-PDF-Hash-Extraction.png
4	Hash saved in Notepad	W3-PM1-Task-4-Hash-Text-File.png
5	Hash loaded and attack initiated in Johnny	W3-PM1-Task-5-JTR-Attack.png
6	PDF password verification	W3-PM1-Task-6-PDF-Verification.png
7	NetworkWalks Hash Calculator	W3-PM2-Task-2-Hash-Calculator.png
8	Extracted PDF hash	W3-PM2-Task-3-Extracted-Hash.png
9	NetworkWalks Password Cracker	W3-PM2-Task-5-Password-Cracker.png
10	Password-cracking process	W3-PM2-Task-6-Cracking-Process.png
11	Password-cracking result	W3-PM2-Task-7-Recovery-Result.png
12	PDF password verification	W3-PM2-Task-8-PDF-Verification.png


<div align="center">👨‍💻 Author
Brian Simpande

LinkedIn: Brian Simpande
📋 Programme details
Cybersecurity and Ethical Hacking – NetworkWalks

Week 03 | Batch B084

Project: Password Cracking and Recovery
</div>
