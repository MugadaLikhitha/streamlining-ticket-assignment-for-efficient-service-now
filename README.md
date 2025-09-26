# Streamlining Ticket Assignment for Efficient Support Operations ServiceNow

This project implements a structured and automated approach to streamline ticket assignment in **ServiceNow**.
It ensures issues are routed to the correct groups automatically, reducing manual effort and improving turnaround time.

## 📋 Overview

Service requests often involve repetitive manual assignment of tickets, which can delay resolution and introduce errors. This project introduces a systematic workflow that:

- Defines users, groups, and roles for access management  
- Creates a custom table to track operations-related issues  
- Implements secure access through roles and ACLs  
- Automates ticket routing using Flow Designer  


## 🎯 Objectives

- Establish clear user, group, and role structures  
- Secure custom data tables with proper access controls  
- Automate issue assignment to the right teams  
- Reduce manual intervention and enhance service efficiency  


## ✨ Key Features

### Users, Groups, and Roles Setup
- Created new **users** with unique details  
- Defined **groups** for access separation  
- Configured **roles** for platform and certification responsibilities  
- Linked users to appropriate groups and roles  


### Custom Table for Operations Issues
- Built a custom table `Operations Related` to track service issues  
- Enabled **Create module** and **mobile module** for accessibility  
- Defined structured fields and issue choices:
  - Unable to login to platform  
  - 404 Error  
  - Regarding certificates  
  - Regarding user expired  
- Configured table access restricted to **Platform** and **Certification** roles  


### Access Control Configuration
- Applied **ACLs** for role-based security  
- Restricted read/write operations to authorized roles  
- Used **elevated Security Admin role** for updates  
- Ensured granular control with field-specific ACLs  



### Flow Designer Automation
- Automated assignment of tickets based on issue type  
- **Flow 1 – Certificates Issues**  
  - Trigger: Create/Update record on `Operations Related` table  
  - Condition: Issue = Regarding Certificates  
  - Action: Assign to **Certificates Group**  

- **Flow 2 – Platform Issues**  
  - Trigger: Create/Update record on `Operations Related` table  
  - Conditions:  
    - Unable to login to platform  
    - 404 Error  
    - Regarding User expired  
  - Action: Assign to **Platform Group**  

- Saved and activated flows for seamless automation  


## 📦 Deliverables
- **Update Sets**: User, Group, Role, Table, ACL, and Flow Designer configurations  
- **Screenshots**: Captured for user/group/role creation, table design, ACL setup, and flow configuration  
- **Documentation**: Updated with implementation steps  


