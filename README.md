# SOC Portfolio Project #1  
## Alert Triage Walkthrough – Impossible Travel


### Project Overview

This project simulates a Tier 1–2 SOC analyst’s response to a common authentication alert: **Impossible Travel**.  
It demonstrates the full alert triage process from initial detection to final decision, using realistic investigative logic and structured documentation.


### Alert Summary

**Alert Name:** Impossible Travel Detected  
**Source:** Microsoft Sentinel (simulated)  
**Severity:** Medium  
**Timestamp:** July 6, 2025 – 08:17 AM  

**Description:**  
SIEM detected a login for user `j.smith@acmeinc.com` from **Bangkok, Thailand**, followed by another login from **Frankfurt, Germany** within 9 minutes.  
The geographic distance and short time frame exceed normal travel speed thresholds. This may indicate VPN use, credential compromise, or session hijacking.


### Triage Process

**1. Acknowledge and Assign Alert**  
- Alert assigned to Tier 1 analyst  
- Initial review begins in SIEM interface

**2. Review Alert Metadata in SIEM**  
- User: `j.smith@acmeinc.com`  
- Logins from Bangkok and Frankfurt, 9 minutes apart  
- Geo-distance: ~9000 km in under 10 mins

**3. Investigate User Account Activity**  
- Check recent logins, device types, and location history  
- Look for any prior impossible travel patterns

**4. Check Endpoint Detection and Response (EDR)**  
- Review device used in Bangkok login  
- Confirm endpoint agent activity and scan results  
- No malicious behavior or suspicious processes observed

**5. Review MFA and Authentication Logs**  
- MFA successfully completed for both logins  
- No brute force or password spraying activity

**6. IP Reputation Check**  
- Frankfurt IP: Associated with NordVPN (clean reputation)  
- Bangkok IP: Residential ISP in Thailand  
- No known malicious IP indicators

**7. User Verification**  
- Analyst contacted user via internal email  
- User confirmed they were traveling and used NordVPN  
- Device and login pattern match historical behavior

**8. Correlate With Other Alerts**  
- No additional alerts for the user or related assets  
- No lateral movement or suspicious internal activity
- 

### Findings and Analyst Decision

**Summary:**  
- Alert triggered by legitimate VPN activity  
- No malware, brute force, or lateral movement detected  
- User confirmed behavior and passed MFA checks

**Decision:**  
> Alert classified as a **false positive**  
> Closed in SIEM with full documentation and user education  

**Action Taken:**  
- Alert closed with notes  
- User informed about VPN impact on travel alerts  
- No further action required

### Skills Demonstrated

- Alert triage workflows (SOC Tier 1–2)  
- SIEM and EDR investigative logic  
- VPN/IP reputation analysis  
- Documentation for SOC ticketing systems  
- User communication and verification protocols


### Final Notes

While this project simulates the tools (Microsoft Sentinel, Defender, AbuseIPDB), the triage process reflects real-world SOC workflows.  
This write-up was created as part of the `Kybersecurity` portfolio to showcase practical incident response skills.

