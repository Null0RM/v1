# 🗼 Node _(in Blockchain)_

## What?

| A software client that participates in the network. | [https://ethereum.org/en/glossary/#node](https://ethereum.org/en/glossary/#node) |
| --------------------------------------------------- | -------------------------------------------------------------------------------- |
| [Node, Full node, Archival node, Pruned node, Peer] |                                                                                  |
| A computer that connects to the Bitcoin network.    |                                                                                  |

Not to be confused with: Lightweight node, SPV node | [https://developer.bitcoin.org/glossary.html#term-Node](https://developer.bitcoin.org/glossary.html#term-Node) |

- legacy
  - _**a device** in the network that participates in **maintaining the blockchain**_
  - make up the blockchain network and are the only way to access it
  - maintains its own copy of the blockchain and works to ensure this copy checks out with all the other nodes and their respective copies

## How?

- 🤝 [Terms: **Consensus**](https://www.notion.so/Terms-Consensus-0c56ca02cff44a5b9b4562f370a9eccc?pvs=21)

# Full Node _(in Blockchain)_

- store **the current and most recent** blockchain states
- participate in validating newly added blocks
- process transactions, execute smart contracts, and query/serve blockchain data

# **Light Node (Light Client)** _(in Blockchain)_

- **only store block headers**, giving them access to minimal blockchain data
- interface with full nodes to get necessary data and validate information
- requires the least investment in hardware, running costs, and technical expertise

# 🧐 Archive Node

| An archive node is an instance of an Ethereum client configured to build an archive of all historical states. It is a useful tool for certain use cases but might be more tricky to run than a full node. | [https://ethereum.org/en/developers/docs/nodes-and-clients/archive-nodes/](https://ethereum.org/en/developers/docs/nodes-and-clients/archive-nodes/) |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| archive nodes can store the complete historical data for the blockchain and serve it on request.                                                                                                          |                                                                                                                                                      |

These are different from full nodes that only store the recent blockchain state and light nodes that primarily request data from full nodes. | [https://www.alchemy.com/overviews/archive-nodes](https://www.alchemy.com/overviews/archive-nodes) | | [Node, Full node, Archival node, Pruned node, Peer] A computer that connects to the Bitcoin network. | [https://developer.bitcoin.org/glossary.html#term-Archival-node](https://developer.bitcoin.org/glossary.html#term-Archival-node) |

## See also

- [https://ethereum.org/en/developers/docs/nodes-and-clients/](https://ethereum.org/en/developers/docs/nodes-and-clients/)
- [https://ethereum.org/en/developers/docs/nodes-and-clients/node-architecture/](https://ethereum.org/en/developers/docs/nodes-and-clients/node-architecture/)
- [https://ethereum.org/en/developers/docs/nodes-and-clients/#sync-modes](https://ethereum.org/en/developers/docs/nodes-and-clients/#sync-modes)
- [https://ethereum.org/en/developers/docs/nodes-and-clients/run-a-node/](https://ethereum.org/en/developers/docs/nodes-and-clients/run-a-node/)

[https://ethereum.org/en/developers/docs/apis/json-rpc/](https://ethereum.org/en/developers/docs/apis/json-rpc/)

---

- legacy
    <aside> 💡 Explains how **archive nodes** work in **Ethereum**
    
    </aside>
    
    ### What?
    
    - store the complete historical data for the blockchain and serve it on request
        
        > **performs a “full sync”, which downloads full block data from the genesis block including block headers, transactions, and receipts**
        
    - must 'synchronize' with the blockchain's current state to store and verify data on the network
        
    - **verify all downloaded blocks, re-execute all transactions, and write all intermediate states to your disk**
        
    - requires the most investment in hardware, running costs, technical expertise, and experience
        
    
    ### Why?
    
    - **provide a gateway for accessing historical information about the blockchain**
    - **useful if you need older data than those contained in the recent 128 blocks (which would be available via full nodes)**
    
    ### Implementations
    
    - **Geth** (Go Ethereum) Archive Node
    - Erigon Archive Node
    - Nethermind Archive Node
    - Besu Archive Node

### 📝 Comparison of Full Node and Light Node

| Feature             | Full Node                                            | Light Node (Light Client)                                |
| ------------------- | ---------------------------------------------------- | -------------------------------------------------------- |
| Storage             | Stores the current and most recent blockchain states | Stores only block headers                                |
| Validation          | Participates in validating newly added blocks        | Interfaces with full nodes to validate information       |
| Processing          | Processes transactions, executes smart contracts     | Does not process transactions or execute smart contracts |
| Data Access         | Queries and serves comprehensive blockchain data     | Accesses minimal blockchain data via full nodes          |
| Hardware Investment | 📈▲ Requires significant investment in hardware      | 📉▼ Requires the least investment in hardware            |
| Running Costs       | 📈▲ Higher running costs                             | 📉▼ Lower running costs                                  |
| Technical Expertise | 📈▲ Requires substantial technical expertise         | 📉▼ Minimal technical expertise needed                   |
