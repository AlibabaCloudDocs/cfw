# \[Virtual patch\] User privilege escalation vulnerability in Kubernetes \(CVE-2018-1002105\)

Kubernetes is commonly stylized as K8s, which is an abbreviation derived by replacing the eight letters "ubernete" with an 8. K8s is an open-source system for managing containerized applications across multiple hosts deployed on the cloud platform.

With a specially crafted request, a normal K8s user who has established a connection through the K8s API server to a backend server can perform privilege escalation. To do so, the normal user must have the exec/attach/portforward permissions on at least one pod. The attacker can then send arbitrary requests over the established connection directly to that backend server to gain full admin privileges \(including root privileges\) on all nodes in a K8s cluster.

Servers using affected K8s versions are at high risk of intrusions. We recommend that you enable [intrusion prevention policies](/intl.en-US/Intrusion prevention/Intrusion prevention.md) in the Cloud Firewall console.

Rule type: Command execution

Risk level: High

Scope of impact:

-   Kubernetes v1.0.x to 1.9.x
-   Kubernetes v1.10.0 to 1.10.10 \(fixed in v1.10.11\)
-   Kubernetes v1.11.0 to 1.11.4 \(fixed in v1.11.5\)
-   Kubernetes v1.12.0 to 1.12.2 \(fixed in v1.12.3\)

Rule-based defense: A virtual patch is available in the Cloud Firewall console to defend against this vulnerability.

