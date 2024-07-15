# Connections

블록 속성은 #Blockchain 별로 그 정의가 다르다.

# Block _(in Blockchain)_

[https://bitcoinwiki.org/wiki/block](https://bitcoinwiki.org/wiki/block)

a permanently recorded file at Bitcoin containing information on occurred transactions. Block is the record of the every recent transaction or its part that has not been recorded in the previous blocks. Practically in all cases blocks are added to the end of the chain, which contains all transactions and is called blockchain. When a block is added to the end of the chain, it cannot be changed. Each block contains information about everything that happened in previous blocks before it was created.

---

[https://developer.bitcoin.org/glossary.html#term-Block](https://developer.bitcoin.org/glossary.html#term-Block)

One or more transactions prefaced by a block header and protected by proof of work. Blocks are the data stored on the block chain.

---


[https://ethereum.org/en/developers/docs/blocks/](https://ethereum.org/en/developers/docs/blocks/)

Blocks are batches of transactions with a hash of the previous block in the chain. This links blocks together (in a chain) because hashes are cryptographically derived from the block data. This prevents fraud, because one change in any block in history would invalidate all the following blocks as all subsequent hashes would change and everyone running the blockchain would notice.                                                                                               
 New blocks are added to Ethereum every 12 seconds (unless a block proposer misses its turn), so a near-constant stream of data gets added to block explorers.
 
 
 Blocks contain a lot of important data that you may find useful:    
### Standard data

- Block height
    - The block number and length of the blockchain (in blocks) on creation of the current block
- Timestamp
    - The time at which a block was proposed
- Transactions
    - The number of transactions included within the block
- Fee recipient
    - The address that received gas fee tips from transactions
- Block Reward
	- The amount of ETH awarded to the validator who proposed the block
- Size
	- The size of the data within the block (measured in bytes)
- Gas used
	- The total units of gas used by the transactions in the block
- Gas limit
	- The total gas limits set by the transactions in the block
- Base fee per gas
	- The minimum multiplier required for a transaction to be included in a block
- Burnt fees
	- How much ETH is burned in the block
- Extra data
	- Any extra data the miner has included in the block

### Advanced data

- Hash
	- The cryptographic hash that represents the block header (the unique identifier of the block)
- Parent hash
	- The hash of the block that came before the current block
- StateRoot
	- The root hash of Merkle trie which stores the entire state of the system

[https://ethereum.org/en/developers/docs/data-and-analytics/block-explorers/#execution-data](https://ethereum.org/en/developers/docs/data-and-analytics/block-explorers/#execution-data) |

## See also

| Standard block relay                                        | The regular block relay method: announcing a block with an inv message and waiting for a response.                                                                                                         | [https://developer.bitcoin.org/glossary.html#term-Stanndard-block-relay](https://developer.bitcoin.org/glossary.html#term-Stanndard-block-relay)   |
| ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| Unsolicited block push                                      | When a miner sends a block message without sending an inv message first.                                                                                                                                   | [https://developer.bitcoin.org/glossary.html#term-Unsolicited-block-push](https://developer.bitcoin.org/glossary.html#term-Unsolicited-block-push) |
| V2 block                                                    | The current version of Bitcoin block                                                                                                                                                                       | [https://developer.bitcoin.org/glossary.html#term-V2-block](https://developer.bitcoin.org/glossary.html#term-V2-block)                             |
| Block header                                                |                                                                                                                                                                                                            |                                                                                                                                                    |
| Header                                                      | An 80-byte header belonging to a single block which is hashed repeatedly to create proof of work.                                                                                                          | [https://developer.bitcoin.org/glossary.html#term-Block-header](https://developer.bitcoin.org/glossary.html#term-Block-header)                     |
| Height                                                      |                                                                                                                                                                                                            |                                                                                                                                                    |
| Block height                                                | The number of blocks preceding a particular block on a block chain. For example, the genesis block has a height of zero because zero block preceded it.                                                    | [https://developer.bitcoin.org/glossary.html#term-Block-header](https://developer.bitcoin.org/glossary.html#term-Block-header)                     |
| Block reward                                                | The amount that miners may claim as a reward for creating a block. Equal to the sum of the block subsidy (newly available satoshis) plus the transactions fees paid by transactions included in the block. |                                                                                                                                                    |
| Not to be confused with: Block subsidy, Transaction fees    | [https://developer.bitcoin.org/glossary.html#term-Block-reward](https://developer.bitcoin.org/glossary.html#term-Block-reward)                                                                             |                                                                                                                                                    |
| Maximum Block Size                                          | The maximum size of a block according to the consensus rules. The current block size limit is 4 million weight units (1 million vbytes).                                                                   |                                                                                                                                                    |
| Not to be confused with: Block, Blockchain, Blockchain size | [https://developer.bitcoin.org/glossary.html#term-Maximum-Block-Size](https://developer.bitcoin.org/glossary.html#term-Maximum-Block-Size)                                                                 |                                                                                                                                                    |
| Blocks-first sync                                           | Synchronizing the block chain by downloading each block from a peer and then validating it.                                                                                                                |                                                                                                                                                    |
| Not to be confused with: Headers-first sync                 | [https://developer.bitcoin.org/glossary.html#term-Blocks-first-sync](https://developer.bitcoin.org/glossary.html#term-Blocks-first-sync)                                                                   |                                                                                                                                                    |
| Bloom filter                                                | A filter used primarily by SPV clients to request only matching transactions and merkle blocks from full nodes.                                                                                            | [https://developer.bitcoin.org/glossary.html#term-Bloom-filter](https://developer.bitcoin.org/glossary.html#term-Bloom-filter)                     |
