
# Lumens Distribution Decision Making
**摘要**：为了实现Lumens的有效分发，达到良好的分发效果，本文提出了一个随时间变化的两阶段Lumens分发模型。首先，选取分发对象。使用加权TOPSIS方法对流通币种进行分析、排序。选出适合的分发对象。下一步，从多角度提出了分发策略的组成要素，构成了$2^{6}$种分发策略。推导出理想的分发策略，将距离理想分发策略最近距离的策略作为最优的分发策略。从而，推导出一个优化的分发模型。我们将进一步在理论上对Stellar系统在分发前后进行稳定性分析，并使用该模型在不同场景下进行模拟分发实验。从而，在理论和实验方面验证本文所提模型的有效性和适应性。
## 1 分发模型
理想的，Lumens如果能够分发到那些认可Lumens的用户。在分发后对能够增大Lumens的覆盖范围和使用范围，并对Lumens的流通产生积极的影响。固定的分发策略达到的效果会因不同市场行情而异。本文分析数字资产的基本情况，选择适合Lumens分发的币种。确定好Lumens分发对象后，提出使用多种分发策略为该对象分发Lumens，根据模拟的分发结果，得到一个最接近理想策略的分发策略。从而，在分发之后，能够使Lumens的分布情况、Lumens账户的活跃情况等具有明显的改善。本文提出一个随着时间而变化的Lumens分发模型，
$$
\Pi(\Theta,P) .                                     
$$其中，$\Theta$ 为分发对象，P为分发策略。$\Pi$ 为使用P为$\Theta$进行Lumens的分发模型。
该模型包括两个阶段：（1）分析币种的基本情况，为Lumens的分发选择分发对象。（2）提出多个分发策略，比较各策略的优劣，推导出近似最优的分发策略。
## 2 选择分发对象
将 t时刻币种$\Upsilon$的基本属性：持币地址数量，流通率，换手率，流通市值排名，以及推导属性：分散度，作为属性集A，A=（$\Psi(\Upsilon,t)$， $N(\Upsilon,t)$ ，$\Chi(\Upsilon,t)$ ， $\Phi(\Upsilon,t)$  ，   $\Omega(\Upsilon,t)$ ），对每个币种进行分析。
定义1 分散度  在t时刻，表示 $\Omega(\Upsilon,t)$  的分布情况的量化值。从宏观上反应了所有用户对$\Upsilon$ 的持有情况。
$$
\Omega(\Upsilon,t)=\sqrt{\frac{1}{m}\sum_{i=1}^{m-1}(\Xi_{i}(\Upsilon,t)-\frac{N(\Upsilon,t)}{\Xi_{i}(\Upsilon,t)})^2}
$$
$\Omega(\Upsilon,t)$越小，表示 $\Upsilon$越分散，说明 $\Upsilon$在所有的持有地址中分布的越均匀。而该数值越大，则 $\Upsilon$越集中到少量地址中。
其中，t时刻链上 $\Upsilon$的持币情况为从账户  $\Lambda(t)$中选择$\Upsilon$的元素。$\Xi(\Upsilon,t)$为持币账户矩阵。
$$
\Xi(\Upsilon,t)=\Lambda(t)\land\Upsilon$$并且，满足关系:$\Upsilon$的流通总量 $N^{'}(\Upsilon,t)=\sum\Xi(\Upsilon,t)$。
在有限数量的币种之中进行决策分析。TOPSIS法能够灵活简单的对原始数据进行充分分析，得到能够精确反应各币种之间的综合差距，得出良好的可比性的评价排序。同时，由于不同属性之间的差异性，对结果的影响力的不同，我们使用加权的TOPSIS法进行分析。
将属性趋同化处理，分发对象$\Theta$的$A_0$ ，$A_1$属于高优属性。持币地址数量越多，流通率越高，则该币种的状态越优。$A_2$属于中性属性，$A_2$不能明确导向币种的优劣.$A_3$，$A_4$属于低优属性。流通市值排名越小，币的分散度越小，则该币种的状态越差。
对于N个评价对象的M个属性，构成的原始数据：
$$ 
 \widetilde\Upsilon=\begin{bmatrix} \widetilde\Upsilon_0^0 & ...&\widetilde\Upsilon_0^{M-1}\\ ...& ...&...\\\widetilde\Upsilon_{N-1}^0 & ...&\widetilde\Upsilon_0^{M-1}\end{bmatrix}
$$
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEyMzMzNDY0MzBdfQ==
-->