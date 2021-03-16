## accountService
提供MultiAddress相关绑定支持接口
### bind(extrinsics)
绑定操作

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|account_service|AccountServiceEnum|对应的绑定选项，目前仅支持自定义Nickname绑定|

---

### clear(extrinsics)
清空当前账号绑定的信息

**参数**

无

---

### forceBind(extrinsics)
使用管理账户进行绑定操作

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|dest|AccountId|需要绑定的目标账号|
|account_service|AccountServiceEnum|对应的绑定选项，目前支持Nickname与Ethereum绑定|

---

### forceClear(extrinsics)
使用管理账户进行账号清空操作

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|dest|AccountId|需要绑定的目标账号|

---

### setKey(extrinsics)
设置管理账户（必须root发起）

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|new|AccountId|需要设置的新账号|

---

### accountRoot(chainstate)
查询管理账号

**参数**

无

**返回**

|参数|值|备注|
| :----------: | :------: | :--------: |
|AccountId|AccountId|管理账户|

---

### fromEthereum(chainstate)
根据Ethereum地址查询绑定的AccountId

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|AccountServiceEnum|AccountServiceEnum::Ethereum|对应的Ethereum地址|

**返回**

|参数|值|备注|
| :----------: | :------: | :--------: |
|AccountId|AccountId|绑定对应的AccountId <AccountId, empty>|

---

### fromNickname(chainstate)
根据Nickname地址查询绑定的AccountId

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|AccountServiceEnum|AccountServiceEnum::Nickname|对应的Nickname|

**返回**

|参数|值|备注|
| :----------: | :------: | :--------: |
|AccountId|AccountId|绑定对应的AccountId <AccountId, empty>|

---

### multiAddressOf(chainstate)
查询对应账户的multiAddress绑定情况

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|AccountId|AccountId|要查询对应的AccountId|

**返回**

|参数|值|备注|
| :----------: | :------: | :--------: |
|nickname|AccountServiceEnum::Nickname|绑定后的Nickname|
|ethereum|AccountServiceEnum::Ethereum|绑定后的Ethereum|

---

## balances
提供余额相关操作的pallet（主要增加限额等数据）
### set_limit(extrinsics)
绑定操作

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|limit_info|AccountLimit|对应的账号limit信息，必须小于系统限额，格式如{daily_limit: 10000, monthly_limit: 100000, yearly_limit: 1000000000}|

---

### transferInfo(chainstate)
查询对应账户的转账总和信息

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|AccountId|AccountId|要查询对应的AccountId|

**返回**

|参数|值|备注|
| :----------: | :------: | :--------: |
|date|u64|当前数据更新日期|
|daily_info|Balance|日转账总量，如果date非当日，即当日无转账|
|monthly_info|Balance|月转账总量，如果date非当月，即当月无转账|
|yearly_info|Balance|年转账总量，如果date非当年，即当年无转账|

---

### limits(chainstate)
查询对应账户的限额信息

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|AccountId|AccountId|要查询对应的AccountId|

**返回**

|参数|值|备注|
| :----------: | :------: | :--------: |
|daily_limit|Balance|日转账总限额|
|monthly_limit|Balance|月转账总限额|
|yearly_limit|Balance|年转账总限额|