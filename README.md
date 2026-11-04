# NIST RMF Security Assessment & Authorization Simulation

## Overview
This project applies an RMF-style assessment process to a personal Ubuntu Server and Wazuh lab. I reviewed selected NIST SP 800-53 controls, implemented security changes, verified their results, and documented findings and outstanding remediation.

This is a learning exercise involving selected controls, not a complete compliance assessment or an official Authority to Operate (ATO).

## Lab Environment
- Ubuntu Server running in VMware Fusion on macOS
- Wazuh for security monitoring
- UFW for host firewall management
- APT for package updates
- Linux command line for configuration and verification

## Work Performed
- Configured and tested inbound firewall restrictions using UFW.
- Applied targeted package updates.
- Checked Wazuh service status and agent connectivity.
- Verified Wazuh service recovery and agent connectivity after reboot.
- Mapped lab activities and evidence to selected controls in the Access Control (AC), Configuration Management (CM), and System and Information Integrity (SI) families.
- Documented findings and outstanding remediation in a Plan of Action and Milestones (POA&M).
- Prepared a simulated authorization recommendation.

## How the Work Relates to the Seven RMF Steps

### 1. Prepare
Defined the Ubuntu/Wazuh lab as the assessment scope and identified the security functions to review: inbound access restrictions, package maintenance, and security monitoring.

### 2. Categorize
Considered the confidentiality, integrity, and availability needs of the lab. This exercise did not establish a formal FIPS 199 security categorization.

### 3. Select
Selected relevant NIST SP 800-53 controls for the exercise. The assessment covered a limited subset rather than a complete control baseline.

### 4. Implement
Configured UFW inbound restrictions and applied targeted package updates in Ubuntu.

### 5. Assess
Reviewed firewall status, package update results, Wazuh service status, and agent connectivity to evaluate whether the implemented changes worked as intended.

### 6. Authorize
Prepared a simulated authorization recommendation based on the assessment findings and outstanding remediation. No official authorization was issued.

### 7. Monitor
Performed post-reboot checks of Wazuh service recovery and agent connectivity. These checks demonstrate follow-up verification; a production system would require an ongoing monitoring program.

## Documentation and Evidence
- [Security assessment](<1. assessment.md>)
- [Remediation plan (POA&M)](poam.md)
- [Simulated authorization recommendation](authorization-recommendation.md)
- [Evidence screenshots](NIST-RMF-Evidence/)
The screenshots document a follow-up review of the lab's current state: configured firewall restrictions, a Wazuh startup failure, and pending package updates. Service recovery, completed patching, and endpoint connectivity were not verified during this review.

## What I Learned
This exercise connected technical changes to security assessment documentation. Configuring a firewall or applying an update is only part of the work: the result must be verified, supported by evidence, and documented alongside any remaining gaps.
