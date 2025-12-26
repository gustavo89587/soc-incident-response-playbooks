# Phishing & Token Abuse

## Incident Scenario
Suspicious login or activity following phishing or MFA fatigue attempt.

## Detection
- Unusual sign-ins
- OAuth token abuse
- MFA prompt flooding

## Analysis
Attackers may gain access without malware by abusing credentials or tokens.
Check:
- IP reputation
- User-reported phishing
- Session activity

## Risk Assessment
High. Account compromise may impact cloud resources and data.

## Response Actions
1. Revoke sessions and tokens
2. Reset credentials
3. Review mailbox and cloud activity
4. Educate user if phishing confirmed

## MITRE ATT&CK Mapping
- TA0001 – Initial Access  
- T1566 – Phishing

## Lessons Learned
- Improve phishing detection
- Enforce conditional access policies
