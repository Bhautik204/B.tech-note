## True Positives or False Positives?
- In a SOC( Security Operations Cent), events from different devices are sent to the SIEM, which is the single source of truth where all the information and events are aggregated. Certain rules (Detection Engineering rules) are defined to identify malicious or suspicious activity from these events. If an event or set of events fulfils the conditions of a rule, it triggers an alert. A SOC analyst then analyses the alert to identify if the alert is a True Positive (TP) or a False Positive (FP). **An alert is considered a TP if it contains actual malicious activity**. On the flip side, **if the alert triggers because of an activity that is not actually malicious, it is considered an FP.** This might seem very simple in theory, but practically, separating TPs from FPs can be a tedious job. It can sometimes become very confusing to differentiate between an **attacker** and **a system administrator.**
## Making a Decision

- While it is confusing to differentiate between TPs and FPs, it is very crucial to get it right. If a TP is falsely classified as an FP, it can lead to a significant impact from a missed cyber attack. If an FP is falsely classified as a TP, precious time will be spent focusing on the FP, which might lead to less focus on an actual attack. So, how exactly do we ensure that we perform this crucial job effectively? We can use the below pointers to guide us.

## Using the SOC Superpower
- The SOC has a superpower. When they are unsure whether an activity is performed by a malicious actor or a legitimate user, they can just confirm with the user. This privilege is not available to the attacker. A SOC analyst, on the other hand, can just send an email or call the relevant person to get confirmation of a certain activity. In mature organisations, any changes that might trigger an alert in the SOC often require Change Requests to be created and approved through the IT change management process. Depending on the process, the SOC team can ask the users to share Change Request details for confirmation. Surely, if it is a legitimate and approved activity, it must have an approved Change Request.

#### context
While it might seem like using the SOC superpower makes things super easy, that is not always the case. There are cases which can act as Kryptonite to the SOC superpower:

- If an organisation doesn't have a change request process in place.
- The performed activity was outside the scope of the change request or was different from that of the approved change request.
- The activity triggered an alert, such as copying files to a certain location, uploading a file to some website, or a failed login to a system. 
- An insider threat performed an activity they are not authorised to perform, whether intentionally or unintentionally.
- A user performed a malicious activity via social engineering from a threat actor.

In such scenarios, it is very important for the ==SOC analyst== to understand the context of the activity and make a judgement call based on their `analysis skills and security knowledge.` While doing so, the analyst can look at the `past behaviour of the user or the prevalence of a certain event or artefact throughout the organisation or a certain department`. For example, *if a certain user from the network team is using Wireshark, there is a chance that other users from the same team also use Wireshark. However, Wireshark seen on a machine belonging to someone from HR or finance should rightfully raise some eyebrows.*

##

![https://youtu.be/-FSt5WmvTEM](https://youtu.be/-FSt5WmvTEM)

Questions : 
What is the name of the account causing all the failed login attempts? - ADM-01
How many failed logon attempts were observed? -1187
What is the IP address of Glitch? -10.0.255.1
When did Glitch successfully logon to ADM-01? Format: MMM D, YYYY HH:MM:SS.SSS - |   |
|---|
|Dec 1, 2024 @ 08:54:39.000|
What is the decoded command executed by Glitch to fix the systems of Wareville? -