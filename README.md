
<p align="center">
<img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExcTY5aXMxZW0yN2JsYjl1c2s4ZG9lMDY0NnRob3ViMGt6MDd3NG96NiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/3o7bu0FIFT72QiCL3q/giphy.gif", width="300", height="300">
</p>

<h1 align="center"> K0RA </h1>
<h4 align="center">Linux-based botnet builder</h4>

### DESCRIPTION

DEDSEC_K0RA is a Linux-based botnet builder designed for creating advanced botnet payloads. The tool allows users to inject malicious payloads into legitimate Python code, enabling the creation of stealthy and persistent botnets. The payload is equipped with advanced features, including the ability to hide within a victim's system, ensure continuous operation through persistence mechanisms, and utilize a Google Calendar as a Command and Control (C2) server for covert communication and command issuance.

The primary function of the botnet payload is to send flood requests to a target server, enabling Distributed Denial of Service (DDoS) attacks. This tool is intended solely for penetration testing and ethical hacking purposes. Always ensure you have explicit permission before using this tool on any device or network. Unauthorized use is illegal and unethical.

### Key Features
  * Botnet Payload Injection: Inject malicious payloads into legitimate Python code or other software.
  * Persistence: Ensures the payload remains active on the victim's system even after reboots.
  * Stealth: The payload is designed to hide within the system, avoiding detection.
  * Command and Control (C2) via Google Calendar: Leverages Google Calendar as a covert C2 server for issuing commands, receiving updates, and coordinating botnet activities without raising suspicion.
  * DDoS Capability: The primary function of the payload is to send flood requests to a target server, overwhelming it and causing a denial of service. Supported attack types include:
    
     - UDP Flood Attack
     - SYN Flood Attack
     - HTTP Flood Attack
     - HTTPS Flood Attack
     - ICMP Flood Attack
     - ACK Flood Attack
     - SLOWLORIS Attack
     - SLOWLORIS HTTPS Attack

#### Intended Use:

* Penetration Testing: Simulate advanced attacks to identify vulnerabilities in systems and networks.

* Ethical Hacking: Test the resilience of systems against botnet-based attacks.

* Research and Education: Study botnet behavior and develop countermeasures.

### SETUP
Setup (Google Calendar C2)

Follow the steps below to configure your Google Cloud project and enable Google Calendar API for C2 communication.

1. Create a Google Cloud Project and Service Account

    Go to: https://console.cloud.google.com

    From the sidebar, go to IAM & Admin → Service Accounts

    Click + Create Project
     * Project name: (e.g.,) rat-calendar-c2
     * Click Create

    Click + Create Service Account
     * Service account name: e.g. test-c2
     * Description: (optional)
     * Click Create and Continue

    Grant this service account access:
      * Role: Owner
      * Click Continue → Done

    Click your newly created service account
      * Go to the Keys tab
      * Click Add Key → Create New Key
      * Select JSON, then click Create
      * Save the file as: creds.json in your directory

3. Share Google Calendar with Service Account

    Visit: https://calendar.google.com

    On the left, click the 3-dot menu beside your calendar → Settings and sharing

    Scroll to Share with specific people
     * Click + Add people and groups
     * Paste your Service Account email
     * Example: test-c2@your-project-id.iam.gserviceaccount.com
     * Set permission to: Make changes and manage sharing
     * Click Send

5. Enable Google Calendar API

     * Go to: https://console.cloud.google.com/apis/library
     * Search for: Google Calendar API
     * Click it → Click Enable
     * 
### INSTALLATION
     git clone https://github.com/0xbitx/DEDSEC_K0RA.git
     cd DEDSEC_K0RA
     sudo pip3 install psutil tabulate requests --break
     chmod +x dedsec_k0ra
     sudo ./dedsec_k0ra

### TESTED ON FOLLOWING [buidler&payload]
* Kali Linux 
* Parrot OS 
* Ubuntu

## Support

If you find my work helpful and want to support me, consider making a donation. Your contribution will help me continue working on projects.

**Bitcoin Address: `36ALguYpTgFF3RztL4h2uFb3cRMzQALAcm`**
   
<h1 align="center"> DISCLAIMER </h1>

<h4 align="center">I'm not responsible for anything you do with this program, so please only use it for good and educational purposes. </h4>
