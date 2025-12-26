# Brute Force / Credential Access

## Incident Scenario
Multiple failed authentication attempts followed by a successful login from an external IP and unusual time window.

## Detection
- Repeated failed logins for the same user
- Successful authentication after failures
- Source IP external to the organization
- Login outside business hours

## Analysis
This pattern indicates a possible brute force or password spraying attack that eventually succeeded.
Key validation points:
- Is the IP known or previously seen?
- Is the login time consistent with user behavior?
- Was MFA involved or bypassed?

## Risk Assessment
High risk. Successful credential access may lead to:
- Lateral movement
- Data exfiltration
- Privilege escalation

## Response Actions
1. Isolate the affected account
2. Force password reset and revoke sessions
3. Review authentication logs for related accounts
4. Escalate to N2 / IR team if scope increases

## MITRE ATT&CK Mapping
- TA0006 – Credential Access  
- T1110 – Brute Force

## Lessons Learned
- Improve detection thresholds for failed logins
- Add behavioral baselines per user
- Enforce MFA where possible
