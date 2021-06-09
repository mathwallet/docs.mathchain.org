The security consideration of secretstore and smartwallet are:

智能钱包的主要安全考虑因素包括：

Secret node 是保证智能钱包安全的主要因素，而它们由 MathChain 控制。对于他们的攻击主要存在如下两种可能：

1 控制 MathChain 的验证节点

解决方案：因为 MathChain 通过平行链机制接入波卡中继链，即自动获得波卡安全性，所以攻击者需要控制多数波卡验证节点，该行为几乎无法完成。

2 通过控制 MathChain 治理控制 Secret node

解决方案：如何对 MathChain 的修改，包括增减 secret node 都需要经过 MathChain 治理过程，而且 MathChain 的治理存在与波卡主网类似的理事会机制。任何提案都会先由理事会进行审核，通过后才能进入公投阶段，因此即使攻击者获得多数的 MATH 公投投票权，但恶意的提案会在理事会审核是被拒绝。
