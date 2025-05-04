* **[[Symmetric Encryption]]** Encryption methods that use the same secret key for both encrypting and decrypting data. Algorithms such as the Advanced Encryption Standard (AES) are widely used for efficiently encrypting message content due to their speed and effectiveness. [2, 40]

* **[[AES-256]]** Advanced Encryption Standard with a 256-bit key length, a widely adopted symmetric block cipher known for its strong security.
	* **[[AES-256 in CBC mode with PKCS#5 padding]]** A specific mode of operation for AES-256 where each block of plaintext is XORed with the previous ciphertext block (Cipher Block Chaining) and padding is added to ensure the plaintext length is a multiple of the block size using the PKCS#5 standard. (Note: OMEMO uses PKCS#7 padding).

* **[[Forward-Secure Authenticated Encryption with Associated Data (FS-AEAD)]]** An authenticated encryption scheme that not only provides confidentiality and integrity for the message and associated data but also ensures that past encrypted messages remain secure even if the current encryption keys are compromised.

* **[[Key Derivation Functions (KDFs)]]** Cryptographic functions that take a secret value and derive one or more pseudorandom secret keys from it.

* **[[HMAC-SHA256]]** A specific type of Keyed-Hash Message Authentication Code that uses the SHA-256 hash function, often employed as a KDF by using a fixed secret and varying input to generate new keys.
	* **[[HKDF (HMAC-based Extract-and-Expand Key Derivation Function) using SHA256]]** A standardized KDF that uses HMAC-SHA256 as its underlying cryptographic primitive to first extract entropy from an input keying material and then expand it into one or more output keys of the desired length.

* **[[Digital Signature Schemes]]** Cryptographic schemes that provide a way to verify the authenticity and integrity of a digital message or document by allowing the signer to produce a unique signature that can be checked by others. They provide a way to verify the authenticity of a message sender and ensure non-repudiation, confirming that the sender cannot deny having sent the message. [6, 48]

* **[[EdDSA (Edwards-Curve Digital Signature Algorithm)]]** A modern public-key signature system that uses elliptic curves and is known for its security, performance, and resistance to certain side-channel attacks.
	*  **[[XEdDSA]]** A specific instantiation of the [[EdDSA (Edwards-Curve Digital Signature Algorithm)|EdDSA]] designed by [[Signal]] Project, optimized for efficiency and security. Creates and verifies EdDSA-compatible signatures using public key and private key formats initially defined for the X25519 and X448 elliptic curve [[Diffie-Hellman (DH)|Diffie-Hellman]] functions.
	* **[[VXEdDSA]]** An extension of the [[XEdDSA]] designed by [[Signal]] Project signature scheme to make it a _verifiable random function_, or VRF. Successful verification of a VXEdDSA signature returns a VRF output which is guaranteed to be unique for the message and public key. The VRF output for a given message and public key is indistinguishable from random to anyone who has not seen a VXEdDSA signature for that message and key.

* **[[Authenticated Encryption with Associated Data (AEAD)]]** Encryption schemes that simultaneously provide confidentiality for the data and integrity and authenticity for both the data and associated (non-encrypted) metadata.
	* **[[Encrypt-then-MAC]]** A method for constructing an AEAD scheme where the plaintext is first encrypted, and then a Message Authentication Code (MAC) is computed over the resulting ciphertext.

* **[[Public-Key Encryption]]** Encryption methods that use a pair of keys for each participant: a public key, which can be freely distributed and used for encryption, and a private key, which is kept secret and used for decryption. Methods including [[RSA (Rivest–Shamir–Adleman) cryptosystem|RSA]] and [[Elliptic Curve Cryptography (ECC)]] are essential for secure key exchange and digital signatures. [2, 40]

- **[[Elliptic-curve cryptography (ECC)]]** is an approach to [[Public-Key Encryption|Public-Key cryptography]]  based on the algebraic structure of elliptic curves over finite fields. ECC allows smaller keys to provide equivalent security, compared to cryptosystems based on modular exponentiation in Galois fields, such as the [[RSA (Rivest–Shamir–Adleman) cryptosystem|RSA cryptosystem]] and [[ElGamal]] cryptosystem. Elliptic curves are applicable for key agreement, digital signatures, [[Pseudorandom Generator (PRG)|pseudorandom generators]], and other tasks. Indirectly, they can be used for encryption by combining the key agreement with a symmetric encryption scheme.
- **[[RSA (Rivest–Shamir–Adleman) cryptosystem]]** is a public-key cryptosystem, one of the oldest (1977) widely used for secure data transmission. An RSA user creates and publishes a public key based on two large prime numbers, along with an auxiliary value. The prime numbers are kept secret. Messages can be encrypted by anyone, via the public key, but can only be decrypted by someone who knows the private key.
* **[[Diffie-Hellman (DH)]]** A cryptographic protocol that allows two parties to establish a shared secret key over an insecure communication channel without ever exchanging the secret directly. Key exchange protocols like Diffie-Hellman enable two parties to securely establish a shared secret key over an insecure channel, which can then be used for symmetric encryption. [39]
	- **[[Triple Diffie-Hellman (3DH)]]** An extension of the [[Diffie-Hellman (DH)|Diffie-Hellman]] key exchange protocol that involves three Diffie-Hellman exchanges, used in protocols like [[Signal]]'s [[X3DH (Extended Triple Diffie-Hellman)|X3DH]] for more robust key establishment.

* **[[Hybrid Public Key Encryption]]** Encryption schemes that combine the efficiency of symmetric encryption with the key management benefits of [[Public-Key Encryption]], often by using a public key to encrypt a session key, which is then used for symmetric encryption of the bulk data.

* **[[ElGamal]]** (1985) An asymmetric key encryption algorithm for [[Public-Key Encryption|public-key cryptography]] based on the difficulty of computing discrete logarithms in a finite field. Based on the [[Diffie-Hellman]] key exchange.

* **[[Cryptographic Hash Functions]]** Functions that take arbitrary-size input and produce a fixed-size, deterministic output (the hash or digest), with the properties of being one-way (computationally hard to reverse) and collision-resistant (computationally hard to find two different inputs that produce the same output). Hashing algorithms like [[SHA256|SHA-256]] are used to generate unique fingerprints of data, ensuring message integrity and playing a role in authentication processes. [48]

* **[[SHA256]]** Secure Hash Algorithm with a 256-bit output, a widely used cryptographic hash function.
	* **[[HMAC-SHA256]]** A specific type of [[Message Authentication Codes (MACs)|MAC]] that uses the [[SHA256]] hash function in combination with a secret key to produce an authentication tag.
* **[[Pseudorandom Function (PRF)]]** A keyed function that, when evaluated on an input, produces an output that is computationally indistinguishable from a truly random function. PRFs are essential for deriving cryptographic keys and other sensitive values.
	* **[[Pseudorandom Generator (PRG)]]** A part of [[Pseudorandom Function (PRF)|PRF]], algorithm that takes a short, truly random seed as input and outputs a much longer sequence of bits that appear to be random, used for generating cryptographic keys and other random-like data.

* **[[Message Authentication Codes (MACs)]]** Cryptographic primitives that provide integrity and authenticity of a message by generating a short, fixed-size tag that is appended to the message. Anyone with the secret key can verify the tag, ensuring the message hasn't been tampered with and originates from a known source.

* **[[Post-Quantum Cryptography]]** Cryptographic algorithms that are believed to be secure against attacks from both classical computers and future quantum computers, intended to replace current public-key cryptography that might be vulnerable to quantum algorithms like Shor's algorithm. The anticipated advancements in quantum computing pose a potential threat to many of the current encryption algorithms that underpin secure messaging, necessitating a transition to post-quantum cryptography. [92]
	* **[[Code-based cryptography]]** A branch of [[Post-Quantum Cryptography]] that relies on the difficulty of solving problems related to error-correcting codes.
	* **[[Isogeny-based cryptography]]** A branch of [[Post-Quantum Cryptography]] that uses isogenies between elliptic curves as the basis for its hard mathematical problems.
	* **[[Lattice-based cryptography]]** A branch of [[Post-Quantum Cryptography]] that constructs cryptosystems based on the mathematical properties of lattices in high-dimensional vector spaces.
	* **[[Hash-based cryptography]]** A branch of [[Post-Quantum Cryptography]] that builds cryptographic schemes primarily using secure [[Cryptographic Hash Functions]].
	* **[[Multivariate cryptography]]** A branch of [[Post-Quantum Cryptography]] that uses systems of polynomial equations over finite fields as its foundation.

* **[[Key Encapsulation Mechanism (KEM)]]** A type of [[Public-Key Encryption]] scheme specifically designed to securely transmit a randomly generated secret key (session key). KEMs are a fundamental building block in many modern cryptographic protocols, including those being developed for post-quantum security.

* **[[Zero-Knowledge Proof]]** Cryptographic methods that allow one party (the prover) to convince another party (the verifier) that a statement is true without revealing any information beyond the validity of the statement itself.
	* **[[Non-interactive zero knowledge (NIZK) proofs]]** A type of [[Zero-Knowledge Proof]] where the prover can generate the proof and the verifier can check its validity without any interaction between them after an initial setup.

* **[[Homomorphic Encryption]]** A type of encryption that allows computations to be performed on ciphertext such that the result of the computation, when decrypted, matches the result of the same computation performed on the plaintext. 

* **[[Threshold Cryptosystems]]** Cryptographic systems where a certain number (the threshold) of participating entities are required to perform a sensitive cryptographic operation, such as decryption or signing. (No specific usage in the context of messaging protocols detailed in the sources).

* **[[Private Set Intersection (PSI)]]** A cryptographic technique that allows two parties, each holding a set of items, to compute the intersection of their sets without revealing any information about the elements that are not in the intersection.

* **[[Forward Secrecy]]** A security property that ensures past messages remain secure even if long-term keys are compromised. It is a key feature provided by the [[Double Ratchet]] algorithm in the [[Signal Protocol]]. [56]

* **[[Post-Compromise Security]]** Also known as future secrecy, this security property ensures that future messages are secure even if a session key is compromised. Like forward secrecy, it is provided by the [[Double Ratchet]] algorithm in the [[Signal Protocol]]. [56]

* **[[Confidentiality]]** The property of keeping the content of a message secret and accessible only to authorized individuals. It is a core tenet of message privacy and security in digital communication. [4]

* **[[Integrity]]** The assurance that a message remains unaltered during transmission, preventing any unauthorized modification. It is a fundamental aspect of message security. [4]

* **[[Availability]]** The guarantee that authorized users can access and use the communication systems and data when required. It is an important component of overall message security. [4]

* **[[Metadata]]** Information about the communication, such as the sender and recipient, timestamps, and message size, as distinct from the actual content of the message. While message content may be protected by encryption, metadata can still reveal significant information about users and their activities, making metadata privacy a critical concern. [8, 9, 80, 31]

* **[[Message Privacy]]** The capacity to transmit information across digital networks in a manner that ensures the content remains comprehensible only to the intended recipient or recipients. It necessitates the protection of the message from unauthorized access, whether during its transmission across the network or while it is stored on servers. At its core, message privacy is about maintaining [[Confidentiality|confidentiality]]  and secrecy, aligning with the user's fundamental expectation that their communications will not be disclosed to unintended parties or made public without their consent. [1, 3]

* **[[Message Security]]** The broader objective of safeguarding the [[Message Privacy|privacy]] and [[Confidentiality|confidentiality]] of messages that are transmitted through electronic means, particularly with the widespread adoption of mobile devices for communication. It involves a multi-faceted approach that includes ensuring authentication of the sender and receiver, maintaining the confidentiality of the message content, preserving the integrity of the message against tampering, providing non-repudiation to prevent denial of sending, ensuring the availability of the communication system when needed, and controlling authorization to access messages. [2, 6]