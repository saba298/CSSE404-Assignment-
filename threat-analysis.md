# Threat Analysis Summary

**System Modeled**: Online University Course Registration System  
**Tool Used**: Microsoft Threat Modeling Tool  
**Threat Modeling Approach**: STRIDE 
---

## STRIDE Threats and Mitigations

| STRIDE Category          | Threat Example                                                  | Mitigation                                                                 |
|--------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------|
| **Spoofing**             | A malicious actor impersonates a student to gain access.         | Use **Multi-Factor Authentication (2FA)** and strong password policies.   |
| **Tampering**            | Unauthorized user modifies course registration records.         | Apply **role-based access control (RBAC)** and **input validation**.      |
| **Repudiation**          | A user denies dropping a course or changing selections.         | Implement **audit logs** with user ID, timestamps, and IP tracking.       |
| **Information Disclosure** | Sensitive data like student grades or schedules is leaked.     | Use **AES-256 encryption**, **HTTPS**, and **access control**.            |
| **Denial of Service (DoS)** | The system is overwhelmed during high-traffic registration days. | Implement **rate limiting**, **load balancing**, and **auto-scaling**.    |
| **Elevation of Privilege** | A student tries to access admin features or override limits.    | Enforce **least privilege** access design and **session validation**.     |

-------------------------

## Notes

- Each threat was detected automatically using the STRIDE model in the Microsoft Threat Modeling Tool.
- Default Microsoft mitigations (e.g., X.509 verification, ASP.NET defenses) were kept for completeness.

