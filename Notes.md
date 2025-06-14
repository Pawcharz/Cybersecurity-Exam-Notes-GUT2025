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
    - Data tampering: Unauthorized modification of data
    - Unauthorized modifications
    - Data corruption: Accidental or malicious alteration of data

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

### 1.2 Information Security Scope
Information security extends beyond IT assets to include all forms of information:

- **Physical Assets**
  - Paper documents
  - Physical records
  - Storage media

- **Intellectual Property**
  - Patents
  - Trade secrets
  - Copyrighted materials
  - Research data

- **Organizational Information**
  - Employee records
  - Financial data
  - Technical reports
  - Policies and procedures
  - Guidelines and documentation

## 2. Access Control

### 2.1 Access Control Types

- **DAC (Discretionary Access Control)**
  - Definition: Access control based on the identity of users and/or groups
  - Characteristics:
    - Owner-controlled access: Resource owners can modify access permissions
    - Flexible and user-friendly: Easy to implement and manage
    - Uses access control lists (ACLs): Explicit lists defining who can access what
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
  - Definition: Process of verifying the identity of a user
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
  - Definition: Uses the same key for encryption and decryption
  - Characteristics:
    - Faster than asymmetric: More efficient for bulk data encryption
    - Requires secure key exchange: Challenge of securely sharing the secret key
    - Examples: AES (Advanced Encryption Standard), DES (Data Encryption Standard), 3DES (Triple DES)
  - Key Management:
    - Secure key distribution: Methods for safely sharing keys between parties
    - Key storage: Protection of keys when not in use
    - Key rotation: Regular replacement of keys to maintain security

- **Asymmetric Cryptography**
  - Definition: Uses public/private key pairs
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

- **Components**
  - Knowledge base
  - Data gathering devices
  - Configuration component
  - Analysis engine
  - Alert system

## 5. Risk Management

### 5.1 Risk Assessment
Risk assessment is the process of identifying, analyzing, and evaluating potential risks to an organization's information assets. It helps organizations understand their security posture and make informed decisions about risk mitigation strategies.

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
Security controls are safeguards or countermeasures designed to protect information systems and data from security threats. They can be technical, administrative, or physical in nature.

- **Organizational Controls**
  - Information security organization: Structured approach to managing security
  - Asset management: Systematic tracking and protection of organizational assets
  - Compliance: Adherence to relevant laws, regulations, and standards
  - Change management: Controlled process for implementing system changes
  - Working in secure areas: Physical security measures for sensitive operations
  - Asset handling: Procedures for managing sensitive information
  - Information security roles: Defined responsibilities for security personnel

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
  - Vital societal functions: Essential services that maintain societal operations
  - Health services: Medical care and public health systems
  - Safety systems: Emergency response and public safety infrastructure
  - Security systems: National and local security operations
  - Economic systems: Financial and economic infrastructure
  - Social services: Essential public services and support systems

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
