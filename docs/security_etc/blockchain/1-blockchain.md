---
comments: true
--- 

## 比特币(Bitcoin)

> 区块链源于比特币，先简单说说比特币

比特币是一种数字货币, 有以下特性:

- **去中心化** 没有中心的服务器，不受某个人的控制，整个系统直接由用户端电脑构成
- **数据防篡改** 所有交易记录[全量存储](https://www.google.com/search?q=%E5%85%A8%E9%87%8F%E4%BF%9D%E5%AD%98&oq=%E5%85%A8%E9%87%8F%E4%BF%9D%E5%AD%98&gs_lcrp=EgZjaHJvbWUyBggAEEUYOTIKCAEQABiABBiiBDIKCAIQABiABBiiBDIKCAMQABiABBiiBDIKCAQQABiABBiiBNIBCDg4MDBqMWo3qAIAsAIA&sourceid=chrome&ie=UTF-8#:~:text=%E6%AF%8F%E5%A4%A9%E5%AD%98%E5%82%A8%E6%9C%80%E6%96%B0%E4%B8%80%E5%A4%A9%E5%85%A8%E9%87%8F%E6%95%B0%E6%8D%AE%EF%BC%8C%E6%AF%8F%E5%A4%A9%E5%9C%A8%E6%BA%90%E7%B3%BB%E7%BB%9F%E5%85%A8%E9%87%8F%E6%8F%90%E5%8F%96%E6%9C%80%E6%96%B0%E6%95%B0%E6%8D%AE%EF%BC%8C%E8%BF%9B%E8%A1%8C%E5%AD%98%E5%82%A8)，并公开给所有的人，而且还被加密和校验
- **固定的发行量**

去中心化的比特币 **交易处理流程:**

1. 用户先把交易传到网络中
2. 网络上会有一些机器叫记账结点，它们通过 **比拼计算力** 的方式竞争记账权。这称为 **挖矿**
3. 获得记账权的结点，会把待记账的交易进行计算打包，并向全网广播。收到新的记账包的结点会对其进行验证，验证通过后加入自己的区块

*PS: 比特币世界没有服务器，完全是靠大家用自己的电脑拼出来的一个分布式系统*

故前提假设是: ^^网络中的任何结点都是不能信任的，每一个都可能会作恶^^

进一步说这个分布式账本系统需要: 任何人都可以拿到所有的数据，即数据要能很容易被验证是合法的，没有被修改过的，而且也要很难被人修改的

故比特币用了两大技术 :  ==区块链技术 & 工作量证明共识机制==


## 工作量证明的共识机制

!!! Question

    在分布式系统中结点是被信任的，而去中心化的网络中则不可信任，那如何保证数据一致性？

数据一致 --> ^^和谁的数据一致？以谁为标准？^^

- "大部分认同的数据即是对的"  --> **Proof-of-Work工作量证明机制** 即 ==**挖矿**==
- 用大规模的计算来找到一个符合系统要求的区块ID
    * 要找到相应ID只能暴力穷举，故要付出系统的大量计算资源和电力