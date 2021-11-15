# Proof Systems for General Statements about Discrete Logarithms

摘要：

关于离散对数知识的证明系统是密码学中的一个重要的原语。我们确定了基本的基础技术，推广了这些技术来证明离散对数之间的线性关系，并提出了一种描述关于离散对数知识的复杂和一般陈述的符号。这种符号直接引出了一种构建有效的知识证明系统的方法。



## Introduction

这篇文章的目的是确定离散对数证明的基本技术并推广，规定一些符号用于离散对数问题证明，推导出有效的证明系统的方法

第二节：描述了离散对数和表示问题，并且定义了一些符号

第三节：非正式的定义了知识证明，并给出了基于离散对数的一些证明例子

第四节：定义并揭示了关于离散对数语句的符号

第五节：展示在给定规范下如何构建有效的证明系统

第六节：例子

第七节：总结

## Section2     Preliminaries

离散对数：

符号定义：

- α || β    表示两者连接
- *H{0,1}→{0,1}<sup>l</sup>* 哈希，把参数转化成固定 l 位的二进制串
- ξ ∈<sub>R</sub> X     表示从有限集合X中按均匀分布随机的选择一个数ξ



## Section3     Proofs of Knowledge

通俗的说，知识证明允许 *prover* 去让 *verifier* 相信他知道某个难以解决的问题的解决方法

导致以下三个属性

- 一个诚实的*prover*，知道一个解决方案，可以成功地说服*verifier*（完整性）

- 作弊的 *prover*无法说服 *verifier*（可靠性）

-  *verifier* 不获得过于*prover*值得的解决方案的有用信息（有用信息存在不同定义，如zero-knowledge 零知识，witness-hiding，minimum-disclosure 最小披露）

#### Example 1

为了证明y=g<sup>x</sup>对基g的离散对数的知识，prover计算了以下值:

![image-20211115222305015](C:\Users\Vking\AppData\Roaming\Typora\typora-user-images\image-20211115222305015.png)

​                                                                                            ![image-20211115222319266](C:\Users\Vking\AppData\Roaming\Typora\typora-user-images\image-20211115222319266.png)

其中规定一些说法为： *t* 承诺值 ， *c* 挑战值， *r* 响应

