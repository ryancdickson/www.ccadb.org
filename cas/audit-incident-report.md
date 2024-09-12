# Audit Incident Reporting Guidelines

## Change History

|Version|Effective Date|
|-|-|
|2.1 (current)|TBD| 
|[2.0](https://github.com/mozilla/www.ccadb.org/blob/master/incident_archive/ir_version_2_0.md)|October 17, 2023| 
|[1.0](https://github.com/mozilla/www.ccadb.org/blob/master/incident_archive/ir_version_1_0.md)|February 15, 2023|

## Audit Incident Reporting

**Note:** The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" on this page are to be interpreted as described in [RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119).

When audits are performed, an audit statement may document qualifications or non-conformities (i.e., findings) that were identified during the audit. In some cases, each finding disclosed in the audit statement may have been self-reported by a CA Owner or third party in a previous [Incident Report](incident-report). In cases where **each** finding was *not* previously recorded in an Incident Report, CA Owners MUST create a new Bugzilla issue by filling out the "Summary" and "Description" fields of [this form](https://bugzilla.mozilla.org/enter_bug.cgi?format=__default__&product=CA%20Program&component=CA%20Certificate%20Compliance&bug_type=task). The Summary field MUST include the CA Owner name, a colon, and "Findings in 20XX Audit", where XX is the year the audit period or point-in-time ended (e.g., "CA ABC: Findings in 2023 Audit").

To create the audit incident report, copy the markdown template below and fill out each section according to the following instructions and requirements:

1. The **Finding** Section MUST contain a description of the nature of each finding. This provides context for the reader to understand the nature of the non-compliance identified by the Auditor.
2. The **Root Cause Analysis** Section MUST contain a detailed analysis of the conditions which combined to give rise to the issue. It is unusual for an incident to have a single root cause; often there must be a confluence of several issues such as a software bug, insufficient checks, and a malformed request. Make sure that **all** contributing causes are identified and described, including noting when they first arose and how they avoided detection until they were discovered or identified.
3. The **Action Items** Section MUST contain a list of remediation items that were or will be undertaken to ensure that similar incidents do not reoccur in the future. Note that it is not sufficient for these action items to simply stop this incident, they MUST create additional protections to prevent future incidents. Each Action Item MUST state:
   - A detailed description of the action that was or will be taken.
   - A classification of whether the action will help _Prevent_ future incidents, _Mitigate_ the impact of future incidents, or _Detect_ future incidents. CA Owners are encouraged to propose action items in all three categories, with an emphasis on prevention and mitigation.
   - A date by which the action item was or will be completed.

If the audit includes multiple findings, the audit incident report should include a separate Finding, Root Cause Analysis, and Action Items Sections for each finding. 

### Audit Incident Report Template

```markdown
## Audit Incident Report

### Finding #1



### Root Cause Analysis



### Action Items

| Action Item | Kind | Due Date |
| ----------- | ---- | -------- |
| Example | Prevent | 2038-01-19 |

### Finding #2



### Root Cause Analysis



### Action Items

| Action Item | Kind | Due Date |
| ----------- | ---- | -------- |
| Example | Prevent | 2038-01-19 |

```


