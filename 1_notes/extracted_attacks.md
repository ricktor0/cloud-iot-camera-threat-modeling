**1. Device / Firmware Layer**

*   **Attack Name:** Hardcoded and Default Credentials
    *   **Short Description:** Manufacturers often ship IoT devices like IP cameras and DVRs with default, easily guessable, or hardcoded root passwords embedded in the firmware, allowing attackers or botnets (such as Mirai) to gain unauthorized access via Telnet or SSH.
    *   **Affected Layer:** Device / Firmware Layer

*   **Attack Name:** Buffer Overflow and Code Injection
    *   **Short Description:** Embedded HTTP servers or CGI scripts in IoT firmware often lack proper input validation, permitting attackers to send oversized or malformed requests that execute arbitrary system commands or crash the device.
    *   **Affected Layer:** Device / Firmware Layer

*   **Attack Name:** Physical Tampering and Storage Extraction
    *   **Short Description:** Attackers with physical access can remove unencrypted external storage (like SD cards) to view private videos, extract network credentials, or connect to exposed UART interfaces to gain a root shell and modify the firmware.
    *   **Affected Layer:** Device / Firmware Layer

*   **Attack Name:** Hidden Backdoors
    *   **Short Description:** Device firmware may contain intentionally or unintentionally placed undocumented access methods (such as a specific user-agent string) that allow unauthenticated remote attackers to execute system commands.
    *   **Affected Layer:** Device / Firmware Layer

*   **Attack Name:** Insecure Firmware Updates
    *   **Short Description:** Devices that download over-the-air (OTA) updates via unencrypted HTTP links or fail to cryptographically verify the firmware's signature allow attackers to perform a Man-in-the-Middle attack and flash malicious firmware.
    *   **Affected Layer:** Device / Firmware Layer

**2. Network / Streaming Layer**

*   **Attack Name:** Unencrypted Communication and Packet Sniffing
    *   **Short Description:** Sensitive information, including Wi-Fi passwords, login credentials, and live video streams (using protocols like RTP or RTSP), is often transmitted in clear text, exposing it to eavesdroppers using tools like Wireshark.
    *   **Affected Layer:** Network / Streaming Layer

*   **Attack Name:** Man-in-the-Middle (MitM) and ARP Spoofing
    *   **Short Description:** Attackers poison the ARP cache of a local network to position themselves between the IoT device and the gateway, allowing them to intercept, block, or alter network traffic.
    *   **Affected Layer:** Network / Streaming Layer

*   **Attack Name:** Denial of Service (DoS) and Flooding
    *   **Short Description:** Attackers overwhelm the network or device resources by sending excessive requests, such as TCP SYN floods, UDP floods, or SSDP amplification attacks, effectively crashing the web server or terminating live video feeds.
    *   **Affected Layer:** Network / Streaming Layer

*   **Attack Name:** Traffic-Based Side-Channel Attack (Video Fingerprinting)
    *   **Short Description:** Even if a video stream is encrypted over DASH, attackers can analyze the variable bit-rate (VBR) burst patterns of the network traffic to uniquely identify which video a user is watching.
    *   **Affected Layer:** Network / Streaming Layer

*   **Attack Name:** Video Injection and Session Modification
    *   **Short Description:** Exploiting unencrypted RTSP or RTP protocols, an attacker can inject fake video clips (e.g., using VideoJak) into a live stream or forge SIP Re-Invite messages to maliciously modify or tear down a multimedia session.
    *   **Affected Layer:** Network / Streaming Layer

*   **Attack Name:** Pollution Attacks
    *   **Short Description:** In Peer-to-Peer (P2P) video streaming networks, malicious peers replace original video chunks with forged content and broadcast it, degrading the system's performance and service quality.
    *   **Affected Layer:** Network / Streaming Layer

**3. Cloud / Backend Layer**

*   **Attack Name:** API Unauthorized Access
    *   **Short Description:** Cloud Application Programming Interfaces (APIs) frequently lack strict authentication and input validation, enabling attackers to bypass verification, extract sensitive data, or issue unauthorized control commands to IoT devices.
    *   **Affected Layer:** Cloud / Backend Layer

*   **Attack Name:** Information Leakage and Exposed Databases
    *   **Short Description:** Misconfigured cloud backends, such as unprotected MongoDB databases or insecure MQTT brokers, expose sensitive telemetry, PII, and private audio/video recordings to the public internet.
    *   **Affected Layer:** Cloud / Backend Layer

*   **Attack Name:** Cloud and Device Impersonation
    *   **Short Description:** Due to weak mutual authentication—such as relying solely on a device's MAC address—attackers can impersonate the cloud server to the device, or spoof the device to the cloud, allowing them to inject forged streams or eavesdrop on data.
    *   **Affected Layer:** Cloud / Backend Layer

*   **Attack Name:** Multi-tenancy Resource Isolation Failures
    *   **Short Description:** In shared cloud infrastructures, inadequate isolation between different tenants (e.g., various IoT service providers) can lead to privacy breaches, cross-tenant attacks, and unauthorized access to other users' IoT data.
    *   **Affected Layer:** Cloud / Backend Layer

**4. Application / User Layer**

*   **Attack Name:** Sensitive Information Leakage via Local Storage
    *   **Short Description:** Mobile companion apps frequently store sensitive data—such as Wi-Fi passphrases, email addresses, and authentication tokens—in plain text within local XML/JSON files, or inadvertently expose them through Android's Logcat debugging tool.
    *   **Affected Layer:** Application / User Layer

*   **Attack Name:** Cryptographic API Misuse
    *   **Short Description:** Mobile IoT apps often implement broken cryptographic practices, such as using obsolete algorithms (MD5, SHA-1, AES-ECB) or relying on hardcoded, constant cryptographic keys, which compromises data integrity and confidentiality.
    *   **Affected Layer:** Application / User Layer

*   **Attack Name:** Flawed SSL/TLS Implementation
    *   **Short Description:** Companion apps frequently bypass proper SSL/TLS certificate validation by using custom trust managers that accept all certificates or failing to implement certificate pinning, leaving the app vulnerable to MitM attacks.
    *   **Affected Layer:** Application / User Layer

*   **Attack Name:** Over-privileged Apps and Intent Spoofing
    *   **Short Description:** IoT applications often request unnecessary runtime permissions or fail to secure internal components, allowing malicious applications on the same phone to spoof intents and steal passwords, camera data, or access point details.
    *   **Affected Layer:** Application / User Layer

*   **Attack Name:** Co-located App Attacks (App-in-the-Middle)
    *   **Short Description:** A malicious application installed on the user's smartphone leverages coarse-grained OS permissions to hijack the shared Bluetooth/BLE channel, gaining unauthorized access to the IoT device through the legitimate companion app.
    *   **Affected Layer:** Application / User Layer
