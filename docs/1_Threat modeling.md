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
## 5) Some common types of threat models

- STRIDE
- DREAD
- CVSS
- ATTACK TREE