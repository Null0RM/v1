1. `Troy` 발표 키워드 나열
2. 연관 관계 정립

What is Ethereum?
○ Transaction-based state machine
● Ethereum and EVM Basics
○ Transaction, State, Block, Account, EVM…
● Application of Ethereum
○ Tokens, DeFi…
● Consensus Mechanism of Ethereum
○ Proof-of-Work
○ Proof-of-Stake
■ BFT
■ Gasper
● Future of Ethereum?
○ Account Abstraction, Single Slot Finality…

https://ethereum.org/en/what-is-ethereum/

https://ethereum.org/en/developers/docs/intro-to-ethereum/

# EVM (Ethereum Virtual Machine)

- 이더리움 네트워크 내 트랜잭션을 수행하기 위한 런타임 환경. 모든 노드가 EVM 위에서 동작하는 것은 아니지만, 모든 EVM은 노드 위에서 동작한다.
- [https://en.wikipedia.org/wiki/Ethereum#Virtual_machine](https://en.wikipedia.org/wiki/Ethereum#Virtual_machine)

# Opcode (Operation Code)

- 하드웨어에게 일련의 명령을 수행할 수 있도록 전달하는 명령 코드. 프로세서 아키텍처에 따라 차이가 있다. EVM은 이러한 차이가 발생하지 않도록 하여, 모든 컴퓨터가 동일한 결과를 계산할 수 있도록 보장한다.
- [https://en.wikipedia.org/wiki/Opcode](https://en.wikipedia.org/wiki/Opcode)

# EVM-compatible

- 어떤 대상이든 이더리움 네트워크와 동일하게 EVM 위에서 트랜잭션 수행이 가능하다면, 이를 EVM과 호환된다고 표현할 수 있다. 이더리움에서 파생되는 네트워크나 스마트 계약, DApp은 모두 EVM 호환성을 갖추어야만 정상적으로 동작한다.

# Gas

- 트랜잭션을 처리하기 위해 발신자가 이더리움 네트워크에 지불해야 하는 수수료. 높을수록 빠르게 처리될 가능성이 높다.
- 가스를 절약하고 싶다면 ?
- [https://en.wikipedia.org/wiki/Ethereum#Gas](https://en.wikipedia.org/wiki/Ethereum#Gas)
- [https://ethereum.org/en/developers/docs/gas/](https://ethereum.org/en/developers/docs/gas/)

# EOA (Externally Owned Account)

- 개인 키로 암호화된 계정을 생성하고, 해당 키의 보유 여부를 통해 인증과 모든 권한에 대한 인가를 진행하는 계정 유형이다.
- [https://ethereum.org/en/developers/docs/accounts/](https://ethereum.org/en/developers/docs/accounts/)
- controlled by anyone with the private keys

# CA (Contract Account)

- 스마트 계약을 통해 네트워크로 배포된 형태의 계정이다.
- a smart contract deployed to the network, controlled by code

# EIPs (Ethereum Improvement Proposals)

- standardize and provide high-quality documentation for Ethereum itself and conventions built upon it
- [https://github.com/ethereum/eips](https://github.com/ethereum/eips)

# ERCs (Ethereum Request for Comments)

- standardize and provide high-quality documentation for the Ethereum application layer
- [https://github.com/ethereum/ERCs](https://github.com/ethereum/ERCs)

# ERC-20

- A standard interface for tokens
- [https://docs.openzeppelin.com/contracts/2.x/erc20](https://docs.openzeppelin.com/contracts/2.x/erc20)
- [https://ethereum.org/ko/developers/docs/standards/tokens/erc-20/](https://ethereum.org/ko/developers/docs/standards/tokens/erc-20/)
- [https://eips.ethereum.org/EIPS/eip-20](https://eips.ethereum.org/EIPS/eip-20)

# ERC-721

- A standard interface for non-fungible tokens, also known as deeds
- [https://ethereum.org/ko/developers/docs/standards/tokens/erc-721/](https://ethereum.org/ko/developers/docs/standards/tokens/erc-721/)
- [https://docs.openzeppelin.com/contracts/2.x/api/token/erc721](https://docs.openzeppelin.com/contracts/2.x/api/token/erc721)

# ERC-1155

- A standard interface for contracts that manage multiple token types. A single deployed contract may include any combination of fungible tokens, non-fungible tokens or other configurations (e.g. semi-fungible tokens)
- [https://docs.openzeppelin.com/contracts/3.x/erc1155](https://docs.openzeppelin.com/contracts/3.x/erc1155)
- [https://ethereum.org/ko/developers/docs/standards/tokens/erc-1155/](https://ethereum.org/ko/developers/docs/standards/tokens/erc-1155/)

# Shanghai Upgrade

- hard fork upgrade in March 2023 was designed to give Ethereum cryptocurrency network users access to their staked ether (ETH) funds for the first time since The Merge, the update that transitioned the blockchain to proof-of-stake in 2022
- [https://www.investopedia.com/what-is-the-ethereum-shanghai-upgrade-7099021](https://www.investopedia.com/what-is-the-ethereum-shanghai-upgrade-7099021)

# Dencun Upgrade

- adopt EIP-4844, commonly called proto-danksharding. This upgrade introduces type-3 transactions (blobs), bringing new opportunities and new complexity for Layer 2 networks to optimize how they settle to the base layer
- [https://www.blocknative.com/ethereum-dencun-upgrade-countdown](https://www.blocknative.com/ethereum-dencun-upgrade-countdown)

# 📃 Smart Contract

- a program that runs on the Ethereum blockchain
- a collection of code (its functions) and data (its state) that resides at a specific address on the Ethereum blockchain
- Smart contracts are a type of Ethereum account. This means they have a balance and can be the target of transactions.
  - However they're not controlled by a user, instead they are deployed to the network and run as programmed.
- User accounts can then interact with a smart contract by submitting transactions that execute a function defined on the smart contract. Smart contracts can define rules, like a regular contract, and automatically enforce them via the code. Smart contracts cannot be deleted by default, and interactions with them are irreversible.

## Properties

- 관측가능성(observability) : 스마트 컨트랙트는 서로의 계약 이행 가능성을 관찰하거나 성과를 입증할 수 있어야 함
- 검증가능성(verifiability) : 계약을 이행하거나 위반할 경우 계약 당사자들이 이를 알 수 있어야 함
- 프라이버시(privacy) : 계약 내용은 계약에 필요한 당사자만 알 수 있어야 함
- 강제 가능성(enforceability) : 계약이 이루어질 수 있도록 구속력이 있어야 함

# Note

A sequence of [block](https://ethereum.org/en/glossary/#block) , each linking to its predecessor all the way to the [genesis block](https://ethereum.org/en/glossary/#genesis-block) by referencing the hash of the previous block. The integrity of the blockchain is crypto-economically secured using a proof-of-stake-based consensus mechanism. [What is a blockchain?](https://ethereum.org/en/developers/docs/intro-to-ethereum/#what-is-a-blockchain)

_(in Blockchain)_

# Ethereum

- Cryptocurrencies, such as bitcoin, **enable anyone to transfer money globally.** Ethereum does too, but it can also **run code that enables people to create apps and organizations.** It’s both resilient and flexible: any computer program can run on Ethereum.
- Ethereum is a decentralized blockchain with **smart contract** functionality.

![[Pasted image 20240707165445.png]]

**특징 요약**

1. 살얼음판: 시스템 규율 외에 모든 것이 자율
2. 철저한 계약 기반: 알면 웃고, 모르면 당한다
3. Immutable: 배포 당시의 환경이 유지된다.

[https://ethereum.org/en/learn/](https://ethereum.org/en/learn/)

[https://en.wikipedia.org/wiki/Ethereum](https://en.wikipedia.org/wiki/Ethereum)

# The Merge

The Merge 변천사

1. 비트코인 위에 프로그램을 실행시킬 수 있도록 하자 제안했지만 거절 당함
2. 그렇게 PoW 기반의 Ethereum으로 따로 만들기 시작
3. 추가로 검증 차원에서 별도로 Beacon Chain을 가동
4. PoW의 보상 시스템보다, PoS의 처벌 시스템이 보안에 더 유리하다고 생각
5. 당시 사용하던 PoW 네트워크는 (Transaction) Execution Layer로 사용하고, Beacon Chain은 Consensus Layer로 사용
6. Execution 레이어는 Paris, Consensus 레이어는 Bellatrix 버전에서 “The Merge”를 기점으로 PoS 전환 (두 네트워크는 Engine API 스펙에 맞춰 통신)
7. 당시 Eth 1, Eth 2 등의 용어가 있었지만 현재는 `Ethereum`으로 통합
