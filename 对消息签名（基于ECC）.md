## 对消息签名（基于ECC）

#### 两个实体

- Signer  U
- Verifier  V

#### 场景

当U想要诚实的发送一个消息M，同时V想要验证M的真实性时使用该签名方案

实际上对于一则消息M，任何拥有U的公钥的实体V都可以对该消息进行验证。

#### U and V之间的交互过程

First U and V should use the setup procedure to establish which options to use the scheme with, then U should use the key deployment procedure to selecta key pair and V should obtain U's public key —U will use the key pair to control the signing operation， and V will use the public key to control the verifying operation. Then,each time U wants to send a message M , entity U should apply the signing operation to M under its key pair to obtain a signature S on M , form a signed message from M and S, and convey the signed message to V. Finally,when V receives the signed message,entity V should apply the verifying operation to the signed message under U's public key to verify its authenticity. If the verifying operation outputs“valid”, entity V concludes the signed message is indeed authentic.

#### 两种签名方案

- 带有appendix，U要发送M和S
- 消息可恢复，U只需要发送S

#### Elliptic Curve Digital Signature Algorithm（ECDSA 椭圆曲线数字签名算法）

是一种基于椭圆曲线密码体制的带附件的签名方案

##### 方案初始化

1. *Hash* 表示哈希函数，*Hashlen*表示生成的八进制哈希值

2. U去建立椭圆曲线域参数 T = *(p,a,b,G,n,h)*或者 T = *(m,f(x),a,b,G,n,h)* 
3. V去获得*Hash* 和参数T

##### 密钥生成

1. U生成密钥对(d~U~ ,Q~U~ ) 
2. V获取U的公钥Q~U~ 

##### 签名过程

