# MathChain SecretStore API

## secretStore
提供secretstore相关支持接口

### addKeyServer(extrinsics)
添加key server

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|KeyServerId|key server id to add|
|network_address|KeyServerNetworkAddress|address|

---

### removeKeyServer(extrinsics)
移除key server

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|KeyServerId|key server id to remove|

---

### changeOwner(extrinsics)
改变key server所有权

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|new_owner|AccountId|new owner|

---

### generateServerKey(extrinsics)
生成新的server key

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id to claim|
|threshold|u8|操作阈值|

---

### claimKey(extrinsics)
声明server key的所有权

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id to claim|

---

### retrieveServerKey(extrinsics)
获取server key

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id to retrieve|

---

### transferKey(extrinsics)
更改server key的所有权

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|related Server Key id|
|new_claimant|EntityId|new owner|

---

### storeDocumentKey(extrinsics)
将document key存入secret store

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id bind|
|common_point|H512|common point of document key|
|encrypted_point|H512|encrypted point of document key|

---

### retrieveDocumentKeyShadow(extrinsics)
恢复document key

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id bind|
|requester_public|H512|requester's public key|

---

### startMigration(extrinsics)
调用该方法开始key servers的迁移流程

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|migration_id|MigrationIdT|Migration id|

---

### confirmMigration(extrinsics)
迁移完成时，每个key server调用confirmMigration确认迁移状态

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|migration_id|MigrationIdT|Migration id|
