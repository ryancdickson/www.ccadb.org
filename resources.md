# Useful Resources

## CCADB Support
* For problems or questions when using the CCADB, please contact support [at] ccadb [dot] org.
* You can record enhancements, bugs, and API access requests in the 'Common CA Database' [component](https://bugzilla.mozilla.org/enter_bug.cgi?product=CA%20Program&component=Common%20CA%20Database) under the 'CA Program' [product](https://bugzilla.mozilla.org/describecomponents.cgi?product=CA%20Program) in Bugzilla.

## CCADB Data

The [CCADB Data Usage Terms](rootstores/usage#ccadb-data-usage-terms) applies to all data hosted in and by the CCADB.

### Root Store Information

The Root Store Operators participating in the CCADB are described below, along with resources and reports that may be helpful to members of the community.

**It is crucial to understand** that each of these root stores is carefully managed for specific use cases and user communities. While the availability of root store reports and associated certificate bundles may seem convenient for re-use, re-purposing custom-built root stores for applications that do not perfectly align with their intended products, communities, or policies can introduce significant risks to security and interoperability. Such misuse can undermine the very protections these root stores are designed to provide. 

In most cases, it's far more appropriate and secure to curate a purpose-built root store tailored to satisfy the specific risk-based determinations of your corresponding user community. To assist user communities in establishing their own root stores, several additional reports are provided in the [Community Reports](#community-reports) section of this page. These can help you determine the set of roots most appropriate for your PKI use case and community goals, leading to a more secure and interoperable outcome compared to simply reusing a root store that you do not control.

#### Apple 

**Description:**  

**Policy:** [Apple Root Certificate Program](https://www.apple.com/certificateauthority/ca_program.html) 

**Additional Resources:** 
     
**Contact:** certificate-authority-program [at] apple [dot] com 

**Root Store Reports:** 

| PKI Use Case              | Downloads         | Note       |
| ------------------------- | ----------------- | ---------- |
| TLS Server Authentication | [CSV]() / [PEM]() |            |
| TLS Client Authentication | [CSV]() / [PEM]() |            |
| S/MIME                    | [CSV]() / [PEM]() |            |
| Timestamping              | [CSV]() / [PEM]() |            |


#### Cisco

**Description:**  

**Policy:** 

**Additional Resources:** 
     
**Contact:**  

**Root Store Reports:** 


#### Google Chrome 

**Description:** The Chrome Root Store launched in 2022 and is optimized _specifically_ for public TLS server authentication in the Chrome web browser when establishing secure connections to websites. Its design and the Certification Authorities (CAs) included are curated to meet these particular user needs, risk profiles, and security objectives. The canonical source of truth for the Chrome Root Store is [found](https://chromium.googlesource.com/chromium/src/+/main/net/data/ssl/chrome_root_store/) in the Chromium source code, and is later replicated to the CCADB. 

**Policy:** [Chrome Root Program Policy](https://g.co/chrome/root-policy)

**Additional Resources:** 
- [Moving Forward, Together](https://googlechrome.github.io/chromerootprogram/moving-forward-together/)
- [Chrome Root Store & Certificate Verifier FAQ](https://chromium.googlesource.com/chromium/src/+/main/net/data/ssl/chrome_root_store/faq.md)
     
**Contact:** chrome-root-program [at] google [dot] com

**Root Store Reports:** 

| PKI Use Case              | Downloads         | Note       |
| ------------------------- | ----------------- | ---------- |
| TLS Server Authentication | [CSV]() / [PEM]() | These downloads exclude [constrained](https://chromium.googlesource.com/chromium/src/+/main/net/data/ssl/chrome_root_store/faq.md#What-does-it-mean-for-a-certificate-in-the-Chrome-Root-Store-to-be-constrained) certificates. |


#### Microsoft

**Description:**  

**Policy:** [Trusted Root Program Requirements](https://aka.ms/RootCert)

**Additional Resources:** 
- [Trusted Root Certificate Program Updates](https://aka.ms/rootupdates)
- [Trusted Root Audit Requirements](https://aka.ms/auditreqs)
     
**Contact:** msroots [at] microsoft [dot] com

**Root Store Reports:**  

| PKI Use Case                   | Downloads         | Note       |
| ------------------------------ | ----------------- | ---------- |
| TLS Server Authentication      | [CSV]() / [PEM]() |            |
| TLS Client Authentication      | [CSV]() / [PEM]() |            |
| S/MIME                         | [CSV]() / [PEM]() |            |
| Timestamping                   | [CSV]() / [PEM]() |            |
| Code Signing                   | [CSV]() / [PEM]() |            |
| Document Signing               | [CSV]() / [PEM]() |            |
| Encrypting File System         | [CSV]() / [PEM]() |            |
| IP Security End System         | [CSV]() / [PEM]() |            |
| IP Security IKE Intermediate   | [CSV]() / [PEM]() |            |
| IP Security Tunnel Termination | [CSV]() / [PEM]() |            |
| IP Security User               | [CSV]() / [PEM]() |            |


#### Mozilla  

**Description:**  

**Policy:** [Mozilla Root Store Policy](https://www.mozilla.org/en-US/about/governance/policies/security-group/certs/policy/)

**Additional Resources:** 
- [Root Program Documentation](https://wiki.mozilla.org/CA)
- [CA Communications](https://wiki.mozilla.org/CA/Communications)
- [CA Incident Dashboard](https://wiki.mozilla.org/CA/Incident_Dashboard)
- [dev-security-policy WebPKI Forum](https://groups.google.com/a/mozilla.org/g/dev-security-policy)
     
**Contact:** certificates [at] mozilla [dot] org

**Root Store Reports:**  

| PKI Use Case              | Downloads         | Note       |
| ------------------------- | ----------------- | ---------- |
| TLS Server Authentication | [CSV]() / [PEM]() |            |
| S/MIME                    | [CSV]() / [PEM]() |            |


### Community Reports

#### Use-case Specific Reports

The following reports contain any root CA trusted for the given PKI use case by at least one CCADB root store operator. 

| PKI Use Case                   | Downloads         | Note       |
| ------------------------------ | ----------------- | ---------- |
| TLS Server Authentication      | [CSV]() / [PEM]() |            |
| TLS Client Authentication      | [CSV]() / [PEM]() |            |
| S/MIME                         | [CSV]() / [PEM]() |            |
| Timestamping                   | [CSV]() / [PEM]() |            |
| Code Signing                   | [CSV]() / [PEM]() |            |
| Document Signing               | [CSV]() / [PEM]() |            |
| Encrypting File System         | [CSV]() / [PEM]() |            |
| IP Security End System         | [CSV]() / [PEM]() |            |
| IP Security IKE Intermediate   | [CSV]() / [PEM]() |            |
| IP Security Tunnel Termination | [CSV]() / [PEM]() |            |
| IP Security User               | [CSV]() / [PEM]() |            |

#### Additional Reports
- [All Certificate Information (root and intermediate) in CCADB (CSV)](https://ccadb.my.salesforce-sites.com/ccadb/AllCertificateRecordsCSVFormatv2) ([Description](https://docs.google.com/document/d/1S3u0-_YACA7m-3LPpjE-t4WCh2cww_SQFh2C9DJeXHA/edit?usp=sharing) of report fields)
- [All Included Root Certificate Trust Bit Settings (CSV)](https://ccadb.my.salesforce-sites.com/ccadb/AllIncludedRootCertsCSV)
- [List of CA problem reporting mechanisms (email, etc.)](https://ccadb.my.salesforce-sites.com/ccadb/AllProblemReportingMechanismsReport) (use this to report a certificate problem directly to the CA)
     - [CSV List of CA problem reporting mechanisms (email, etc.)](https://ccadb.my.salesforce-sites.com/ccadb/AllProblemReportingMechanismsCSV)
- [List of CAA Identifiers](https://ccadb.my.salesforce-sites.com/ccadb/AllCAAIdentifiersReportV2) (used to restrict issuance of certificates to specific CAs via a [DNS Certification Authority Authorization Resource Record](https://tools.ietf.org/html/rfc6844))
     - [CSV List of CAA Identifiers](https://ccadb.my.salesforce-sites.com/ccadb/AllCAAIdentifiersReportCSVV2)
- [Accepted Roots for Production Certificate Transparency Logs](https://ccadb.my.salesforce-sites.com/ccadb/RootCACertificatesIncludedByRSReportCSV) (includes CAs trusted by at least one of the CCADB root stores)
- [Accepted Roots for Test Certificate Transparency Logs](https://ccadb.my.salesforce-sites.com/ccadb/RootCACertificatesInclusionReportCSV) (includes CAs that have applied to at least one of the CCADB root stores)
- [Disclosed Domain Control Validation Practices](https://ccadb.my.salesforce-sites.com/googlechrome/TLSCertDomainValidationCSVFormat)

### Additional Resources ###
- [crt.sh Certificate Search](https://crt.sh/)
- [Censys Certificate Search](https://censys.io/)
- [Certificate Explainer](https://tls-observatory.services.mozilla.com/static/certsplainer.html)
- [public@ccadb.org WebPKI Forum](https://groups.google.com/a/ccadb.org/g/public)
- [Trust Service Provider Technical Best Practices](/documents/TSP_Technical_Best_Practices_eIDAS.pdf)
- [Qualified Website Authentication Certificates (QWACs) Interoperability](/documents/Qualified_Website_Authentication_Certificates_Interoperability.pdf)
