## Compile Contract

Open [https://remix.ethereum.org](http://remix.ethereum.org/)

Delete the default files, and create a new file: NFT.sol

Copy the Token.sol code from below repo

https://github.com/mathwallet/MathChain-Contracts/blob/main/Contracts/NFT.sol

You need to modify NFTToken code based on your needs

![](http://qiniu.eth.fm/2020-11-06-16046513970734.jpg)

For example, you want to create a ColorNFT serie, and this NFT Token is named RED

![](http://qiniu.eth.fm/2020-11-06-16046531242013.jpg)

BaseURI is the meta data of the NFT token, format can be reference is below:

http://developer.mathwallet.org/bsc/nfttest/#

This json need to return a image URL for the NFT, ex:

http://developer.mathwallet.org/bsc/nfttest/red.jpg

Any user should be able to visit this image URL so that it can be showed in wallet and NFT markets.

For compiler version, select 0.5.5

![](http://qiniu.eth.fm/2020-11-06-16046533699220.jpg)

## Deploy Contract

![](http://qiniu.eth.fm/2020-11-06-16046534642628.jpg)

## Config Contract

Now you need to use addMinter to add an address

![](http://qiniu.eth.fm/2020-11-06-16046547018646.jpg)

Then this address will be able to call mint function to mint NFT to others

![](http://qiniu.eth.fm/2020-11-06-16046543017652.jpg)

Then you will able to review the detail NFT token information in block explorer

[http://scan.boka.network/#/Galois/](http://scan.boka.network/#/Galois/)
