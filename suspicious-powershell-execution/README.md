# Suspicious PowerShell Execution

## Incident Scenario
PowerShell executed with suspicious parameters, potentially initiated by a document or script.

## Detection
- PowerShell execution with encoded or obfuscated commands
- Unusual parent process (e.g., Office applications)
- Execution outside expected admin workflows

## Analysis
PowerShell is commonly abused for post-exploitation.
Validation focuses on:
- Command-line arguments
- Parent-child process relationship
- User context and execution time

## Risk Assessment
Medium to high risk depending on payload and persistence indicators.

## Response Actions
1. Terminate the PowerShell process
2. Isolate endpoint if persistence is suspected
3. Collect command-line and script content
4. Escalate if malicious behavior confirmed

## MITRE ATT&CK Mapping
- TA0002 – Execution  
- T1059.001 – PowerShell

## Lessons Learned
- Enhance detection for PowerShell + Office chains
- Alert on encoded commands
