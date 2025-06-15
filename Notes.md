# Cybersecurity Exam Study Guide

## 1. Information Security Fundamentals

### 1.1 CIA Triad
The CIA Triad is the fundamental model of information security:

- **Confidentiality**
  - Definition: Ensuring information is accessible only to those authorized to have access
  - Examples:
    - Encrypted data transmission
    - Password protection
    - Access control lists
  - Violations:
    - Unauthorized data access
    - Data leaks
    - Eavesdropping: Unauthorized interception of communications

- **Integrity**
  - Definition: Maintaining and assuring the accuracy and completeness of data
  - Examples:
    - Data validation
    - Checksums
    - Digital signatures
  - Violations:
    - Data tampering: Deliberate alteration of information without authorization ??
    - Ransomware attacks ??
    - Data corruption: Unintended or malicious data damage ??

- **Availability**
  - Definition: Ensuring authorized users have access to information when needed
  - Examples:
    - Redundant systems
    - Backup systems: Regular data backups to prevent data loss
    - Disaster recovery plans: Comprehensive strategies for system restoration
  - Violations:
    - Denial of Service (DoS): Attacks that prevent legitimate users from accessing systems
    - Distributed Denial of Service (DDoS): Coordinated attacks from multiple sources
    - Ransomware attacks: Malware that encrypts data and demands payment for access
    - System failures: Unexpected breakdowns in system operations

## 2. Access Control

### 2.1 Access Control Types

- **Access Monitors**
  - Definition: Security tools that track, log, and analyze access attempts to resources
  - Purpose:
    - Auditing: Record of who accessed what and when
    - Compliance: Meeting regulatory requirements
    - Security monitoring: Detecting suspicious activities
  - Implementation:
    - Operating systems: Track file and system access
    - Databases: Monitor data access and queries
    - Network devices: Log network access attempts
    - Applications: Track user activities
  - Used across all access control models:
    - DAC: Monitor discretionary access decisions
    - MAC: Track mandatory access control enforcement
    - RBAC: Monitor role-based access patterns

- **DAC (Discretionary Access Control)**
  - Definition: Access control based on the identity of users and/or groups, where resource owners have the authority to determine access permissions
  - Characteristics:
    - Owner-controlled access: Resource owners can modify access permissions
    - Flexible and user-friendly: Easy to implement and manage
    - Uses access control lists (ACLs): Explicit lists defining who can access what
    - Access control lists are utilized in: File systems, network devices, and operating systems to manage permissions
  - Implementation:
    - File permissions: Granular control over file access rights
    - User groups: Logical grouping of users with similar access needs
    - Access rights: Specific permissions granted to users or groups

- **MAC (Mandatory Access Control)**
  - Definition: Access control based on security labels and clearances, where the system enforces access decisions based on predefined security policies
  - Characteristics:
    - System-enforced: Access decisions are made by the system, not users
    - Hierarchical: Clear levels of security classification
    - Less flexible but more secure: Strict enforcement of security policies
  - Implementation:
    - Security classifications: Labels indicating the sensitivity of information
    - Clearance levels: Authorization levels for accessing classified information
    - Compartmentalization: Isolation of information based on security requirements

- **RBAC (Role-Based Access Control)**
  - Definition: Access control based on roles within an organization, where permissions are assigned to roles rather than directly to users
  - Characteristics:
    - Role-based permissions: Access rights tied to organizational roles
    - Scalable: Easy to manage in large organizations
    - Easy to manage: Simplified administration through role assignments
  - Implementation:
    - Role definitions: Clear specification of job functions and responsibilities
    - Permission assignments: Mapping of access rights to roles
    - User-role mapping: Assignment of users to appropriate roles

### 2.2 Authentication and Authorization

- **Authentication**
  - Definition: Process of verifying the identity of a user or system through various validation methods
  - **Identification vs Authentication**:
    - Identification: Process of claiming an identity (e.g., username)
    - Authentication: Process of proving the claimed identity (e.g., password)
  - Methods:
    - Something you know (passwords)
    - Something you have (tokens)
    - Something you are (biometrics)
  - Implementation:
    - Multi-factor authentication
    - Single sign-on
    - Password policies

- **Authorization**
  - Definition: Process of determining what resources and actions a user is permitted to access after successful authentication
  - Implementation:
    - Access control lists: Detailed permissions for specific resources
    - Role-based permissions: Access rights based on organizational roles
    - Policy enforcement: Systematic application of security policies

## 3. Cryptography

### 3.1 Basic Concepts

- **Key Length**
  - Definition: Number of bits in the binary representation of a cryptographic key
  - Importance:
    - Longer keys = stronger security
    - Minimum recommended lengths
    - Impact on performance

- **Keyspace**
  - Definition: The total number of possible keys in a cryptographic system
  - Examples:
    - Symmetric: 128-bit key has **2^128 possible combinations**
    - Asymmetric: 2048-bit RSA key has 2^2048 possible combinations

- **Communication Channels**
  - Definition: Methods and pathways for exchanging cryptographic information
  - Types:
    - Secure channels: Protected communication paths for sensitive data
    - Insecure channels: Public or untrusted communication paths
  - Requirements:
    - **Symmetric cryptography**: Requires **secure** channel for key exchange
    - **Asymmetric cryptography**: Public keys can be shared over **insecure** channels
  - Implementation:
    - Physical security: Direct, in-person key exchange
    - Secure protocols: TLS, SSH, or other secure communication methods
    - Key distribution centers: Centralized key management systems

- **Restricted Cryptographic Algorithm**
  - Definition: Algorithm whose security relies on keeping its design secret, rather than mathematical complexity
  - Characteristics:
    - Security through obscurity: Reliance on secrecy of the algorithm/code itself
    - Not recommended for general use: Lack of peer review and potential vulnerabilities
    - Limited peer review: Reduced ability to identify and fix security flaws

- **Cryptographic Naming Conventions**
  - Alice: Typically represents the sender in cryptographic protocols
  - Bob: Typically represents the intended receiver in cryptographic protocols
  - Eve: Typically represents an eavesdropper attempting to intercept communications
  - Used in cryptographic protocols and examples to illustrate security concepts

### 3.2 Cryptography Types

- **Symmetric Cryptography**
  - Definition: Uses the **same key** for encryption and decryption
  - Key Exchange:
    - Secure communication channel required
  - Characteristics:
    - Faster than asymmetric: More efficient for bulk data encryption
    - Requires secure key exchange: Challenge of securely sharing the secret key
    - Examples: AES (Advanced Encryption Standard), DES (Data Encryption Standard), 3DES (Triple DES)
  - Key Management:
    - Secure key distribution: Methods for safely sharing keys between parties
    - Key storage: Protection of keys when not in use
    - Key rotation: Regular replacement of keys to maintain security

- **Asymmetric Cryptography**
  - Definition: Uses **public/private key pairs**
  - Characteristics:
    - Slower than symmetric: More computationally intensive
    - No need for secure key exchange: Public keys can be freely shared
    - Examples: RSA (Rivest-Shamir-Adleman), ECC (Elliptic Curve Cryptography)
  - Implementation:
    - Public key distribution: Methods for sharing public keys
    - Private key protection: Security measures for private key storage
    - Digital signatures: Using private keys to sign messages for authenticity

## 4. Network Security

### 4.1 Firewalls
A firewall is a network security device that monitors and filters incoming and outgoing network traffic based on an organization's previously established security policies. It acts as a barrier between a trusted network and an untrusted network, such as the Internet.

- **Types of Firewalls**
  - Network-based:
    - Deployed between network zones: Acts as a barrier between different network segments
    - Hardware-based: Dedicated physical devices for network protection
    - Protects entire network: Provides centralized security for all network traffic
  - Host-based:
    - Software-based: Installed on individual systems
    - Protects individual hosts: Provides granular control at the system level
    - Not deployed between network zones: Focuses on protecting specific endpoints

- **Firewall Characteristics**
  - Rule-based filtering: Systematic application of security policies
  - Stateful inspection: Tracking of connection states for better security
  - Application layer filtering: Deep packet inspection for application-specific threats
  - Configuration importance: Critical role of proper firewall setup
  - Router integration: Coordination with network routing functions

### 4.2 Intrusion Detection Systems (IDS)
An Intrusion Detection System (IDS) is a security tool that monitors network or system activities for malicious activities or policy violations. It analyzes traffic patterns to identify potential security threats and generates alerts when suspicious activities are detected.

- **Does not have access monitors**
- **Types of IDS**
  - Network-based (NIDS):
    - Monitors network traffic
    - Detects network attacks
    - Focuses on communication events
  - Host-based (HIDS):
    - Monitors local system
    - Detects local attacks
    - Focuses on system events

- **Detection Methods**
  - Signature-based:
    - Known attack patterns
    - Lower false positive rate
    - Requires regular updates
  - Anomaly-based:
    - Behavioral analysis
    - Higher false positive rate
    - Detects unknown attacks
    - Advantages:
      - Can detect zero-day attacks
      - Adapts to changing patterns
      - No need for signature updates
    - Disadvantages:
      - Higher false positive rate
      - Requires extensive training
      - May miss known attacks

- **Components**
  - Knowledge base
  - Data gathering devices
  - Configuration component
  - Analysis engine
  - Alert system

## 5. Risk Management

### 5.1 Risk Assessment
Risk assessment is the process of identifying, analyzing, and evaluating potential risks to an organization's information assets. It helps organizations understand their security posture and make informed decisions about risk mitigation strategies.

- **Phases of Risk Management**
  - Risk assesment 1: **Risk Identification**:
    - Asset identification: Catalog all information assets
    - Threat identification: Identify potential threats to assets
    - Vulnerability assessment: Find weaknesses in systems
  - Risk assesment 2:**Risk Analysis**:
    - Impact assessment: Evaluate potential damage
    - Likelihood assessment: Determine probability of occurrence
    - Risk calculation: Combine impact and likelihood
  - Risk assesment 3: **Risk Evaluation**:
    - Risk prioritization: Rank risks by severity
    - Risk acceptance criteria: Define acceptable risk levels
    - Decision making: Choose appropriate responses
  - **Risk Treatment**:
    - Control selection: Choose appropriate security measures
    - Implementation: Deploy selected controls
    - Monitoring: Track effectiveness of controls

- **Impact Levels (FIPS 199)**
  - Low: Limited adverse effect on organizational operations, assets, or individuals
  - Moderate: Serious adverse effect on organizational operations, assets, or individuals
  - High: Severe or catastrophic adverse effect on organizational operations, assets, or individuals

- **Residual Risk**
  - Definition: The level of risk that remains after implementing security controls and risk mitigation strategies
  - Characteristics:
    - Can contain unidentified risk: Potential threats that were not discovered during assessment
    - Not increased during analysis: Risk assessment should not create new vulnerabilities
    - Not removed during evaluation: Some risk will always remain despite controls
  - Management:
    - Risk acceptance: Deliberate decision to accept certain levels of risk
    - Risk transfer: Shifting risk to another party (e.g., through insurance)
    - Risk avoidance: Eliminating activities that pose unacceptable risks

### 5.2 Security Controls

- **Definition and Types**
  - Security controls are safeguards or countermeasures designed to protect information systems and data from security threats
  - Can be technical, administrative, or physical in nature
  - Types:
    - Preventive controls: Stop security incidents before they occur
    - Detective controls: Identify security incidents when they occur
    - Corrective controls: Mitigate the impact of security incidents

- **Organizational Controls**
  - Information security organization: Dedicated security team with clear responsibilities
  - Asset management: Inventory and classification of all information assets
  - Compliance: Regular audits and documentation of compliance measures
  - Change management: Formal process for system changes with impact assessment
  - Working in secure areas: Access control and monitoring of sensitive areas
  - Asset handling: Secure storage and disposal procedures for sensitive data
  - Information security roles: Defined security officer and incident response duties

- **ICT Infrastructure and Protection**
  - Definition: **Information and Communication Technology (ICT)** infrastructure includes all hardware, software, networks, and data centers
  - Protection measures:
    - Physical security: Protection of physical assets
    - Network security: Protection of network infrastructure
    - Access control: Management of system access
    - Data protection: Safeguarding sensitive information
    - Backup systems: Ensuring data availability

## 6. Standards and Frameworks

### 6.1 International Standards

- **ISO/IEC 27001**
  - Information security management system: Framework for managing information security
  - Risk management approach: Systematic method for identifying and addressing risks
  - Continuous improvement: Ongoing enhancement of security measures

- **ISO/IEC 27002**
  - Best practices: Recommended approaches to information security
  - Security controls: Specific measures for protecting information
  - Implementation guidelines: Detailed instructions for applying controls

### 6.2 Government Standards

- **NIST SP 800-53**
  - Security control baselines: Standardized security measures for federal systems
  - Federal agency guidelines: Requirements for government information systems
  - Control families: Grouped security controls by function

- **FIPS 199**
  - Impact levels: Classification of security impact categories
  - Security categorization: Process of determining system security levels
  - Risk assessment: Framework for evaluating security risks

## 7. Critical Infrastructure

### 7.1 Definition and Scope

- **Critical Functions**
  - Vital societal functions: Power grid operations and maintenance
  - Health services: Hospital emergency departments and medical facilities
  - Safety systems: 911 emergency response systems
  - Security systems: Border control and immigration systems
  - Economic systems: Banking and financial transaction systems
  - Social services: Social security and welfare distribution systems

### 7.2 Impact of Disruption

- **Security Impact**
  - National security
  - Public safety
  - Economic security

- **Health and Safety**
  - Public health
  - Emergency services
  - Medical systems

## 8. Security Violations

### 8.1 Availability Violations

- **Types of Attacks**
  - Ransomware:
    - Encrypts data: Blocks access to critical information
    - Demands payment: Extorts money for data recovery
    - Blocks access: Prevents legitimate use of systems
  - DoS/DDoS:
    - Overwhelms systems: Floods resources with excessive traffic
    - Blocks legitimate access: Prevents authorized users from using services
    - Multiple attack sources: Coordinated attacks from various locations
  - Case Study: Zeus Attack (2010-2011)
    - Impact: Data erasure on infected hard disks
    - Violated attribute: Availability

### 8.2 Integrity Violations

- **Types of Violations**
  - Unauthorized modifications: Changes made without proper authorization
  - Data tampering: Deliberate alteration of information
  - Data corruption: Accidental or malicious data damage
  - System compromise: Unauthorized access to system functions

## 9. Organizational Security

### 9.1 Management Involvement

- **Current Challenges**
  - Insufficient management involvement
  - Unrealistic cost expectations
  - Lack of attention to ICT protection

- **Best Practices**
  - Management commitment
  - Resource allocation
  - Regular reviews
  - Security awareness

### 9.2 Security Controls

- **Types of Controls**
  - Information backup: Regular copying of critical data
  - Encryption: Protection of sensitive information
  - Access control: Management of system access
  - Monitoring: Continuous surveillance of systems
  - Incident response: Procedures for handling security events
  - Disaster recovery: Plans for system restoration

## 10. Usability in Cybersecurity

### 10.1 Definition and Principles
- Definition: The degree to which security measures can be effectively and efficiently used by users
- Key principles:
  - User-centered design: Security measures must align with user needs and behaviors
  - Security by default: Implement secure settings that require minimal user configuration
  - Clear communication: Security messages and alerts must be understandable

### 10.2 Assuring Usable Cybersecurity
- **User testing and feedback** (most important on exam):
  - Regular usability testing with actual users
  - Collect and implement user feedback
  - Monitor security measure adoption rates
- Security design guidelines:
  - Minimize user effort required for security tasks
  - Provide clear security status indicators
  - Use consistent security patterns across systems
- Training and support:
  - Regular security awareness training
  - Clear documentation and help resources
  - Ongoing user support for security features


## Costs
### Direct cost
- Costs of recovery

### Cost categorisation/calculation approaches:
- balance sheet oriented
- security measure lifecycle oriented
- IT security process oriented
- standard oriented approach
- ISMS-layer oriented


## Open Questions and examples

### Provide an example of a security control to reduce the risk of copying accounting data by unauthorised users.
- Access control lists (ACLs) that restrict copying permissions for accounting data to authorized personnel only

### Are there many (more than 10) information security risk assessment methods?
- Yes, there are many methods including:
  - Standard frameworks (OCTAVE, NIST, ISO 27005, FAIR, CRAMM, MEHARI, EBIOS, CORAS, TARA, ISAMM)
  - Industry-specific methods
  - Proprietary methodologies

## Qualitative risk assesment method
### Explain the systematic process of developing list of threats during risk assesment.
- Seeking threat lists from various sources until they start to repeat substantially
- keeping diferent coherent levels of abstraction