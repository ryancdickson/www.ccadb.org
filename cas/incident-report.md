# Incident Reporting Guidelines

## Change History

|Version|Effective Date|
|-|-|
|2.1 (current)|TBD| 
|[2.0](https://github.com/mozilla/www.ccadb.org/blob/master/incident_archive/ir_version_2_0.md)|October 17, 2023| 
|[1.0](https://github.com/mozilla/www.ccadb.org/blob/master/incident_archive/ir_version_1_0.md)|February 15, 2023|

## Incident Reporting

**Note:** The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" on this page are to be interpreted as described in [RFC 2119](https://datatracker.ietf.org/doc/html/rfc2119).

### Who can submit an Incident Report?
Anyone should feel encouraged to submit an Incident Report that’s founded upon credible and well-substantiated evidence.

Some Root Store Operator policies require CA Owners to submit an Incident Report as described on this page after self-discovering or being made aware of an Incident (e.g., receiving and corroborating an issue described in a Certificate Problem Report).

### How do I submit an Incident Report?
Create a new Bugzilla issue by filling out the Summary and Description fields of [this form](https://bugzilla.mozilla.org/enter_bug.cgi?format=__default__&product=CA%20Program&component=CA%20Certificate%20Compliance&bug_type=task). 

The "Summary" field in Bugzilla (i.e., "Subject line") MUST begin with the CA Owner’s name, followed by a colon, and a brief title that highlights the type of incident being reported (e.g., "EXAMPLE CA OWNER: Incorrect Subject RDN Encoding"). 

The "Description" field MAY contain a Preliminary or Full Incident Report (copied and pasted from the corresponding markdown template, as explained [below](#incident-report-templates)). 

### What format should be used?
Use one of the templates below, depending on the type of Incident Report being disclosed:

- [Preliminary Incident Report](#preliminary-incident-report) (for third party reporters and CA Owners)
- [Full Incident Report](#full-incident-report) (for CA Owners)

If being reported by the CA Owner corresponding with an incident, all fields included in the relevant template MUST be completed.

### When are Incident Reports expected?

Within 72 hours of the CA Owner being made aware of an incident (i.e., “initial incident disclosure”), it MUST 

Either:
1) disclose a Preliminary or Full Incident Report; or
2) respond to a Preliminary Incident Report previously created for the incident by a third party reporter.

And:
- accurately and completely disclose the impact of the incident (e.g., a corpus of mis-issued certificates).
- describe whether the incident should be considered contained (e.g., because certificate issuance was stopped) or ongoing.

While Full Incident Reports SHOULD be posted as soon as possible, they MUST be posted within 14 days of the incident’s initial disclosure.

### What is considered an incident?

[todo: write the following better]
The failure of a CA Owner to meet the commitments of the corresponding set of CA/Browser Forum Baseline Requirements, the CCADB Policy, or the corresponding Root Program policy associated with either an inclusion reuqest or an included root is considered an incident.

### What is considered an "initial incident disclosure"?
[todo - give examples, describe when the clock starts]

[third party report]
[internal problem repoert]

[If we imagine the following events....]
[use this as an opportunity to define when the clock starts for revocation?]

### When should Incident Reports be updated?

CA Owners SHOULD respond promptly to comments and questions, and in no circumstances MUST a request or question linger without a response for more than 7 days , even if the response is only to acknowledge the request or question and provide a later date when a response will be delivered. Comments from the community SHOULD be acknowledged and addressed by CA Owners.

Open Incident Reports MUST be updated:
- on or before the “Next update” date in the “Whiteboard” field of the bug (note: CA Owners MAY request the "Next update" Whiteboard field be set by a Root Store Operator to align with a specific date related to an open Action Item.);
- weekly, if a “Next update” date is not recorded;
- in response to community questions or comments as described above; or
- when Action Items are changed, completed, or delayed.

### How should Incident Reports be scoped?

There SHOULD be a single Incident Report for each distinct matter, and CA Owners MUST submit an additional, separate Incident Report when:
- policy requires the revocation of one or more certificates by a certain deadline, such as those in BR Section 4.9, but that deadline will not be or has not been met by the CA Owner (i.e., a delayed revocation Incident Report).
- in the process of researching one incident, another incident with a distinct root cause and/or remediation is discovered.
- after an incident is marked resolved in Bugzilla, the incident reoccurs.

Incident Reports MUST be free-standing (i.e., not rely upon the contents of other reports). The Incident Report MAY repeat things previously stated in discussions or Bugzilla comments, in which case the report SHOULD state a summary of previous findings. The existence of data in discussions or Bugzilla comments does not excuse a CA Owner from the task of compiling an Incident Report that aligns with the guidance on this page.

### How should Incident Reports be closed?

If (1) all Action Items are marked as complete and (2) there are no outstanding comments or questions that need to be addressed, CA Owners SHOULD clearly communicate in a Bugzilla comment when they believe an Incident Report can be closed. This is accomplished by writing a short-summary that includes:
- a description of the incident, its root cause(s), and remediation.
- a summary of all commitments made in response to the incident.
- an attestation that all Action Items have been completed.

CA Owners MUST use the template below when providing an incident closure summary.

```markdown
### Incident Report Closure Summary
- **Incident Description**: [A few sentences summarizing the incident.]
- **Incident Root Cause(s)**: [A few sentences summarizing the root cause(s).]
- **Remediation Description** [A few sentences summarizing the incident's remediation.]
- **Commitment Summary**: [A few sentences summarizing ongoing commitments made in response to this incident.]

All Action Items disclosed in this Incident Report have been completed as described, and we request its closure.

```

Upon completing the above, a final call for comments will be made by a Bugzilla moderator, and the incident closed no less than 7 days later.

### Incident Report Templates

The templates below describe the expected contents of an Incident Report. When responding to an incident, the latest version of these templates MUST be relied upon.

#### Preliminary Incident Report

```markdown
## Preliminary Incident Report

### Summary
<!---

**Expectations:**

- This section SHOULD clearly address the following:
     - **Incident description**: [A short description of the nature of the issue. This provides just enough context for new readers to understand the details of the incident.]
     - **Relevant policies**: [Describe the policies and corresponding sections that result in this problem being diagnosed as an incident.]
 
- If the report was created by the corresponding CA Owner, this section MUST also answer the following question:
     - **When is the Full Incident Report expected by?**: [DATE within 2 weeks of the incident’s initial disclosure (i.e., either to the CA Owner, or Bugzilla)]

-->
```

#### Full Incident Report

```markdown
## Full Incident Report

### Summary
<!---

**Expectations:**

 - This section MUST clearly address the following:
     - **Incident description**: [A short description of the nature of the issue. This provides just enough context for new readers to understand the details of the incident.]
     - **Relevant policies**: [Describe the policies and corresponding sections that result in this problem being diagnosed as an incident.]
     - **Source of incident disclosure**: [CHOICE of "Self Reported" OR "Third Party Reported"]

     NOTE: If notified of an incident by a Third Party Reporter, please respect their privacy by only disclosing their name if affirmativley approved to do so (i.e., use "We received a report from a community member" instead of explicitly naming individuals).
 
-->

### Impact
<!---

**Expectations:**

- The Impact Section MUST contain a description of the size and nature of the incident. For example: how many certificates, OCSP responses, or CRLs were affected; whether the affected objects share features (such as issuance time, signature algorithm, or validation type).
- If certificates are impacted, the Impact Section MUST address the following:
     - **Total number of certificates**: [if applicable, the total count of all certificates affected by the issue(s) described in this Incident Report, including expired and revoked certificates]
     - **Total number of "remaining valid" certificates**: [if applicable, the total count of certificates affected by the issue(s) described in this Incident Report, minus expired and revoked certificates. Minimally, this set of certificates MUST be disclosed in the Appendix section of this report.]
     - **Affected certificate types:** [A summary of the corresponding CA/Browser Forum policy OIDs (i.e., DV, IV, OV, and EV) that appear in the certificates affected by this incident (e.g., “This incident affects DV and OV certificates.”)]
     - **Incident heuristic:** [if applicable, EITHER:
          - (a) describe a heuristic that would allow a third party to assemble the full corpus of affected certificates, if not provided in the Appendix (e.g., "Any certificate containing policy OID 1.2.3.4.5.6 and issued between 11/13/2024 and 4/11/2024 is affected by this incident. Certificates that have been revoked or are expired are omitted from the certificate list disclosed in the Appendix."), 
          - (b) clearly explain why this isn't possible (e.g., "This incident affected every certificate issued between 5/25/2023 and 6/15/2024 that relied upon BR Validation Method 3.2.2.4.19. Because the relied upon validation method is not described in a certificate, this heuristic cannot be used by a third party to assemble the full corpus of affected certificates. Certificates that have been revoked or expired have been omitted from the certificate list disclosed in the Appendix.), or
          - (c) the full corpus of affected certificates are disclosed in the Appendix.]
     - **Was issuance stopped in response to this incident, and why or why not?:** [yes/no - explanation (e.g., "Yes. As described in the incident timeline, we stopped issuance after learning of this issue to correct the corresponding certificate profile.")]
     - **Additional Considerations:** [share any additional considerations that might be useful in describing the size and nature of the incident. For example, if the issue affected pre-certificates and "final" certificates differently, describe how and why in more detail here.]

-->

### Timeline
<!---

**Expectations:**

- The Timeline Section MUST include a detailed timeline of all events and actions leading up to and taken during and after the incident.
- The timeline MUST include not just the actual discovery of the incident and subsequent events, but also relevant events occurring beforehand (e.g., something changed or was introduced).
- All times MUST be in UTC OR UTC+local offset, and SHOULD have at least minute-level granularity.
- In addition, it MUST indicate the following events:
     - All policy, process, and software changes that contributed to the Root Cause(s)
     - The time at which the incident began
     - The time(s) at which the same failure mode was observed in other incidents disclosed in Bugzilla during the two years preceding this report
     - The time at which the CA Owner became aware of the incident
     - The time at which the CA Owner received a Certificate Problem Report (if applicable)
     - The time at which the CA Owner provided a preliminary report on its findings to the entity who filed the Certificate Problem Report (if applicable)
     - The time at which the CA Owner provided a preliminary report on its findings to the affected Subscriber(s) (if applicable)
     - The time at which the CA Owner concluded and disclosed the scope and impact of the incident
     - The time at which the CA Owner is expected to complete revocation of affected certificates (if applicable)
     - The time(s) at which the CA Owner actually completed revocation of affected certificates (if applicable) 
     - The time at which the incident ended
     - The times at which issuance ceased and resumed (if applicable)
-->

### Root Cause Analysis
<!---

**Expectations:**

- A root cause is defined as a factor that caused a nonconformance and SHOULD be permanently eliminated through process improvement.
- This section MUST contain a detailed analysis of the conditions which combined to give rise to the issue.
- It is unusual for an incident to have a single root cause; often there is a confluence of several issues such as a software bug, insufficient checks, and a malformed request.
- Make sure that all contributing causes are identified and described, including noting when they first arose and how they avoided detection until they were discovered or identified. 

**Preferred reporting format:**

#### Issue [#]: [Title]
- **Description:** [A detailed description of the specific issue.]
- **Issue Onset:** [Date when the issue began]
- **Issue Detection:** [Date when the issue was detected or otherwise made known]
- **Symptoms that Led to Detection**: [A detailed description of the circumstances that led to the detection of the issue.]
- **How the Issue Avoided Detection**: [A detailed description of how the issue was not detected earlier.]
- **Root Cause Analysis Methodology Used**([OPTIONAL, but RECOMMENDED]): [A description of the methodology used to derive the issue described above (e.g., "5-Whys", Fishbone Diagram, Pareto Analysis, etc.)]

-->

### Lessons Learned
<!---

**Expectations:** This section MUST answer the following questions:
- **What went well:** [a list of things that caused the incident to have less impact than it otherwise could have, such as early detection, rapid response, or good safety mechanisms. This section provides an opportunity for others to learn from the good practices of this CA Owner.]
- **What didn’t go well:** [a list of things that caused the incident to have more impact than it otherwise would have, such as missing checks or unclear documentation. Each item here MUST have at least one corresponding Action Item below and SHOULD provide opportunities for others to ensure they make similar improvements if they haven’t already.]
- **Where we got lucky:** [a list of things that went well, but which cannot be relied upon, such as early detection by an external security researcher or limited impact simply due to a small number of requests. Items here SHOULD generally also have corresponding Action Items, so that the CA Owner doesn’t have to rely on luck in the future.]

-->

### Action Items
<!---

**Expectations:**

- This section MUST contain a list of remediation items that will be undertaken to ensure that similar incidents do not reoccur in the future.
- Note that it is not sufficient for these action items to simply stop this incident, they MUST create additional protections to prevent future incidents.
- Each Action Item MUST state:
     - A detailed description of the action to be taken.
     - A classification of whether the action will help Prevent future incidents, Mitigate the impact of future incidents, or Detect future incidents. CA Owners are encouraged to propose action items in all three categories, with an emphasis on prevention and mitigation.
     - The specific Root Cause that the Action intends to remediate (i.e., each issue entry in the "Root Cause Analysis" and "What didn't go well" Sections MUST be mapped to at least one specific action item)
     - A date by which the action item will be complete.

| Action Item | Kind    | Corresponding Root Cause(s) | Due Date   |
| ----------- | ----    | --------------------------- | ---------- |
| Example     | Prevent | Root Cause # 1              | 2025-01-19 |

-->

### Appendix
<!---

**Expectations:**
- The Appendix is for all supporting data: log files, graphs and charts, etc.
- In particular, in the case of incidents that directly impact certificates, the Appendix MUST include a listing of the complete certificate details of all affected certificates.
- The recommended format is to ensure that all affected certificates are logged to CT, then to attach a text file where each line is of the form https://crt.sh/?sha256=[sha256 fingerprint of the pre-certificate].
- When the incident being reported involves an S/MIME certificate, if disclosure of personally identifiable information in the certificate MAY be contrary to applicable law, please provide at least the certificate serial number and SHA256 hash of the certificate.

-->

```

### Are there examples of “good" Incident Reports?

Here are some examples of good practice, where a CA Owner did most or all of the things recommended above:

- [Serving invalid or incomplete CRLs](https://bugzilla.mozilla.org/show_bug.cgi?id=1900129)
     - Clear Summary and Impact statements allow readers to quickly understand the scope of the incident
     - Detailed and thorough evaluation of existing safeguards that failed, allowing for an understanding of why the the incident was allowed to take place
     - Comments and questions from the community were responded to promptly.

- [keyCompromise key blocking deviation from CP/CPS](https://bugzilla.mozilla.org/show_bug.cgi?id=1886876)
     - Clear indication of Preliminary and Full Incident Reports.
     - Detailed timeline that identifies all policy, process, and software changes that contributed to the root cause, and an indication of when the incident began and ended.
     - Detailed Root Cause Analysis that offers background on the various conditions that gave rise to the issue.
     - Timely updates in response to questions posed, continued analysis, and changes to Action Items.
 
- [Failure to properly validate IP address](https://bugzilla.mozilla.org/show_bug.cgi?id=1876593)
     - Significant amount of background information that informs the timeline of the incident.
     - Clear identification of the contributing factors that contributed to the incident that notes how many of them avoided detection in the Root Cause Analysis.
     - Action Items that prevent, mitigate, and detect what didn’t go well.
     - Timely and detailed updates conveying Action Item status.
 
- [Anomaly in OCSP services after CA software upgrade](https://bugzilla.mozilla.org/show_bug.cgi?id=1878106)
     - Clear Summary that provides just enough context for new readers to understand the rest of the report.
     - Effective use of the “5 Whys” Root Cause Analysis methodology where “why” is asked as many times as necessary to identify the root cause of the incident.
     - Action Items that prevent and detect what didn’t go well.
     - Timely updates in response to questions posed and changes to Action Items.
 
  Upon adoption of the updated Incident Report templates above, examples of good practice will be updated.
