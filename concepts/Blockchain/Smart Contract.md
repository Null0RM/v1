> 개념 자체는 1990년대에 `Nick Szabo`에 의해 처음으로 소개되었다. [1](https://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/smart.contracts.html)[2](https://www.fon.hum.uva.nl/rob/Courses/InformationInSpeech/CDROM/Literature/LOTwinterschool2006/szabo.best.vwh.net/idea.html) 자판기가 인력의 투입 없이 _( without a human intermediary )_ 판매 행위를 자동화하는 것처럼, `Smart Contract` 또한 모든 형태의 교환을 가상으로 자동화한다. _( automate exchange virtually )_

- 이후 `Ethereum` 진영에서 `EVM` 위에서 `deterministic`한 방식으로 동작하는 바이트 코드를 컴파일 언어 `Solidity`를 활용하여 쉽게 작성할 수 있도록 지원했다.
- 다른 `cryptocurrency blockchain`도 이 기능을 지원한다. 따라서, `Smart Contract`를 `Ethereum`만의 독자적 기술로 보는 견해는 타당하지 않다.
- 누구나 계약을 작성하여 네트워크로 배포할 수 있다. 이러한 계약은 투명하게 공개되어, 그 내용을 누구나 쉽게 읽을 수 있다.

## How do smart contracts work?

- Smart contracts are written in a variety of programming languages (including Solidity, Web Assembly, and Michelson). On the Ethereum network,  each smart contract’s code is stored on the blockchain, allowing any interested party to inspect the contract’s code and current state to verify its functionality.
- Each computer on the network (or “node”) stores a copy of all existing smart contracts and their current state alongside the blockchain and transaction data.
- When a smart contract receives funds from a user, its code is executed by all nodes in the network in order to reach a consensus about the outcome and resulting flow of value. This is what allows smart contracts to securely run without any central authority, even when users are making complex financial transactions with unknown entities.
- To execute a smart contract on the Ethereum network, you will generally have to pay a fee called “gas” (so named because these fees keep the blockchain running).
- Once deployed onto a blockchain, smart contracts generally can’t be altered, even by their creator. (There are exceptions to this rule.) This helps ensure that they can’t be censored or shut down.

Solidity compiled to bytecode running on EVM

Ethereum

https://ethereum.org/en/smart-contracts/
https://ethereum.org/en/developers/docs/smart-contracts/
https://en.wikipedia.org/wiki/Smart_contract
https://ko.wikipedia.org/wiki/스마트_계약
https://www.ibm.com/topics/smart-contracts

https://www.coinbase.com/learn/crypto-basics/what-is-a-smart-contract
