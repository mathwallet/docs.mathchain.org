# MathChain SecretStore API

## SecretStore
SecretStore realted API

### addKeyServer(extrinsics)
Add key server

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|KeyServerId|key server id to add|
|network_address|KeyServerNetworkAddress|address|

---

### removeKeyServer(extrinsics)
Remove key server

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|KeyServerId|key server id to remove|

---

### changeOwner(extrinsics)
Change key server owner

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|new_owner|AccountId|new owner|

---

### generateServerKey(extrinsics)
Generate new server key

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id to claim|
|threshold|u8|threshold value|

---

### claimKey(extrinsics)
Claim server key ownership

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id to claim|

---

### retrieveServerKey(extrinsics)
Get server key

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id to retrieve|

---

### transferKey(extrinsics)
Change server key owner

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|related Server Key id|
|new_claimant|EntityId|new owner|

---

### storeDocumentKey(extrinsics)
Save document key to secret store

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id bind|
|common_point|H512|common point of document key|
|encrypted_point|H512|encrypted point of document key|

---

### retrieveDocumentKeyShadow(extrinsics)
Retrive document key

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|id|ServerKeyId|Server Key id bind|
|requester_public|H512|requester's public key|

---

### startMigration(extrinsics)
Start key servers migration process

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|migration_id|MigrationIdT|Migration id|

---

### confirmMigration(extrinsics)
When migration complete, every key server need to confirm Migration status

**Params**

|Params|Value|Note|
| :----------: | :------: | :--------: |
|migration_id|MigrationIdT|Migration id|
