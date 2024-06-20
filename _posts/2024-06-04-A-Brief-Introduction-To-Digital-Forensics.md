Before discussing digital forensics we need clarity about forensic sciences.

You might have listened to the word forensics in movies, which is basically used to retrieve data from the crime scene.
In simpler words, forensic science is a branch of science to collect evidence using various scientific techniques and analysis of the electronic hardware or software available from the crime scene.
In the case of digital forensics, usually electronic evidence is collected. Electronic evidence is a piece of data available from the electronic devices involved in the crime. And for extraction of this data, five steps are followed :
1. **Identification**: It is the very first step in which the devices under attack are identified. In this stage, it is determined how long the attacker had access to the system and creating a timeline of the attack. 
2. **Preservation**: The identified devices are seized and stored to avoid any cases of tampering. After that, an investigator can use various forensic methods to extract the data from the device that may be helpful and then store this data securely.
3. **Analysis**:  The data preserved from the under-attack devices are replicated to perform the analysis that is recovering encrypted files or documents. This stage may involve a lot of techniques like reverse steganography, or various tools like Autopsy, Volatility, etc.
4. **Documentation**: After the analysis is done, the findings are properly documented so that the whole investigation process is understandable. Thus it provides a conclusion to a criminal activity so that the same mistakes are not repeated.
5. **Presentation**: The findings can be presented to the criminal court to provide evidence.

# Importance of Digital Forensics #
1. It can help to understand the reason behind the attack and who did it.
2. Data breach issues can be handled with care in this case
for example--
Let's say a company suffers from a data breach. A forensics analyst would investigate how the attacker got into the system and what actions were performed on their network, also, the analyst has to detect whether there was any manipulation of the company's database. In such cases, data has to be recovered from any damaged hardware.

# Types of Forensics #
## 1. Computer Forensics: ##
Investigation of computers and digital storage devices to identify, preserve, analyze, and present evidence.
Examples: Analyzing hard drives, solid-state drives (SSDs), and removable storage to recover deleted files, emails, browsing history, and system logs.

## 2. Network Forensics: #
Monitoring and analyzing network traffic to detect and investigate network-based attacks, data breaches, and unauthorized activities.
Examples: Capturing and examining packets, and logs from routers, firewalls, and intrusion detection systems (IDS).
Various log files recovered from digital analysis:
*System Logs (Syslogs)*:
Purpose: Record general system events such as reboots, hardware issues, software updates, and other critical events.
Content: Includes timestamps, event descriptions, severity levels, and source IP addresses.

*Traffic Logs*:
Purpose: Monitor and record network traffic passing through the router.
Content: Details about source and destination IP addresses, port numbers, protocols used, and the amount of data transmitted.

*Event Logs*:
Purpose: Record specific events like user logins, configuration changes, and failed login attempts.
Content: Usernames, timestamps, event types, and any changes made to the router’s configuration.

*Firewall Logs*:
Purpose: Record information about traffic that has been allowed or blocked by the router's firewall.
Content: Source and destination IP addresses, port numbers, action taken (allowed/blocked), and reasons for blocking.

## 3. Mobile Forensics: 
Retrieval and analysis of data from mobile devices like smartphones, tablets, and wearables.
Examples: Recovering call logs, text messages, photos, app data, GPS locations, and deleted data from Android and iOS devices.

## 4. Database Forensics: 
Examination of databases and their metadata to uncover tampering, data theft, or unauthorized access.
Examples: Investigating SQL databases to track changes, recover deleted records, and analyze transaction logs.

## 5. Memory Forensics: 
Analysis of volatile memory (RAM) to capture data that is lost when the device is powered off.
Examples: Examining memory dumps for running processes, network connections, encryption keys, and malicious code.

## 6. Malware Forensics: 
Investigation of malicious software to understand its behavior, origin, and impact.
Examples: Analyzing malware samples to determine how they infect systems, spread, and what data they compromise or steal.

## 7. Forensic Data Analysis: 
Examination of large datasets to detect patterns, anomalies, and hidden connections.
Examples: Using data mining and big data analytics to uncover fraud, financial crimes, and insider threats.

## 8. Multimedia Forensics:  
Analysis of digital multimedia files (images, audio, video) to verify authenticity, detect tampering, and extract metadata.
Examples: Using techniques like steganalysis to detect hidden messages, examining EXIF data, and analyzing audio files for signs of editing.


# Methods(Used in methods)

1. **Reverse Steganography**: It is a technique that is mainly used for extracting hidden info seemingly normal data, such as images, audio files, text, or other types of media.

2. **Data Carving or Deleted File Recovery**: It is a process of identifying and retrieving erased or deleted files by looking for any fragments that the deleted files could have left behind. The detailed explanation for this method is as follows:
> For data carving, first use write blockeers in order to avoid any alterations in data. And prepare a documentation of all actions taken.

> Then use tools like FTK(forensic Toolkit) imager to create a bit by bit copy of the storage device from where the info is to be extracted.

> To verify the integrity keep the cryptographic hashes of cryptographic devices and images. 
(programs that use a mathematical function, like an algorithm, to convert information to a hexadecimal form are cryptographic hash functions)  

> Next we analyze the forensic image as generated before.

> Then we analyze slack space (the unused space in the last cluster of a file) as it may contain remnants of deleted data

> Unallocated space can contain remnants of deleted files. Use forensic tools to search for file headers and footers to reconstruct deleted files.

> If a memory dump is available, analyze it using tools like *Volatility* or *Rekall*. Memory analysis can reveal data remnants that were in use before the deletion occurred.

> If the deleted data was encrypted, identify the encryption method and attempt to decrypt it using known keys, passwords, or cryptographic analysis techniques.

3. **Live Analysis**: It is a technique by which the volatile data that is kept in RAM or cache is located, analyzed, and extracted using system tools when the operating system is working or live. To effectively preserve the chain of evidence, live analyses are mainly conducted or examined in a forensic lab.

4. **Cross-drive Analysis (CDA)**: Cross-drive analysis is also used in the process of investigation analysis and is a feature extraction technique that enables investigators to examine data from many sources at once.

