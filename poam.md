# Plan of Action and Milestones (POA&M)

This document tracks the issues found during the lab review, the steps planned to address them, and the evidence needed to confirm completion.

These are planned actions. No fixes were completed during this review.

## F-01: Wazuh Manager Startup Failure

**Finding:** Wazuh Manager reported a startup timeout. Some Wazuh processes were still running, but healthy monitoring was not confirmed.

**Why it matters:** The lab may not reliably collect and process security events.

**Planned actions:**
1. Review the Wazuh and system logs to understand the startup failure.
2. Address the cause and start the service.
3. Confirm that the service stays running and receives new events from the endpoint.

**Owner:** Kenneth Martey  
**Status:** Open  
**Target completion:** To be scheduled  
**Evidence needed to close:** Service status showing active and running, plus a new endpoint event received by Wazuh.

## F-02: Pending Package Updates

**Finding:** Ubuntu's saved package list showed available updates, including updates for Wazuh Manager, Indexer, and Dashboard.

**Why it matters:** Pending updates may include security fixes and reliability improvements. The update list alone does not establish specific vulnerabilities.

**Planned actions:**
1. Refresh the package list.
2. Review available updates and compatibility requirements.
3. Back up the lab before making changes.
4. Apply the selected updates and check that the affected services work afterward.

**Owner:** Kenneth Martey  
**Status:** Open  
**Target completion:** To be scheduled  
**Evidence needed to close:** Update results, installed package versions, and successful service checks.

## F-03: Firewall Rules Need Connection Testing

**Finding:** UFW was active with incoming traffic denied by default and two rules allowing specific traffic from the Mac host. Connection testing was not performed during this review.

**Why it matters:** Reviewing the rules shows the intended restrictions. Testing is needed to confirm how they work.

**Planned actions:**
1. Confirm that an approved connection to a listening service succeeds.
2. Test a connection that should be blocked.
3. Record the results and review firewall logs to confirm that UFW caused the block.

**Owner:** Kenneth Martey  
**Status:** Verification pending  
**Target completion:** To be scheduled  
**Evidence needed to close:** Test results showing the allowed connection succeeds and the prohibited connection is blocked by the firewall.

## Follow-Up

Each finding will remain open until the planned work is completed and supporting evidence is saved. Any remaining gaps will be documented before a finding is closed.
