![[Pasted image 20240707164949.png]]

# Nonce _(in Consensus: PoW: Mining)_

| [Solo Mining]

The mining software constructs a block using the template (described below) and creates a block header. It then sends the 80-byte block header to its mining hardware (an ASIC) along with a target threshold (difficulty setting). The mining hardware iterates through every possible value for the block header nonce and generates the corresponding hash.

If none of the hashes are below the threshold, the mining hardware gets an updated block header with a new merkle root from the mining software; this new block header is created by adding extra nonce data to the coinbase field of the coinbase transaction.

| On the other hand, if a hash is found below the target threshold, the mining hardware returns the block header with the successful nonce to the mining software. The mining software combines the header with the block and sends the completed block to bitcoind to be broadcast to the network for addition to the block chain. | [https://developer.bitcoin.org/devguide/mining.html?highlight=nonce#solo-mining](https://developer.bitcoin.org/devguide/mining.html?highlight=nonce#solo-mining) |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Proof of work,                                                                                                                                                                                                                                                                                                                   |                                                                                                                                                                  |
| POW] A hash below a target value which can only be obtained, on average, by performing a certain amount of brute force work—therefore demonstrating proof of work.                                                                                                                                                                | [https://developer.bitcoin.org/glossary.html#term-Proof-of-work](https://developer.bitcoin.org/glossary.html#term-Proof-of-work)                                 |

# Nonce _(in Ethereum)_

| An account nonce is a transaction counter in each account, which is used to prevent replay attacks. | [https://ethereum.org/en/glossary/#nonce](https://ethereum.org/en/glossary/#nonce) |
| --------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |

# Nonce _(in Cryptography)_

| a number that can only be used once – in cryptography is a one-time code, vibrant overcome or pseudorandom manner, which is used to biopsy the main to do transmission, preventing to take the power of reproduction. | [https://bitcoinwiki.org/wiki/nonce](https://bitcoinwiki.org/wiki/nonce)           |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| In cryptography, a value that can only be used once.                                                                                                                                                                  | [https://ethereum.org/en/glossary/#nonce](https://ethereum.org/en/glossary/#nonce) |
