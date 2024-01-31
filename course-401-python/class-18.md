# *Course 401 Python, Entry 18: Cryptography

**What is the basic principle behind the Caesar Cipher, and how was it used historically?**

The basic principle is letter shifting. It was used by Julius Caesar to conceal confidential information. Likewise, the nephew of Caesar, Augustus, also used the cipher.

**What are the key differences between symmetric and asymmetric encryption? How is asymmetric used in secure communication today?**

Symmetric encryption means that any two characters are connected. If A is X, then X is A. In other words, the keys for encryption and decryption are the same. In asymmetric encryption, every key has it's own corresponding key. In this case, there is a pair of keys, one for decryption, and the other for decryption.

In AES, one of the prevailing modern encryption standards. AES is a symmetric encryption standard. The enigma machine was also symmetric.

RSA is the most common asymmetric encryption standard.

**How do computers generate random numbers, and what are the differences between true random number generation (TRNG) and pseudo-random number generation (PRNG)? Discuss their use cases in cryptography.**

Computers generate random numbers via hardware inputs (mouse movements, keyboard types and timings, fan speeds, etc.). An example of this implementation is Linux's /dev/random. A pseudo-random number is generated via an algorithm, so maybe too predictable. For this reason, RdRand on its own is not trusted and more entropy is added on top of the output from this chip.

**What’s the difference between encryption and decryption? Explain with an analogy.**

Encryption is the act of making plaintext less decipherable ciphertext. Decryption is the opposite, taking ciphertext and converting it to plaintext.

## Things I want to know more about

Why AES was needed to replace DES in 1999? What exactly were the weaknesses?
