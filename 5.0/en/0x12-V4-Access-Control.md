# V4 Access Control

## Control Objective

Authorization is the concept of allowing access to resources only to those permitted to use them. Ensure that a verified application satisfies the following high-level requirements:

* Persons accessing resources hold valid credentials to do so.
* Users are associated with a well-defined set of entitlements.
* Access control policy metadata is protected from replay or tampering.

## V4.1 General Access Control Design

| # | Description | L1 | L2 | L3 | CWE |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **4.1.1** | [MODIFIED] Verify that the application enforces access control rules at a trusted service layer and doesn't rely on controls which an untrusted user could manipulate such as client-side JavaScript. | ✓ | ✓ | ✓ | 602 |
| **4.1.2** | [MODIFIED] Verify that specific controls exist to prevent end users from making changes to access control policy information, such as user roles, permissions, and feature access levels, unless they are explicitly authorized to do so. | ✓ | ✓ | ✓ | 639 |
| **4.1.3** | Verify that the principle of least privilege exists - users should only be able to access functions, data files, URLs, controllers, services, and other resources, for which they possess specific authorization. This implies protection against spoofing and elevation of privilege. ([C7](https://owasp.org/www-project-proactive-controls/#div-numbering)) | ✓ | ✓ | ✓ | 285 |
| **4.1.4** | [DELETED, DUPLICATE OF 4.1.3] | | | | |
| **4.1.5** | [GRAMMAR] Verify that access controls fail securely by denying access, including when an exception occurs. ([C10](https://owasp.org/www-project-proactive-controls/#div-numbering)) | ✓ | ✓ | ✓ | 285 |

## V4.2 Operation Level Access Control

| # | Description | L1 | L2 | L3 | CWE |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **4.2.1** | Verify that sensitive data and APIs are protected against Insecure Direct Object Reference (IDOR) attacks targeting creation, reading, updating and deletion of records, such as creating or updating someone else's record, viewing everyone's records, or deleting all records. | ✓ | ✓ | ✓ | 639 |
| **4.2.2** | [MOVED TO 50.3.1] | | | | |

## V4.3 Other Access Control Considerations

| # | Description | L1 | L2 | L3 | CWE |
| :---: | :--- | :---: | :---: | :---: | :---: |
| **4.3.1** | [MODIFIED] Verify administrative interfaces can only be logically accessed from trusted endpoints or locations. For example, restricting access to bastion or jump hosts, trusted admin workstations or endpoints (e.g., device authentication), administrative LANs, etc. | ✓ | ✓ | ✓ | 419 |
| **4.3.2** | [SPLIT TO 14.3.4, 14.3.5] | | | | |
| **4.3.3** | [GRAMMAR] Verify the application has additional authorization (such as step up or adaptive authentication) for lower value systems, or alternatively segregation of duties for high value applications to enforce anti-fraud controls as per the risk of application and past fraud. | | ✓ | ✓ | 732 |

## References

For more information, see also:

* [OWASP Testing Guide 4.0: Authorization](https://owasp.org/www-project-web-security-testing-guide/v41/4-Web_Application_Security_Testing/05-Authorization_Testing/README.html)
* [OWASP Cheat Sheet: Access Control](https://cheatsheetseries.owasp.org/cheatsheets/Access_Control_Cheat_Sheet.html)
