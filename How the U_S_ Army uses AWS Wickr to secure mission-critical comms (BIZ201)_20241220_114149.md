# Summary of AWS re_Invent 2024 - How the U_S_ Army uses AWS Wickr to secure mission-critical comms (BIZ201).txt

# AWS re:Invent 2024 - How the U.S. Army uses AWS Wickr to secure mission-critical comms

## Summary

### Importance of Secure Communications

- Secure communications are crucial for the U.S. Army due to the growing threat landscape, including targeted intrusions from nation-states and adversaries trying to gain unauthorized access to conversations.
- End-to-end encryption, server compromise defense, and endpoint management are essential defenses against evolving threats that target data, metadata, and traffic patterns.

### Wickr: A Secure Collaboration Suite

- Wickr is a secure collaboration suite that offers end-to-end encrypted messaging, audio/video calls, file sharing, screen sharing, and location sharing.
- It provides enterprise management capabilities like SSO, user and policy management, and data retention in a location of the customer's choice.
- Wickr is designed to be digitally sovereign, allowing customers to deploy it in their own regions while enabling cross-boundary communication.

### Key Features and Capabilities

- **Ephemeral Messaging**: Messages can be set to self-destruct after a specified time or after being read, ensuring data doesn't persist on endpoints.
- **Administrative Controls**: Granular controls over user access, permissions, and data policies.
- **Wickr Open Access**: Traffic obfuscation feature that masks Wickr traffic as regular AWS traffic, preventing threat actors from identifying and targeting Wickr communications.
- **Secure File Sharing**: Files shared within Wickr can be configured to be viewable only within the app, preventing unauthorized downloads.
- **Bots and Workflows**: Customers can integrate Wickr with their existing systems and workflows using bots and APIs, enabling advanced use cases like telemedicine triage and emergency response.
- **Language Translation**: Customers can integrate their own translation models or use Amazon Translate for secure, customer-owned translation services within Wickr.

### U.S. Army Use Cases

- **Mission Collaboration**: Wickr enables secure communication between U.S. Army personnel, foreign partners, and allies during joint exercises and operations.
- **Classified Communications**: Wickr's secure architecture and flexible deployment options make it suitable for classified communications, even in disconnected or tactical edge environments.
- **Bring Your Own Device (BYOD)**: Wickr allows soldiers to use personal devices for basic communications while providing elevated capabilities on managed devices with stricter security policies.
- **Emergency Response**: Bots and workflows integrated with Wickr have significantly reduced response times for emergency situations like medical evacuations and disaster relief efforts.

### Deployment Options

- **AWS Wickr**: A cloud-native SaaS offering managed by AWS, available in GovCloud and 10 commercial regions, with authorizations up to IL5 in the U.S. and IRAP, C5 internationally.
- **Wickr Enterprise**: An on-premises version that can be deployed on private networks, radio networks, satellite networks, and other disconnected environments.

## Key Insights and Conclusions

- Secure communications are a critical requirement for the U.S. Army, and Wickr provides a comprehensive solution that addresses evolving threats while enabling seamless collaboration and mission-critical use cases.
- Wickr's end-to-end encryption, data sovereignty, and advanced security features like Wickr Open Access and ephemeral messaging ensure data protection and identity privacy, even in adverse scenarios.
- The flexibility of Wickr's deployment options, integration capabilities, and enterprise management features make it suitable for a wide range of use cases, from basic communications to classified operations and emergency response.
- The U.S. Army's successful adoption of Wickr demonstrates its ability to meet stringent security requirements while providing a user-friendly experience that facilitates collaboration and improves operational efficiency.