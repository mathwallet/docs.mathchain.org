# MathChain SecretStore API

Endpoint: [wss://secretstore.maiziqianbao.net/ws](wss://secretstore.maiziqianbao.net/ws)

## secretStore
提供secretstore相关支持接口

### addKeyServer(extrinsics)
添加key server

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|id|KeyServerId|key server id to add|
|network_address|KeyServerNetworkAddress|address|

---

### removeKeyServer(extrinsics)
移除key server

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|id|KeyServerId|key server id to remove|

---

### changeOwner(extrinsics)
改变key server所有权

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|new_owner|AccountId|new owner|

---

### claimKey(extrinsics)
声明server key的所有权

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id to claim|

---

### generateServerKey(extrinsics)
生成新的server key

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id to claim|
|threshold|u8|操作阈值|

---

### storeDocumentKey(extrinsics)
将document key存入secret store

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id bind|
|common_point|H512|common point of document key|
|encrypted_point|H512|encrypted point of document key|

---

### retrieveDocumentKeyShadow(extrinsics)
恢复document key

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id bind|
|requester_public|H512|requester's public key|

---

### transferKey(extrinsics)
更改key的所有权

**参数**

|参数|值|备注|
| :----------: | :------: | :--------: |
|id|ServerKeyId|related Server Key id|
|new_claimant|EntityId|new owner|

