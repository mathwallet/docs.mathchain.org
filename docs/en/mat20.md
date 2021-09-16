## Compile and Deploy

Open [https://remix.ethereum.org](https://remix.ethereum.org)

Delete the default files, and create a new file: Token.sol

![](http://qiniu.eth.fm/2020-11-06-16046499469366.jpg)

Copy the Token.sol code from below repo

[https://github.com/mathwallet/MathChain-L2-Contracts/blob/main/erc20.sol](https://github.com/mathwallet/MathChain-L2-Contracts/blob/main/erc20.sol)

You need to modify MAT20Token code based on your needs, including name, symbol, decimals, totalSupply

![](http://qiniu.eth.fm/2020-11-06-16046500570434.jpg)

Compile:

Go to 2nd tab, click Compile Token.sol

![](http://qiniu.eth.fm/2020-11-06-16046501720182.jpg)

Deploy：

Go to 3rd tab

ENVIRONMENT select Injected Web3, Remix will connect to MathWallet which is need to sign the deployment transaction

![](http://qiniu.eth.fm/2020-11-06-16046502362638.jpg)

Click 'Deploy' to start

In the popup MathWallet confirm window, click 'Accept'

After few seconds, you can find your new smart contract on block explorer

[https://docs.mathchain.org/en/networks/](https://docs.mathchain.org/en/networks/)

## Config Contract

Mint Token

Find mint function, enter the address and amount (remember to add the decimals in the amount field)

![](http://qiniu.eth.fm/2020-11-06-16046508859398.jpg)

Open transfer

Find unpause function, click 'Write', sign the transaction

![](http://qiniu.eth.fm/2020-11-06-16046510225935.jpg)

Now your MAT20 token is ready to transfer

Note: you can use MathChain Explorer (https://explorer.mathchain.org/) - Token - Create Token to do this as well with friendly UI.

If you need a token contract with more functions such as mint / pause / unpause etc, you may reference below solidity code:

[https://github.com/mathwallet/MathChain-Contracts/blob/main/Contracts/MAT20.sol](https://github.com/mathwallet/MathChain-Contracts/blob/main/Contracts/MAT20.sol)
