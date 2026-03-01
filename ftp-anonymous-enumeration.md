# Misconfigured FTP Service — Anonymous Access Enumeration

## Objective

The goal of this lab was to practice service enumeration and understand how insecure configurations can expose sensitive information without requiring exploitation.

---

## Methodology

The approach followed a structured methodology:

1. Identify exposed services
2. Analyze service behavior
3. Test authentication mechanisms
4. Enumerate accessible data
5. Assess potential impact

---

## Enumeration

Initial reconnaissance was performed to discover open ports and running services on the target system.

An FTP service was identified as publicly accessible. Since FTP commonly suffers from weak or misconfigured authentication controls, it became the primary focus of analysis.

Rather than assuming a software vulnerability, the investigation centered on verifying access control configuration.

---

## Service Analysis & Interaction

A connection to the FTP service was established successfully.

Authentication testing revealed that the service permitted interaction without valid credentials. This behavior indicated a configuration weakness rather than an exploit.

Once access was confirmed, accessible resources were enumerated to determine what information an unauthenticated user could retrieve.

Available files were listed, retrieved locally, and analyzed in order to evaluate potential exposure.

No brute force attempts or exploitation techniques were required.  
Access was gained purely due to insecure service configuration.

---

## Findings

The FTP service allowed unauthenticated users to access internal data.

This represents an **information disclosure vulnerability** caused by misconfiguration.

Impact:

- Exposure of internal user-related information  
- Increased reconnaissance capability for attackers  
- Potential groundwork for future targeted attacks  

---

## Key Takeaways

- Enumeration is the foundation of offensive security
- Not all security issues require exploitation — misconfigurations are common and dangerous
- Services should never allow anonymous access unless absolutely necessary
- Information gathering is a critical phase in real-world attack scenarios

---

## Mitigation Recommendations

- Disable anonymous FTP login
- Enforce authentication mechanisms
- Apply strict file permission controls
- Monitor externally exposed services regularly
- Conduct periodic configuration audits

---

## Conclusion

This exercise reinforced the importance of service enumeration and configuration assessment.

Security weaknesses often arise not from complex exploits, but from overlooked configuration mistakes that silently expose sensitive information.


---

## Note

This write-up intentionally omits sensitive outputs and exact results.
The purpose is to demonstrate methodology and reasoning rather than provide direct solutions.

