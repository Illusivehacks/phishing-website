# phishing-website


🚨 Beware of Fake YouTube WatchTime Offer 🚨
Overview
This webpage claims to offer "4000 hours of YouTube WatchTime" if the user completes a verification process. However, in reality, it secretly collects user information, including:

IP Address

Geolocation

Device details (browser, OS, hardware)

Clipboard contents

Screen capture

Audio & video recordings

The collected data is then sent to a Telegram bot, allowing the attacker to monitor the victim's information remotely.

How the Code Works

1️⃣ Frontend UI

The webpage uses HTML & CSS to create a visually appealing page.
A "Complete Verification Now" button triggers the data collection.
A fake progress bar is shown to make the process appear legitimate.

2️⃣ JavaScript Data Collection

When the user clicks the button, the script attempts to gather:


IP Address: Fetched via an external API (ipapi.co).

Geolocation: Obtained using navigator.geolocation.getCurrentPosition().

Device Details: Extracted from navigator properties.

Clipboard Data: Reads the last copied text using navigator.clipboard.readText().

Screen Capture: Tries to record the screen using navigator.mediaDevices.getDisplayMedia().

Audio/Video Recording: Uses navigator.mediaDevices.getUserMedia() to record the microphone and camera.


3️⃣ Sending Data to Telegram

The stolen data is formatted into a Telegram message.

It is sent to a Telegram bot (controlled by the attacker) using sendMessage and sendPhoto API calls.


Security & Ethical Implications


🔴 This script is an example of a phishing attack and should NEVER be used for malicious purposes.

🔴 It violates user privacy and cybersecurity laws in many countries (GDPR, CCPA, etc.).

🔴 If you encounter a webpage like this, DO NOT enter your details or click any verification button.


How to Protect Yourself


✔ Never trust offers that seem too good to be true.

✔ Do not grant unnecessary permissions (camera, microphone, clipboard access) to unknown websites.

✔ Use a browser with strong privacy settings.

✔ Report suspicious websites to cybersecurity authorities.



⚠️ Disclaimer:


This README is for educational and ethical hacking awareness only. The intent is to educate users on how phishing pages work so they can recognize and avoid such scams. Do not use this knowledge for illegal activities.


🚀 Stay Safe Online! 🚀







