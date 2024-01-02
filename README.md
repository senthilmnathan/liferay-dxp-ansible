**This contains code that can be used to deploy liferay DXP stack using Ansible.**

*The contents comprise of*

1. Instrastructure
1. Portal

- Infrastructure
   - This folder contains the ansible roles that deploys tasks requiring privileged root access. There are three roles in total.
      - liferay_application_infrastructure
      - liferay_elasticsearch_infrastructure
      - liferay_web_infrastructure
  - This folder also contains the wrapper ansible code required for Ansible project
      - liferay-infrastructure-platform
- Portal
    -  This folder contains the ansible role used to deploy liferay DXP on application servers. The role is liferay_application_portal
    -  The wrapper ansible code that ties up the above role is also added
      - liferay_portal_platform

```mermaid
graph TD
subgraph X [GIT Repository]
  A[liferay_application_infrastructure]
  B[liferay_web_infrastructure]
  C[liferay_elasticsearch_infrastructure]
  D[liferay-infrastructure-platform]
  E[liferay_application_portal]
  F[liferay-platform-platform]
end
subgraph Y [Ansible Tower]
  G[Infrastructure Project]    
  H[Portal Project]
end
D ---> G
F ---> H
style X fill:#f9f,stroke:#333,stroke-width:4px
style Y fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5
style A fill:#f90,stroke:#333,stroke-width:4px
style B fill:#f90,stroke:#333,stroke-width:4px
style C fill:#f90,stroke:#333,stroke-width:4px
style D fill:#f90,stroke:#333,stroke-width:4px
style E fill:#290,stroke:#333,stroke-width:4px
style F fill:#290,stroke:#333,stroke-width:4px
style G fill:#f90,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5
style H fill:#290,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5
```
