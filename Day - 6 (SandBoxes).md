## Learning Objectives

- Analyze malware behaviour using sandbox tools.
- Explore how to use YARA rules to detect malicious patterns.
- Learn about various malware evasion techniques.
- Implement an evasion technique to bypass YARA rule detection.

---
## Detecting Sandboxes

A sandbox is an isolated environment where (malicious) code is executed without affecting anything outside the system. Often, multiple tools are installed to monitor, record, and analyze the code's behaviour.

Mayor Malware knows that before his malware executes, it needs to check if it is running on a Sandbox environment. If it is, then it should not continue with its malicious activity.

---
## Can YARA Do It?

Mayor Malware knows that McSkidy is a big fan of YARA rules.

YARA is a tool used to identify and classify malware based on patterns in its code. By writing custom rules, analysts can define specific characteristics to look for—such as particular strings, file headers, or behaviours—and YARA will scan files or processes to find matches, making it invaluable for detecting malicious code.

Mayor Malware does not think such a simple tool can detect his malware. But just to be sure, he has to test it out himself.

To do this, he wrote a small script that executes a YARA detection rule every time a new event is added to the System monitor log. This particular YARA rule detects any command that tries to access the registry.

----
## Beware of Floss

While obfuscation is helpful, we also need to know that there are tools available that extract obfuscated strings from malware binaries. One such tool is Floss, a powerful tool developed by Mandiant that functions similarly to the Linux strings tool but is optimized for malware analysis, making it ideal for revealing any concealed details.

----

#AOC 