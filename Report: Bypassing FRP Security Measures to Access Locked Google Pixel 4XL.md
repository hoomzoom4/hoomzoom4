# Report: Bypassing FRP Security Measures to Access Locked Google Pixel 4XL

### Introduction

**Objective**: To regain access to a Google Pixel 4XL after the lock screen PIN and Gmail password were forgotten, using ethical and legal methods to assist a family member in need.

**Context**: In 2021, My father forgot his phone’s lock screen PIN and Gmail password. Despite attempting all possible combinations and recovery options, he was unable to unlock his phone. As he needed the phone for work the next day, I took on the challenge to help him regain access.

### Problem Statement

The primary issue was the inability to unlock the Google Pixel 4XL due to forgotten credentials. The phone required a factory reset, which led to a further challenge of bypassing the Google account verification during the phone setup process.

### Methodology

### Step 1: Factory Reset

1. **Initial Attempt**: Attempted all known PIN combinations and Gmail password recovery options without success.
2. **Decision to Factory Reset**: Decided to perform a factory reset to regain access to the phone, understanding the implications of data loss and the need for a clean slate.

![a73dece1-82db-4363-933f-6390c00c3592](https://github.com/hoomzoom4/hoomzoom4/assets/139533936/ea06efae-f6ab-4750-9eda-3c0eacd9f282)

### Step 2: Bypassing Google Account Verification

1. **Encountering Verification**: After the factory reset, the phone required the original Google account login, triggering the Factory Reset Protection (FRP) mechanism.

![FRP_LOCK](https://github.com/hoomzoom4/hoomzoom4/assets/139533936/61ceb6dd-2e09-4252-af4f-2c8bd0871778)

1. **Exploring Accessibility Settings**: At the initial setup page (language selection), accessed the "Help" button to navigate to the FAQ website, leveraging the accessibility features (“Assistive options”) as an attack vector.

![b2ca7d45-3dbc-415b-9361-47a3b1007372](https://github.com/hoomzoom4/hoomzoom4/assets/139533936/f776f9ea-ba56-4135-8cd7-4b367712aa47)

1. **Finding a Backdoor**: Utilized the accessibility settings to exploit a legitimate backdoor, allowing navigation to the login page for Gmail.
2. **Logging into New Gmail**: Conducted a session hijacking by logging into my father’s new Gmail account and logging out of the old one.
3. **Completing Setup**: Returned to the initial setup page and continued the setup process using the new Gmail account, effectively bypassing the FRP lock.

### Results

- Successfully bypassed the Google account verification, mitigating the FRP lock.
- Completed the phone setup with the new Gmail account, restoring full functionality.
- Ensured the phone was operational, allowing my father to resume his work without further delay.

![new_pixel](https://github.com/hoomzoom4/hoomzoom4/assets/139533936/15720952-040a-4a2d-b625-3266a28318a8)

### Technical Skills Demonstrated

- **Problem-Solving**: Identified and implemented a solution to bypass security measures using ethical hacking techniques.
- **Technical Knowledge**: Applied knowledge of Android OS, Google account management, and FRP mechanisms.
- **Resourcefulness**: Exploited a legitimate backdoor through accessibility settings, demonstrating an understanding of potential attack vectors.
- **Persistence**: Demonstrated determination by spending several hours to find a viable solution, showcasing resilience in troubleshooting.

### Ethical Considerations

- **Legality**: Ensured that all actions taken were within legal boundaries and aimed at helping a family member regain access to their own device.
- **Ethical Hacking**: Applied ethical hacking principles to solve a real-world problem without causing harm or violating terms of service, adhering to the ethical guidelines of cybersecurity practices.

### Conclusion

This project highlights my ability to handle cybersecurity challenges, think critically, and apply technical skills to solve problems. The experience has reinforced my interest in cybersecurity and my commitment to developing my skills further. I believe this project demonstrates my potential as a candidate for the Poly Cyber Work-Learn Scheme by the Digital and Intelligence Service.
