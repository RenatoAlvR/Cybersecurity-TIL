**2026-06-19**

# Birthday Attack
- A type of cryptographic brute force attack, that exploits the math behind the birthday paradox
- The birthday paradox is the probability of two people sharing a birthday in a room of random people which is 50% in a room of 23 people.
- The objective is to find a hash collision, which can be found in 2^(n/2) tries on average.

# How is it dangerous?
1. Digital signatures rely on hash values, an attacke could create 2 documents (a real one and a fraudulent one) and then generate millions of variations of them (not visual alterations, but enough so that the hash of them changes).

They generate list of hashes and try to find a collision. If found, they can make the victim sign the real document, and because the signature is linked to the hash, they can make the victim's signature valid and verified for the fraudulent document too.

2. It can be used to bypass file integrity checks. If an update or patch is intercepted, attackers could swap the files due to them having the same hash, even though the software is legitimized as original software

An example of this happened in 2008, when researcherds managed to create a forged Certificate Authority (CA) certificates using a birthday attack on MD5. Managing to make Man-in-the-Middle attacks in HTTPS websites.

# How to prevent it?
- Using larger hashing values, like SHA256 (which has 256 bits output), which makes it computationally infeasible to find a collision.
- Using salting with the hash values. This adds random data to the input of the hash function, which makes it harder to find a collision.

# Note
MD5 and SHA-1 are considered vulnerable and insecure due to this attack. As of now, SHA-256 and SHA-512 are considered secure due to current computational limitations. But due to Quantum Computing development, this could change in the near future.