# Active Directory Home Lab Project

### Project Overview
This project demonstrates how to build a comprehensive home lab environment to practice **Active Directory (AD)** management, security monitoring, and both **blue team** (defensive) and **red team** (offensive) cybersecurity tactics. By setting up and integrating various tools such as **Splunk** for monitoring, **Kali Linux** for attack simulations, and **Atomic Red Team** for telemetry generation, this lab provides a practical, hands-on learning experience.

### Objectives
- **Learn Active Directory Administration:** Build a fully functional AD environment with Windows Server 2022, complete with user management, domain setup, and machine integration.
- **Simulate Cybersecurity Attacks and Defenses:** Use Kali Linux for attack simulations like brute-force attacks on AD, while monitoring and analyzing telemetry through Splunk.
- **Gain SIEM Expertise:** Install and configure Splunk to detect security incidents, analyze logs, and create dashboards for better security visibility.
- **Enhance Problem-Solving Skills:** Troubleshoot issues that arise during setup and configuration of the lab components, mimicking real-world IT challenges.

---

### Project Components

#### 1. **Active Directory Setup**
  - **Windows Server 2022** is the core of this lab environment, hosting the AD domain controller. 
  - Managed and configured users, organizational units, and joined a target Windows machine to the domain.
  
#### 2. **Security Information and Event Management (SIEM)**
  - **Splunk** was deployed to ingest telemetry data from the AD server and target machine, allowing for real-time monitoring and detection of security incidents.
  - Configured Splunk to create alerts, dashboards, and reports based on the collected data.

#### 3. **Red Teaming Simulation**
  - Using **Kali Linux**, I performed brute-force attacks on the Active Directory setup to understand offensive techniques and how security events reflect on Splunk.
  - Ran **Atomic Red Team** to generate additional attack scenarios for further detection insights in Splunk.

---

### Tools and Technologies

- **Windows Server 2022**: Hosts Active Directory.
- **Windows 10 Pro**: A target machine added to the AD domain.
- **Kali Linux**: Used for red team exercises, simulating brute-force attacks and other offensive tactics.
- **Splunk (with Ubuntu Server)**: Acts as the SIEM, collecting logs and creating actionable security alerts.
- **VirtualBox**: Virtualization platform to manage VMs for the lab environment.
- **Atomic Red Team**: Open-source project to simulate attack techniques for red/blue team practice.

---

### Lab Setup & Configuration

- **Virtual Machine Configuration**: Hosted four VMs (Windows Server 2022, Windows 10 Pro, Ubuntu Server, Kali Linux) on VirtualBox with an additional two in the cloud.
  
- **Networking**: Configured a **NAT Network** within VirtualBox, allowing the VMs to communicate internally, and set static IPs for reliable network connections.

- **Active Directory Setup**: Promoted Windows Server 2022 to a domain controller, created users, and organizational units (OUs), and integrated target machines into the domain.

- **Splunk Configuration**: Installed and configured Splunk on the Ubuntu server, set up the **Splunk Universal Forwarder** on the Windows 10 Pro machine, and forwarded system, security, and application logs to the SIEM.

---

### Learning Outcomes

- **Active Directory Management**: Successfully set up an AD environment, including user management, security group configuration, and machine integration.
  
- **Splunk Mastery**: Installed, configured, and used Splunk to create custom dashboards, alerts, and reports for monitoring real-time security data.

- **Offensive and Defensive Cybersecurity Techniques**: Gained hands-on experience simulating attacks (brute-force, etc.) using **Kali Linux**, and analyzing telemetry data in **Splunk** to detect these attacks.

---

### Key Steps

- **Setting Up the Active Directory Domain**: 
  - Installed **AD Domain Services** on Windows Server 2022.
  - Promoted the server to a domain controller, added machines to the domain, and set up user accounts with appropriate organizational units (OUs).
  
- **Deploying Splunk as a SIEM**: 
  - Installed Splunk on an Ubuntu server to collect logs from the domain controller and target machine.
  - Created custom **Splunk dashboards** to monitor login attempts, security events, and other critical activities.

- **Executing Red Teaming Techniques**:
  - Used **Kali Linux** and the **Crowbar tool** to simulate brute-force attacks on AD’s Remote Desktop Protocol (RDP).
  - Deployed **Atomic Red Team** to execute real-world attack simulations for testing detection rules in Splunk.

---

### Conclusion

By completing this lab, I achieved a solid understanding of how to set up and manage an Active Directory environment, how to simulate and detect cybersecurity attacks, and how to use Splunk for effective security monitoring. This project mirrors real-world security operations and highlights both my technical proficiency and my problem-solving capabilities in managing and securing IT infrastructure.

---

### Future Improvements
- Integrating **additional attack simulations** using more advanced techniques.
- Implementing **incident response workflows** to automatically mitigate threats detected by Splunk.
- Enhancing reporting by linking **Sysmon logs** with detailed dashboards for better event visibility.
