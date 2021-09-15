# MathChain L1 Substrate Runtime API

Network information:

[https://docs.mathchain.org/en/networks/](https://docs.mathchain.org/en/networks/)

## accountService
MultiAddress Binding

### bind(extrinsics)

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|account_service|AccountServiceEnum|support alias|

---

### clear(extrinsics)
Clear current account bindings

**Params**

None

---

### forceBind(extrinsics)
Admin account binding

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|dest|AccountId|target address|
|account_service|AccountServiceEnum|support ETH address as alias|

---

### forceClear(extrinsics)
Admin account clean address binding

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|dest|AccountId|target address|

---

### setKey(extrinsics)
Setup admin account (need sudo)

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|new|AccountId|Need a new account|

---

### accountRoot(chainstate)
Query admin account

**Params**

Non

**Return**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|AccountId|AccountId|Admin account|

---

### fromEthereum(chainstate)
Query binding AccountId based on ETH address

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|AccountServiceEnum|AccountServiceEnum::Ethereum|ETH address|

**Return**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|AccountId|AccountId|Binding AccountId <AccountId, empty>|

---

### fromNickname(chainstate)
Query binded AccountId based on alais

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|AccountServiceEnum|AccountServiceEnum::Nickname|Bined alias|

**Return**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|AccountId|AccountId|Bind AccountId <AccountId, empty>|

---

### multiAddressOf(chainstate)
Query account multiAddress data

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|AccountId|AccountId|Target AccountId|

**Return**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|nickname|AccountServiceEnum::Nickname|Binded alias|
|ethereum|AccountServiceEnum::Ethereum|Binded Ethereum Address|

---

## balances
Balance related pallet（Add spending limitations）
### set_limit(extrinsics)
Binding operations

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|limit_info|AccountLimit|Format {daily_limit: 10000, monthly_limit: 100000, yearly_limit: 1000000000}|

---

### transferInfo(chainstate)
Query account total spending

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|AccountId|AccountId|Target AccountId|

**Return**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|date|u64|updatedate|
|daily_info|Balance|daily total spending, if not today means no spending|
|monthly_info|Balance|monthly total spending, if not this month means no spending|
|yearly_info|Balance|yearly total spending, if not this year means no spending|

---

### limits(chainstate)
Query account spending limit

**Params**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|AccountId|AccountId|Target AccountId|

**Return**

|Name|Value|Note|
| :----------: | :------: | :--------: |
|daily_limit|Balance|daily spending limit|
|monthly_limit|Balance|monthly spending limit|
|yearly_limit|Balance|yearly spending limit|
