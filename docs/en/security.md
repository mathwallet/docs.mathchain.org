The security consideration of secretstore and smartwallet

The secret node is key to the security of smart wallet, and they are controlled by the MathChain. There will be 2 levels of attack may happen:

1 Control the validator of MathChain

Solution: because MathChain is the para-chain of Polkadot which means the attacker need to control most of the Polkadot validators. This is almost impossible to archive.

2 Control the secret node through MathChain governance

Solution: Any changes of MathChain including add/remove secret node need to go through MathChain governance. And same as Polkadot, there will be a council to vote the 1st round of governance proposal which means malicious proposal will be rejected at the council review and will not go to referendum phase.

Another security consideration is the operation of secret node:

1 If one secret node stop operation 3 years later?

Solution: the secretstore pallet supports transfer the node to a new one after the approval of MathChain governance

2 If one secret node temporary offline?

Solution: there is N:M threshold of secretkey, and this will impact the recovery process

