https://docs.optimism.io/stack/protocol/rollup/overview

- an L2 blockchain built by Ethereum developers that processes its transactions in batches using optimistic rollups. Users gain access to cheap and near instantaneous transactions are cheap and nearly instantaneous. Developers can use Optimism as a fast, stable, scalable and secure solution to programmes requiring Ethereum apps.
- an implementation of optimistic rollup
- [https://ethereum.org/en/developers/tutorials/optimism-std-bridge-annotated-code/](https://ethereum.org/en/developers/tutorials/optimism-std-bridge-annotated-code/)


### 계속 이의 제기를 하게 되면 network를 느리게 할 수 있다 ( X )
Validator의 이의 제기 > fraud proof
이의제기를 하는 비용에 비해 검증 비용이 매우 높기 때문에 악의적인 밸리데이터가 지연 공격을 수행할 가능성은 충분히 존재

대부분의 optimistic rollup에서 챌린지는 permissioned entity (예. 밸리데이터)만 제기할 수 있도록 구현
fraud proof를 명백히 악의적인 목적으로 제기했다고 판명되는 경우에는 거버넌스나 security council 등 상위 권한의 시스템에 의해 밸리데이터에서 추방되거나 슬래싱
optimistic rollup은 대부분 중앙화된 시퀀서에 의해 동작하고 있기 때문에 챌린지를 발동 자체가 희귀함
Kroma 체인에서 챌린지를 발동시켜 성공한 사례 [https://blog.kroma.network/about-the-first-successful-challenge-on-kroma-mainnet-aeca715b05d7](https://blog.kroma.network/about-the-first-successful-challenge-on-kroma-mainnet-aeca715b05d7 "https://blog.kroma.network/about-the-first-successful-challenge-on-kroma-mainnet-aeca715b05d7")

vs

### L2->L1 으로의 출금 tx을 수행하지 못하는 것이지 L2의 네트워크 지연과는 무관하다. ( O )
이의 제기를 하더라도 시퀀서가 계속해서 L2 블록을 생성합니다.
이의 제기를 계속적으로 발생시킬 경우 L2의 최신 체크포인트가 확정되지 않으니,

이의 제기가 발생할 경우, 승자를 가리는 챌린지 프로세스가 진행되며, 이 경우 패자는 담보로 맡겨놓은 이더를 승자에게 지불하게 됩니다. 따라서 공격 자금을 소모해가며 계속해서 이의제기를 수행할 순 있지만, 이는 출금 트랜잭션만을 지연시키는 것에 해당하며 자금이 고갈될 경우 최신 체크포인트가 확정되면서 출금도 마저 진행될 수 있습니다.

이의제기라는 프로세스 자체 또한 트랜잭션일까요?
만약 그 과정 또한 트랜잭션이라면 flash loan 또는 flash swap을 통해 무담보대출을 이용해 "담보"를 제출하고, 무작위 이의제기 공격 실패 시, loan을 상환하지 못하므로 트랜잭션 자체가 실패하게 되니 공격자는 수수료와 가스비만 지출하게 되니 충분히 이를 이용해 공격이 가능하지 않을까 하는 생각에 질문 드립니다...!

이의제기 스타트는 한번의 트랜잭션으로 시작되나 챌린지 프로세스는 여러 트랜잭션에 나눠서 진행됩니다. 그리고 담보의 경우 미리 이더를 컨트랙크에 예치해야하며 보통 언락 기간이 있어 단번에 예치와 출금을 수행할 수는 없습니다. 챌린지 프로세스를 간략히 설명하자면 누가 잘못된 체크포인트를 주장하는지 잘못된 부분을 찾는 과정입니다. 가장 직관적인 방법은 geth같은 이더리움 클라이언트를 L1 컨트랙트로 구현하고, 이의제기된 기간동안의 L2 트랜잭션을 해당 컨트랙트에서 실행하여 output (체크포인트)를 확인하는 방법입니다. 하지만 해당 방법은 계산 리소스가 너무 많이 소비되기 때문에 서로 핑퐁을 해가면서 서로간 동의하지 않는 아주 작은 부분을 찾아내고 (bisect 과정) 해당 트랜잭션에 대해서만 검증을 수행하는 과정을 거쳐 승자와 패자를 결정합니다.

optimistic rollup의 finality가 1주일이라 1주일 동안 dispute 하면 되는거라 L2 네트워크 자체의 속도에는 영향을 주지는 않습니다. (악의적인 challenge 요청 자체가) https://kelvinfichter.com/pages/thoughts/challenge-periods/