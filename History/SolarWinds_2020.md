**2026-06-21**

# What happened essentially?
- Hackers, identified as APT29 (also known as Cozy Bear) linked to Russia Foreign Intelligence Agency, compromised SolarWinds via a supply chain attack. SolarWinds is a company that provides IT management software to governments and large organizations.
- The hack was discovered during december 2020 and it initiated during late 2019. The group targeted the SolarWinds's Orion software. 

# What consecuences did it have?
- 18.000 networks were compromised, including several US goverment department and private companies (like Deloitte, Microsoft, Cisco and FireEye).
- The attackers didn't seem interested in damaging the infrastructure, but rather in espionage. They also targeted not all of the infected networks, but the most critical ones.

# How did they breach the network in the first place?
- They used a technique called DLL hijacking in order to bypass the authentication mechanism of the SolarWinds's Orion software. 
- They basically, injected malware via a DLL during patch updates.
- The infected software was then signed with digital certificates from SolarWinds, making the malware look like legitimate trusted software.
- After that, they used sophisticated techniques to move laterally across networks, exploiting misconfigurations and vulnerabilities to gain access to sensitive data.

# Tools used:
- SUNSPOT: implant that injected the SUNBURST malware into the SolarWinds network. Used by APT29. It monitors processes related to the compilation of source code for the Orion software, it then replaces a source file with the SUNBURST backdoor.
- SUNBURST: trojanized dll malware used by APT29 since the SolarWinds attack. It remained dormant for weeks before exfiltrating data.
- TEARDROP: memory-only dropper used to deploy Cobalt Strike beacons on compromised networks.
- Other tools used: Cobalt Strike, AdFind, GoldFinder, GoldMax, Mimikatz, Raindrop, Sibot, TrailBlazer.

# Actions by the security teams
## Short term actions
- Isolate the infected systems from the internet to prevent communication between the malware and the Control and Command (C2) servers.
- Invalidate the digital certificates by resetting the accounts twice, allowing the tokens to rotate.
- Rebuild the systems from trusted media not just from backups, because they could be infected too.
- Disable single sign-on (SSO) and multi-factor authentication (MFA) on compromised systems to prevent lateral movement.

## Long term actions
- Supply chain verification, which means verifying the integrity of software updates and patches.
- Moving away from the "trusted networks" concept and pivoting around the Zero-Trust architecture.
- Conditional access.
- Behavioral hunting.

# NOTE:
- This is one of the most sophisticated attacks in the last years.

# Questions:
- Moving from trusted networks into Zero-Trust Architecture has prevented attacks of this kind of magnitude?
- What other types of supply chain attacks are there?
- How is the economic impact of this attack quantified?
- FireEye, KPMG and CrowdStrike helped SolarWinds during this period. They don't work for free. What happens if the affected company does not have resources to pay or ask for help? Do they shut down? Go to jail for inoperancy?

# Sources
- SolarWinds, CrowdStrike, MITRE Att&ck.