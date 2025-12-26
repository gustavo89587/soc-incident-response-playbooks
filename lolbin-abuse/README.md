# LOLBin Abuse

## Incident Scenario
Use of a legitimate Windows binary (LOLBin) to execute suspicious activity.

## Detection
- Execution of tools like mshta.exe, rundll32.exe, regsvr32.exe
- External network connections
- Unusual execution context

## Analysis
LOLbins are trusted binaries abused to bypass security controls.
Key questions:
- Is this binary used legitimately in the environment?
- What is the parent process?
- Was execution blocked by EDR?

## Risk Assessment
High. LOLBin abuse often indicates active attacker behavior.

## Response Actions
1. Confirm whether activity was blocked
2. Review process tree and network activity
3. Contain endpoint if execution succeeded
4. Document behavior for future detection

## MITRE ATT&CK Mapping
- TA0005 – Defense Evasion  
- T1218 – Signed Binary Proxy Execution

## Lessons Learned
- Tune alerts for LOLBin misuse
- Maintain allowlists for legitimate admin usage
