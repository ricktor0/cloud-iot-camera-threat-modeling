## 1) What is a threat model ? 

- Threat model is basically a structured description which tells us what are we defending, whom we are defending against , and how they might attack , and what we can do to protect against the attacker.
## 2) Threat modeling 

-  A systematic way of identifying possible threats, ranking them by risk, and planning what controls we can put in to mitigate them.
## 3) What a threat model includes 

- Description of the system (architecture, data flows, trust boundaries).
- Assumption of the environment and the attacker (suppose DB is in the private sub net etc ).
- Assets worth protecting (Database, credentials, services )
- Potential threats  and attack paths relevant to that system.
- Mitigations or security control maps to each threat.
- A way to validate that mitigations actually work (testing, reviews, etc.)
## 4) Why threat model  

- It helps in finding the left or missing control early (left during SDLC or development).
-  Prioritize work by focusing on threats with highest impact and likelihood.
- Communicate risks and required controls clearly to devs, architects, and management.

## 5) Some common types of threat models :

### 1. STRIDE :
Originally developed by Microsoft for structured threat identification.
STRIDE is a **threat classification model**.

It answers:
>“What kinds of things can go wrong in this system?”

- It does NOT score risk.  
- It does NOT simulate attacks.  
- It categorizes threats.
-----
### 2. DREAD :
- Also developed at Microsoft.
- DREAD is a **risk scoring model**, not a threat identification model.
- It evaluates severity.

| Letters | Meaning          |
| ------- | ---------------- |
| D       | Damage potential |
| R       | Reproducibility  |
| E       | Exploitability   |
| A       | Affected users   |
| D       | Discoverability  |
### Example in IoT Camera

Token leakage vulnerability:
- Damage: High (privacy exposure)
- Reproducibility: High
- Exploitability: Medium
- Affected users: High
- Discoverability: Medium
 Result → High risk
-----
### 3. CVSS (Common Vulnerability Scoring System) :

- Maintained by FIRST.
- CVSS is used globally for scoring vulnerabilities (like CVEs).
- It produces a numerical score (0–10).

It evaluates:

- Attack vector
- Attack complexity
- Privileges required
- User interaction
- Scope
- Impact (Confidentiality, Integrity, Availability)
#### Example

An unauthenticated remote API exposure:
- Attack vector: Network
- Privileges required: None
- Impact: High confidentiality
Score might be 9.8 (Critical).
----
### 4. ATTACK TREE : 

- Proposed by Bruce Schneier.
- Attack tree is a graphical model.

**Structure:**

Root = Attacker Goal  
Branches = Sub-goals  
Leaves = Attack steps
#### Example 

Goal: Access live stream

Branch 1:
- Steal credentials
- Exploit weak password reset

Branch 2:
- MITM network
- Intercept RTSP

Branch 3:
- Exploit cloud API
- Bypass authentication


