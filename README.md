# Networkwalks Cybersecurity Internship – Practical Labs

## PDF Password Hash Extraction and Cracking

### Overview
As part of my Networkwalks Cybersecurity Internship, I completed a practical password recovery exercise involving three password-protected PDF test files. The exercise introduced me to password hash extraction, dictionary attacks, and password recovery using cybersecurity tools.

### Tools Used
- **Online PDF Hash Calculator / Hash Extractor:** Provided in the Networkwalks exercise instructions to extract password hashes from PDF files.
- **Kali Linux:** Operating system used to perform the practical exercise.
- **John the Ripper:** Password auditing and recovery tool used to test extracted password hashes.
- **RockYou Wordlist:** A commonly used password dictionary for dictionary-based password testing.
- **Terminal:** Used to execute commands and manage hash files.

### Methodology

**1. PDF Hash Extraction**

- Used the online PDF hash extraction tool provided in the Networkwalks instructions.
- Uploaded each of the three password-protected PDF test files.
- Extracted the corresponding password hashes.
- Saved each extracted hash into a separate text file:
  - `hash1.txt`
  - `hash2.txt`
  - `hash3.txt`

**2. Preparing the Kali Linux Environment**

- Used Kali Linux within VirtualBox.
- Verified that John the Ripper was installed and supported PDF hash formats.
- Prepared the RockYou wordlist for dictionary-based password testing.

**3. Password Cracking with John the Ripper**

Used John the Ripper with the RockYou wordlist to test the extracted PDF hashes.

Example command:

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt ~/hash2.txt
```

Also practised:
- Checking cracking progress.
- Resuming interrupted sessions using `john --restore`.
- Monitoring completed cracking sessions.

**4. Password Verification**

Used the following command to display recovered passwords:

```bash
john --show --format=PDF ~/hash2.txt
```

Repeated the process for all three PDF hash files.

### Results

Successfully recovered the passwords for all three provided PDF test files using John the Ripper and the RockYou wordlist.

The exercise demonstrated how extracted password hashes can be tested against known password dictionaries to identify matching passwords.

Objective

To gain practical experience in extracting password hashes from password-protected PDF documents and recovering passwords using password-cracking tools.

Tools Used
- Windows laptop
- Networkwalks Hash Calculator
- Networkwalks Password Cracker
- Kali Linux
- John the Ripper
- RockYou wordlist

 Networkwalks Hash Calculator and Password Cracker (Windows)
1. Accessed the Networkwalks Hash Calculator provided for the practical task.
2. Uploaded the supplied My Locked PDF1.pdf file.
3. Used the Hash Calculator to extract the PDF password hash.
4. Copied and saved the extracted hash for password-cracking analysis.
5. Used the Networkwalks Password Cracker tool to attempt password recovery.
6. Retrieved the recovered password and used it to unlock the protected PDF.

### Key Skills and Learning Outcomes

- PDF password hash extraction.
- Understanding password hashes and PDF hash formats.
- Using John the Ripper for password auditing.
- Performing dictionary attacks.
- Working with password wordlists.
- Managing and resuming password-cracking sessions.
- Verifying recovered passwords.
- Practical use of Kali Linux terminal commands.

### Conclusion

This exercise strengthened my practical understanding of password security and password recovery techniques. It also demonstrated why organisations should enforce strong, unique passwords and avoid relying on common or easily guessed passwords.

*All testing was performed on the PDF files provided for the Networkwalks educational exercise.*
