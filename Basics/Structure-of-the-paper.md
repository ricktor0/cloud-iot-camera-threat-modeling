**1. Introduction**  
Briefly introduce IoT camera systems, explain why cloud-connected cameras pose security challenges, and outline the motivation and goals of the study.

**2. Architecture of Cloud-Connected IoT Camera Systems**  
Describe how a typical cloud-based IoT camera system works, including device hardware, network communication, cloud backend services, and user applications.

**3. Threat Modeling Approach**  
Explain the threat modeling methodology used in the paper (layered model and STRIDE concepts) to analyze security risks across the system.

**4. Security Challenges**  
Analyze the major security vulnerabilities affecting different components of cloud-connected IoT camera systems.

	4.1 Device Layer Attacks 
	Discuss attacks targeting camera firmware and hardware, such as default credentials, insecure firmware updates, and physical tampering.

	4.2 Network / Streaming Layer Attacks 
	Explain network-based threats like RTSP interception, man-in-the-middle attacks, traffic analysis, and video stream manipulation.

	4.3 Cloud / Backend Attacks  
	Describe vulnerabilities in cloud services including insecure APIs, authentication failures, exposed databases, and device impersonation.

	4.4 Application Layer Attacks  
	Analyze weaknesses in mobile or web applications such as credential leakage, TLS misconfiguration, and over-privileged applications.

**5. Cross-Layer Attack Scenarios**  
Show how vulnerabilities across different layers can combine to form more complex attack chains that compromise the entire system.

**6. Defense Mechanisms**  
Summarize existing security solutions and mitigation techniques proposed in the literature to protect IoT camera systems.

**7. Research Gaps**  
Identify limitations in current research and highlight areas that require further investigation for improving IoT camera security.

**8. Conclusion**  
Summarize the key findings of the study and emphasize the importance of a layered security approach for cloud-connected IoT camera systems.




# Priority of the sections :

2 Architecture
4 Security Challenges
3 Threat Modeling
5 Cross-Layer Attacks
6 Defense Mechanisms
1 Introduction
7 Research Gaps
	8 Conclusionp