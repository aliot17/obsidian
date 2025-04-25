* **[[End-to-End Encryption Protocols]]** (E2EE) Protocols that ensure only the sender and recipient(s) can decrypt the messages, protecting against eavesdropping by intermediaries. E2EE encrypts data directly on the sender's device and remains encrypted until it reaches the intended recipient's device, ensuring that no intermediary, including service providers, can access the unencrypted content. [27, 28, 29, 30, 31]
	- **[[Signal Protocol]]** A cryptographic protocol providing [[End-to-End Encryption Protocols|end-to-end encrypted messaging]] end-to-end encrypted messaging for text, voice, and video calls, known for its apparently strong security properties. Widely adopted by applications such as [[Signal]], [[WhatsApp]], and others, it offers end-to-end encryption by default for all forms of communication. [49, 53, 54, 55, 56]
		* **[[Double Ratchet]]** A key management algorithm at the core of the [[Signal Protocol]] that provides forward secrecy and post-compromise security through continuous key derivation. It ensures that past messages remain secure even if long-term keys are compromised (forward secrecy) and future messages are secure even if a session key is compromised (post-compromise security). [56]
			* **[[Symmetric-key ratchet]]** A component of the Double Ratchet that uses a shared symmetric key to generate a sequence of new message keys.
			* **[[Asymmetric ratchet (public-key ratchet)]]** A component of the Double Ratchet that uses [[Diffie-Hellman (DH)|Diffie-Hellman] key exchanges to establish new shared secrets, driving the symmetric-key ratchet forward.
		- **[[X3DH (Extended Triple Diffie-Hellman)]]** The initial key exchange protocol used in [[Signal]] to establish a shared secret root key using long-term, medium-term, and ephemeral [[Diffie-Hellman (DH)|Diffie-Hellman]] keys. It's utilized for the initial agreement on a shared secret key between communicating parties in the [[Signal Protocol]]. [56]
		- **[[ProScript]]** A JavaScript implementation or variant of the [[Signal Protocol]]. 
		- **[[Sealed Sender]]** A feature in the [[Signal Protocol]] that aims to conceal the sender's identity from the server by encrypting metadata with the recipient's identity key, adding an extra layer of anonymity to communications. [54, 58]
		- **[[PQXDH (Post-Quantum Extended Diffie-Hellman)]]** A [Kyber](https://en.wikipedia.org/wiki/Kyber "Kyber")-based [[Post-Quantum Cryptography]] upgrade to the [[Diffie-Hellman (DH)|Diffie-Hellman key exchange]] introduced in the [[Signal Protocol]] aimed at providing resistance against attacks from quantum computers, representing a proactive approach to address future threats. [56]
	- **[[Messaging Layer Security (MLS)]]** A protocol standard designed to provide secure end-to-end group messaging with features like confidentiality, integrity, and authenticity. It represents an ongoing evolution of secure communication protocols, particularly for enhancing security and privacy features in group messaging. [95]
		- **[[TreeKEM]]** An asynchronous decentralised key management scheme, used within MLS for managing keys in dynamic groups using a tree structure.

* **[[XMPP (Extensible Messaging and Presence Protocol)]]** An open standard for real-time, extensible messaging and presence, upon which many instant messaging applications and services are built, allowing for various security extensions.
	* **[[Multi-User Chat (MUC/MIX) (XMPP)]]** An [[XMPP (Extensible Messaging and Presence Protocol)|XMPP]] protocol extension that enables group chat functionalities with potentially varying levels of security depending on implemented extensions like [[OMEMO (XMPP Extension Protocol XEP-0384)|OMEMO]].
	* **[[OMEMO (XMPP Extension Protocol XEP-0384)]]** An extension to the [[XMPP (Extensible Messaging and Presence Protocol)|XMPP]] protocol that provides multi-end-to-end encryption capabilities for instant messaging.

* **[[OTR (Off-the-Record)]]** A cryptographic protocol providing secure two-party conversations with encryption, authentication, deniability, and perfect forward secrecy.
	* **[[GOTR (Group OTR)]]** Extensions of the OTR protocol intended for secure group conversations.
	* **[[GOTR (2007)]]** An early version of Group OTR that uses a trusted relay server with pairwise OTR connections.
	* **[[GOTR (2013)]]** A later version of the Group OTR protocol. (No specific description in the sources).
	* **[[mpOTR (Multi-Party OTR)]]** Another extension of OTR aimed at securing conversations with more than two participants. (No specific description in the sources).

* **[[TextSecure Protocol]]** The cryptographic protocol developed by Open Whisper Systems that served as the basis for the [[Signal Protocol]].

* **[[Axolotl Ratchet]]** The key management algorithm used in the TextSecure Protocol, the precursor to the Double Ratchet.

* **[[iMessage Protocol]]** The proprietary messaging protocol used by Apple's iMessage service. Provides end-to-end encryption for messages exchanged between Apple devices by default, but messages sent to non-Apple devices typically fall back to less secure SMS/MMS protocols. [75, 25]
	* **[[iMessage PQ3 protocol]]** A specific version or security enhancement within the Apple iMessage protocol. 

* **[[Silent Circle Protocol]]** The proprietary encryption protocol used by the secure communications platform Silent Circle.

* **[[Pond Protocol]]** A secure messaging protocol that focuses on metadata privacy and leverages [[Onion Routing + Message Padding (e.g., Tor)|Tor]] hidden services.

* **[[SIMPP (Secure Instant Messaging Protocol Package)]]** A protocol designed for secure instant messaging.

* **[[IMKE]]** A secure messaging protocol that uses a central server to facilitate the exchange of ephemeral keys.

* **[[((n+1)sec protocol)]]** A protocol that provides Distributed Group Key Establishment (DGKE) and includes mechanisms to verify transcript consistency.

* **[[ASMesh]]** A secure messaging protocol. 

* **[[TLS (Transport Layer Security)]]** A cryptographic protocol that provides secure communication over a network, often used to secure web traffic (HTTPS). TLS establishes a secure communication channel between a client application and a server, ensuring the privacy and integrity of data exchanged over computer networks. It provides encryption of transmitted data, facilitates authentication of communicating parties, and incorporates mechanisms for data integrity. [36, 37, 38, 39, 41]
	* **[[TLS 1.3]]** A more recent and secure version of the Transport Layer Security protocol. It offers significant improvements in both performance and security compared to older versions. [36, 44]

* **[[TCPCrypt]]** A tool or protocol for adding opportunistic encryption to TCP connections.

* **[[ZRTP]]** A cryptographic key-agreement protocol used in VoIP to establish secure communication channels using short authentication strings (SAS).

* **[[SafeSlinger]]** A protocol for secure key exchange and messaging that uses short authentication strings (out-of-band) for verification.

* **[[S/MIME]]** A standard for encrypting and digitally signing email messages using public-key cryptography and often relying on Certificate Authorities.

* **[[Matrix Protocol]]** An open standard and communication protocol designed for real-time communication, with a primary goal of enabling interoperability between different messaging systems through a decentralized architecture. Unlike centralized messaging platforms, Matrix employs a federated model where multiple independent servers (known as homeservers) can communicate with each other, allowing users to choose their service provider while still being able to interact with users on other servers. [62, 64]
	* **[[Olm/Megolm Protocol]]** The [[End-to-End Encryption Protocols|end-to-end encryption]] cryptographic protocols used by the [[Matrix Protocol|Matrix]] open-source decentralized communication platform. The Olm library provides for optional end-to-end encryption on a room-by-room basis via a [[Double Ratchet]] Algorithm implementation. It can ensure that conversation data at rest is only readable by the room participants. With it configured, data transmitted over Matrix is only visible as ciphertext to the Matrix servers, and can be decrypted only by authorized participants in the room. Megolm is an expansion of Olm to better suit the need for bigger rooms.  [62]

* **[[Group Key Agreement (GKA) protocols]]** Cryptographic protocols that allow a group of participants to establish a shared secret key.

* **[[Distributed Group Key Establishment (DGKE) protocols]]** Protocols that enable a group of users to establish a shared secret key in a distributed manner, without a central trusted authority.

* **[[Metadata-Protecting Communication Systems (MPCS)]]** Communication systems designed to protect metadata associated with communications, such as sender, receiver, and timing, from network adversaries. This is crucial as metadata can reveal highly sensitive information about users' relationships, daily routines, habits, and locations, even when the content of a message is protected by strong encryption. [8, 9, 80]
	* **[[Anonymous Broadcast]]** A type of [[Metadata-Protecting Communication Systems (MPCS)|MPCS]] where the sender of a broadcasted message is protected from being identified by network observers.
	* **[[End-to-End Messaging (E2E)]]** In the context of [[Metadata-Protecting Communication Systems (MPCS)|MPCS]], systems that aim to protect the communication relationships between users, hiding who is communicating with whom.
	- **[[Sender Unlinkable Messaging Systems (SUMS)]]** [[Metadata-Protecting Communication Systems (MPCS)|MPCS]] that aim to prevent a message from being linked to its sender.
	* **[[Sender Unlinkable Broadcast Systems (SUBS)]]** [[Metadata-Protecting Communication Systems (MPCS)|MPCS]] designed to provide anonymity for senders in broadcast scenarios.
	* **[[Relationship Unobservable Systems (RUS)]]** [[Metadata-Protecting Communication Systems (MPCS)|MPCS]] that aim to conceal the fact that a communication is taking place between specific users.
	* **[[Receiver Unlinkable Messaging Systems (RUMS)]]** [[Metadata-Protecting Communication Systems (MPCS)|MPCS]] that aim to prevent a message from being linked to its intended recipient.
	* **[[Communication Unobservable Systems (CUS)]]** [[Metadata-Protecting Communication Systems (MPCS)|MPCS]] that aim to hide even the existence of a communication event.
	
- **[[Transport Privacy Protocols]]** Protocols that operate at the transport layer to hide metadata about communication, such as sender, receiver, and conversation.

* **[[Store-and-Forward]]** A basic message delivery mechanism where messages are held by intermediate servers and then forwarded to the recipient. Used by email and basic text messaging.

* **[[DHT Lookup (e.g., Kademlia)]]** Distributed Hash Table protocols used for peer discovery and routing in decentralized networks.

* **[[Onion Routing + Message Padding (e.g., Tor)]]** A technique that routes communication through multiple encrypted layers (like an onion) and uses padding to obscure message length, enhancing anonymity.

* **[[Hidden Services (e.g., Ricochet, Pond)]]** Services within anonymity networks like [[Onion Routing + Message Padding (e.g., Tor)|Tor]] that do not reveal their network address, providing privacy for both the service and its users.

* **[[Inbox Servers]]** A messaging model where messages are delivered to a personal inbox on a server, potentially offering some level of privacy through indirection.

* **[[Random Delays (e.g., Mixminion)]]** A technique used in mix networks to introduce random delays in message forwarding to prevent timing analysis and improve anonymity.

* **[[DC-Nets]]** Dining Cryptographers Networks, a cryptographic protocol that enables anonymous broadcasting within a group.
	* **[[Silent Rounds (e.g., Anonycaster)]]** A more efficient variant of [[DC-Nets]] that aims to reduce communication overhead.
	* **[[Shuffle-Based DC-Net + Leader]]** A [[DC-Nets|DC-Net]] construction that uses shuffling of messages and a designated leader node.
	* **[[Shuffle-Based DC-Net + Anytrust Servers (e.g., Verdict)]]** A [[DC-Nets|DC-Net]] variant that employs shuffling and relies on a set of servers that are not necessarily fully trusted.

* **[[Message Broadcast]]** A communication method where a message is transmitted to all participants in a network or group.

* **[[Blockchain]]** A distributed, immutable ledger that can be used to broadcast and record transactions or messages, with privacy implications depending on the specific implementation.

* **[[PIR (Private Information Retrieval) (e.g., Pynchon Gate)]]** Cryptographic techniques that allow a user to retrieve specific information from a database without revealing which information is being retrieved.

* **[[Continuous Key Agreement (CKA)]]** Key agreement protocols designed to continuously establish and update shared secret keys over time.
	* **[[Code-based CKA]]** A type of [[Continuous Key Agreement (CKA)||Continuous Key Agreement]] that uses error-correcting codes in its cryptographic construction, potentially offering resistance to quantum computer attacks.
	* **[[CKA combiner]]** A mechanism or protocol used to combine the outputs or states of multiple Continuous Key Agreement instances.

* **[[KleeQ]]** An early group chat protocol designed to maintain message causality over unreliable networks.

* **[[OldBlue]]** Another early group chat protocol focused on preserving the order of messages in group conversations despite network issues.
