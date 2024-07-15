EVM opcode는 이더리움 네트워크에서 스마트 계약을 실행하기 위한 기계어 명령어입니다. 이 명령어들은 EVM이 스마트 계약의 코드를 이해하고 실행할 수 있게 해줍니다. Opcode는 스마트 계약의 로직을 구현하는 데 필수적인 요소이며, 가스 소비, 메모리 관리, 흐름 제어 등 다양한 작업을 수행합니다.

## 중요성

- **가스 소비 계산**: 각 opcode는 실행 시 일정량(변동성을 가진 연산도 존재)의 가스를 소비합니다. 이는 네트워크의 자원을 사용하는 대가로, 스마트 계약의 효율성을 평가하는 데 중요한 요소입니다.
- **스마트 계약 실행**: opcode는 스마트 계약의 비즈니스 로직을 실행하는 데 필요한 기본적인 구성 요소입니다.
- **보안**: 일부 opcode는 보안 관련 작업을 수행하여 스마트 계약을 안전하게 유지합니다.

## 주요 Opcode 예시

- **SSTORE(0x55)** `storage[key] := val`

- **SLOAD(0x55)** `storage[key]`

- **CREATE (0xF0):** `addr = keccak256(rlp([address(this), this.nonce]))`
- **CREATE2 (0xF5):** `addr = keccak256(0xff ++ address(this) ++ salt ++ keccak256(mem[ost:ost+len-1]))[12:]`
  - ++ 연산자는 EVM의 CREATE2 opcode 컨텍스트에서 문자열 또는 바이트 시퀀스의 연결을 나타냅니다.

### tips

- `a, b => a + b` indicates that the `ADD` opcode takes two items off the stack (`a` and `b`) and places the sum of these two values on the stack. The leftmost item (`a`) is the top of the stack.

- All stack descriptions elide subsequent items that may be on the stack. It can be assumed that unspecified stack elements do not influence the semantics of an operation, except when a stack overflow would result.

- The maximum stack size is **1024** items, and all stack items are **32** bytes.

- `a // b` indicates flooring division. The result of division by 0 in the EVM is 0.

- All arithmetic operations are modulo 2\*\*256.

- Including the designated `INVALID` opcode, the EVM currently implements **141** opcodes, **65** of which are duplicates indicating the number of operands (`PUSHn`, `DUPn`, `SWAPn`, `LOGn`).

### 참고

- [evm-playground](https://www.evm.codes/)

  - [CREATE](https://www.evm.codes/playground?callValue=9&unit=Wei&codeType=Mnemonic&code=%27z0q0f9q9f0y4%20FFmslk3%200x63FFFFFFFF6000526004601CF3gvMSTORE~13~19gp%20%27~k%20z%2F%2F%20Createmnmccountjith%20yjeimnd%20v%5Cnqynolgg~pvCREATEm%20al%20codekvPUSH1j%20wg~0fpvvz%01fgjklmpqvyz~_)
  - [CREATE2](https://www.evm.codes/playground?callValue=9&unit=Wei&codeType=Mnemonic&code=%27z0LjjVfannoYrecWQ_parameters%2C%20becausliYgenerates_addressjjVz9L~1j~9Vz0v4%20FFZskX3%200x63FFFFFFFF60005260046000F3NyMSTORE~2~13~19Nq%27~X%20zfWanZccounYQ%20y%5Cnv%20weiZnd%20qyCREATE2le%20k%20codejNNf%2F%2F%20C_%20thlsamlZ%20aYt%20XyPUSH1WreatlVqyyQwithN~0Lvnok%01LNQVWXYZ_fjklqvyz~_)

- [ethereum/opcodes](https://ethereum.org/en/developers/docs/evm/opcodes/)

- https://jellopaper.org/evm/

- [opcodes/gas](https://github.com/wolflo/evm-opcodes/blob/main/gas.md)
