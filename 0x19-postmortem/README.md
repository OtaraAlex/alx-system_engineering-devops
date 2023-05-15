# Postmortem

## Issue Summary
* **Duration:**
May 10, 2023, 10:00 PM (EAT) to May 11, 2023, 2:00 AM (EAT)

* **Impact:**
The main service experienced a complete outage during the specified duration. Users were unable to access the service, resulting in a 100% user impact.

## Timeline
+ **Issue Detected:** May 10, 2023, 10:15 PM (EAT)
+ **Detection Method:** An engineer received a monitoring alert indicating a service disruption.
+ **Actions Taken:** The engineering team began investigating the issue and focused on the database infrastructure as the initial assumption for the root cause.
+ **Misleading Investigation/Debugging Paths:** The team initially suspected a database failure due to a recent configuration change, leading them to spend significant time investigating database-related issues.
+ **Escalation:** As the incident persisted, it was escalated to the senior engineering team and the operations manager for further assistance and coordination.
+ **Resolution:** After thorough analysis and collaboration, the incident was resolved by identifying and addressing a networking misconfiguration.

## Root cause and Resolution
+ **Root Cause:** The root cause of the service outage was identified as a misconfigured network switch, which caused a disruption in the network connectivity between different components of the system. This resulted in the service becoming inaccessible.

+ **Resolution:** To resolve the issue, the misconfiguration in the network switch was rectified, restoring proper connectivity. The network switch settings were adjusted to align with the required network topology, ensuring uninterrupted service availability.

## Corrective And Preventative Measures
* **Improvement/Fixes:**
+ Strengthen network infrastructure monitoring: Implement additional monitoring tools to proactively detect and alert for network connectivity issues.
+ Automated configuration management: Develop an automated system for managing network configurations to minimize the risk of manual misconfigurations.
+ Enhanced incident response protocol: Revise the incident response protocol to include specific steps for investigating and resolving network-related issues promptly.

* **Tasks to Address the Issue:**
+ Perform a thorough review of the network topology and identify any other potential misconfigurations.
+ Conduct a comprehensive audit of all network switches to ensure alignment with best practices and system requirements.
+ Enhance network monitoring capabilities to capture real-time insights into network health.
+ Implement automation for network configuration management to reduce the likelihood of human errors.
+ Conduct training sessions for the engineering team on effective incident response and debugging techniques for network-related incidents.

By implementing these measures, we aim to prevent future incidents stemming from network misconfigurations and improve the overall reliability and resilience of our services.

In conclusion, the service outage was caused by a misconfigured network switch. Although the incident resulted in a complete service outage, it was promptly detected and resolved by the engineering team. Moving forward, we will implement corrective measures to prevent similar incidents and enhance the overall stability of our services.
