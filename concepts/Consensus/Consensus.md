PoS (Proof of Stake)

Ethereum Protocol

동일한 PoS도 구현 방법이 다를 것이다.
Consensus는 엄밀히 따지면 Blockchain이 갖추어야 할 요건이다.

# Consensus _(in blockchain)_

| 1. When several nodes (usually most nodes on the network) all have the same blocks in their locally-validated best block chain. 2. what happens when nodes follow the same consensus rules

Not to be confused with: Social consensus (often used in discussion among developers to indicate that most people agree with a particular plan)

| Consensus rules (1. the block validation rules that full nodes follow to stay in consensus with other nodes 2. the rules that allow nodes to maintain consensus)                                                                     | [https://developer.bitcoin.org/glossary.html#term-Consensus](https://developer.bitcoin.org/glossary.html#term-Consensus) |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------ |
| When more than 2/3 of the computers in a network agree that they have the same set of records, making sure everyone is on the same page. This isn't about the rules they follow, but making sure they all have the same information. | [https://ethereum.org/en/glossary/#consensus](https://ethereum.org/en/glossary/#consensus)                               |

## See also:

- [Consensus rules (Ethereum)](https://ethereum.org/en/glossary/#consensus-rules)
- [Consensus rules (Bitcoin)](https://developer.bitcoin.org/glossary.html#term-Consensus-rules)
- [\*\*Consensus client](https://ethereum.org/en/glossary/#consensus-client)\*\*
- [**Consensus layer**](https://ethereum.org/en/glossary/#consensus-layer)

---

- legacy
  - Each node chooses to **accept or reject** the newest block based on the validity of its signatures and transactions
    - communicating with other nodes makes it easy to reject invalid blocks and identify bad nodes (no need to rely on a single source of truth)
    - block accepted → continues to be shared with other nodes until a consensus is reached and they are all in sync
  - When several nodes (usually most nodes on the network) all have the same blocks in their locally-validated best block chain.
