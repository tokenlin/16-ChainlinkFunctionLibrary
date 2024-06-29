# ChainlinkFunctionLibrary 开源项目介绍

## 1. 缘起
Chainlink是区块链预言机的龙头，其下的[chainlink-functions](https://docs.chain.link/chainlink-functions/getting-started)可以实现web2与web3的数据通讯。通过链上智能合约发送JS代码参数，可以请求web2的数据。详细介绍见chainlink-functions官方文档：https://docs.chain.link/chainlink-functions/getting-started

有了JS的加持，chainlink-functions可以认作为是EVM的扩展，EVM的L2。如消耗gas的复杂逻辑运算等均可以交给chainlink-functions进行处理，大大节省主链的gas。可以说chainlink-functions会有非常广的发展空间。

但是为了更安全运行，chainlink-functions对JS代码进行了限制.只能进行原生JS代码，不能引入包，这就意味着功能函数少。很多原本import下，一句代码就能解决的事，可能需要开发者用纯JS手搓个类似的函数来代替。这就意味着开发效率，开发质量可能降低。另外也对提高了chainlink-functions的入门门槛，不利chainlink-functions的推广。

因此，本项目目标是建立一个chainlink-functions的JS标准库，把项目上会遇到的需要手搓的函数都标准化，方便开发者直接进行调用，而不用自己再开发该函数。此举也降低了入门门槛，使得新手也可以快速开发出高质量的产品。

## 2. 适合人群
本项目为开源项目，任何人都可以参与。前期侧重于函数开发标准化，较适合对JS和solidity较熟悉的人员。后面技术手册编制，前端页面代码展示，项目推广等均可以参与。


## 3. 标准库的入库标准
任何有意义的函数均可以归入该标准库。函数入库前大体需要进过3个步骤测试及检验：
1. 首先经过[Chainlink Functions Playground](https://functions.chain.link/playground)的验证，这是检验函数是否有效的最快的验证方法。

2. 通过第1步的验证后，再发送链上进行测试环境验证.

3. 通过以上2步后，最后通过技术委员会对代码质量做最后的审查。

## 4. 标准库的初步规划
首批函数计划是实现solidity上的功能函数，包括但不限于如下：
1. abi.encodePacked()
2. abi.encode()
3. keccak256()-(by Kevin, on going)
4. bytes => string
5. string => bytes
6. 各种类型的转换
7. sign() and ecrecover()-(by Kevin, on going)
8. encrypt() and decrypt()-(by Kevin, on going)
9. 其他...


但是有其他的函数也非常欢迎提PR。


## 5. 激励
我们秉持做开源免费的项目。当然，若有获得赞助，我们会根据大家的贡献发bounty。

## 6. 社区支持
Openbuild
