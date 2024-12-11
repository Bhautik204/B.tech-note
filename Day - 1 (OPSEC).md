# Title : Maybe SOC-mas music, he thought, doesn't come from a store?
- ### Learning Objectives
	- Learn how to investigate malicious link files.
	- Learn about OPSEC and OPSEC mistakes.
	- Understand how to track and attribute digital identities in cyber investigations.

---

- ### YouTube to MP3 Converter Websites
	- These websites have been around for a long time. They offer a convenient way to extract audio from YouTube videos, making them popular. However, historically, these websites have been observed to have significant risks, such as:
	- **Malvertising**: Many sites contain malicious ads that can exploit vulnerabilities in a user's system, which could lead to infection.
	- **Phishing scams**: Users can be tricked into providing personal or sensitive information via fake surveys or offers.
	- **Bundled malware**: Some converters may come with malware, tricking users into unknowingly running it.

--- 
### Test
- when we extract dowload.zip and extract it , create `song.mp3` and `somg.mp3` . 
- To quickly determine the file's contents, double-click on the "Terminal" icon on the desktop then run the `file` command on each one. First, let's try checking `song.mp3`.
	- There doesn't seem to be anything suspicious, according to the output. As expected, this is just an MP3 file
- How about the second file `somg.mp3`? From the filename alone, we can tell something is not right. Still, let's confirm by running the `file` command on it anyway.
	- The output tells us that instead of an MP3, the file is an "MS Windows shortcut", also known as a `.lnk` file. This file type is used in Windows to link to another file, folder, or application. These shortcuts can also be used to run commands! If you've ever seen the shortcuts on a Windows desktop, you already know what they are.
	- There are multiple ways to inspect `.lnk`  files to reveal the embedded commands and attributes. For this room, however, we'll use **ExifTool**, which is already installed on this machine.
```
exiftool somg.mp3
```
- Look through the output to locate the command used as a shortcut in the `somg.mp3` file. If you scroll down through the output, you should see a PowerShell command.
- The `-ep Bypass -nop` flags disable PowerShell's usual restrictions, allowing scripts to run without interference from security settings or user profiles.

---

### OPSEC
- Operational Security (OPSEC) is a term originally coined in the military to refer to the process of protecting sensitive information and operations from adversaries. The goal is to identify and eliminate potential vulnerabilities before the attacker can learn their identity
- In the context of cyber security, when malicious actors fail to follow proper OPSEC practices, they might leave digital traces that can be pieced together to reveal their identity. Some common OPSEC mistakes include:
	- Reusing usernames, email addresses, or account handles across multiple platforms. One might assume that anyone trying to cover their tracks would remove such obvious and incriminating information, but sometimes, it's due to vanity or simply forgetfulness.
	- Using identifiable metadata in code, documents, or images, which may reveal personal information like device names, GPS coordinates, or timestamps.
	- Posting publicly on forums or GitHub (Like in this current scenario) with details that tie back to their real identity or reveal their location or habits.
	- Failing to use a VPN or proxy while conducting malicious activities allows law enforcement to track their real IP address.
- You'd think that someone doing something bad would make OPSEC their top priority, but they're only human and can make mistakes, too.

For example, here are some real-world OPSEC mistakes that led to some really big fails:

-----

#### AlphaBay Admin Takedown
One of the most spectacular OPSEC failures involved Alexandre Cazes, the administrator of AlphaBay, one of the largest dark web marketplaces:
- Cazes used the email address pimp_alex_91@hotmail.com in early welcome emails from the site.
- This email included his year of birth and other identifying information.
- He cashed out using a Bitcoin account tied to his real name.
- Cazes reused the username "Alpha02" across multiple platforms, linking his dark web identity to forum posts under his real name.

----

#### Chinese Military Hacking Group (APT1)

There's also the notorious Chinese hacking group APT1, which made several OPSEC blunders:

- One member, Wang Dong, signed his malware code with the nickname "Ugly Gorilla".
- This nickname was linked to programming forum posts associated with his real name.
- The group used predictable naming conventions for users, code, and passwords.
- Their activity consistently aligned with Beijing business hours, making their location obvious.

These failures provided enough information for cyber security researchers and law enforcement to publicly identify group members.

-----
#AOC 