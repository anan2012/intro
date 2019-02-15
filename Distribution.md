
# Lumens Distribution Decision Making
**摘要**：为了实现Lumens的有效分发，达到良好的分发效果，本文提出了一个随时间变化的两阶段Lumens分发模型。首先，选取分发对象。使用加权TOPSIS方法对流通币种进行分析、排序。选出适合的分发对象。下一步，从多角度提出了分发策略的组成要素，构成了$2^{6}$种分发策略。推导出理想的分发策略，将距离理想分发策略最近距离的策略作为最优的分发策略。从而，推导出一个优化的分发模型。我们将进一步在理论上对Stellar系统在分发前后进行稳定性分析，并使用该模型在不同场景下进行模拟分发实验。从而，在理论和实验方面验证本文所提模型的有效性和适应性。
## 1 分发模型
理想的，Lumens如果能够分发到那些认可Lumens的用户。在分发后对能够增大Lumens的覆盖范围和使用范围，并对Lumens的流通产生积极的影响。固定的分发策略达到的效果会因不同市场行情而异。本文分析数字资产的基本情况，选择适合Lumens分发的币种。确定好Lumens分发对象后，提出使用多种分发策略为该对象分发Lumens，根据模拟的分发结果，得到一个最接近理想策略的分发策略。从而，在分发之后，能够使Lumens的分布情况、Lumens账户的活跃情况等具有明显的改善。本文提出一个随着时间而变化的Lumens分发模型，
$$
\Pi(\Theta,P) .                                     
$$
其中，$\Theta$ 为分发对象，P为分发策略。$\Pi$ 为使用P为$\Theta$进行Lumens的分发模型。
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
\Xi(\Upsilon,t)=\Lambda(t)\land\Upsilon$$
并且，满足关系:$\Upsilon$的流通总量 $N^{'}(\Upsilon,t)=\sum\Xi(\Upsilon,t)$。
在有限数量的币种之中进行决策分析。TOPSIS法能够灵活简单的对原始数据进行充分分析，得到能够精确反应各币种之间的综合差距，得出良好的可比性的评价排序。同时，由于不同属性之间的差异性，对结果的影响力的不同，我们使用加权的TOPSIS法进行分析。
将属性趋同化处理，分发对象$\Theta$的$A_0$ ，$A_1$属于高优属性。持币地址数量越多，流通率越高，则该币种的状态越优。$A_2$属于中性属性，$A_2$不能明确导向币种的优劣.$A_3$，$A_4$属于低优属性。流通市值排名越小，币的分散度越小，则该币种的状态越差。

对于V个评价对象的M个属性，构成的原始数据：
$$ 
 \widetilde\Upsilon=\begin{bmatrix}\widetilde\Upsilon_0^0 & ...&\widetilde\Upsilon_0^{M-1}\\ ...& ...&...\\\widetilde\Upsilon_{V-1}^0 & ...&\widetilde\Upsilon_0^{M-1}\end{bmatrix}
$$

显然，其中M=5。V为选取的币种数量。
使用$(\widetilde\Upsilon_i^j)^{'}=\frac{m}{m+|\widetilde\Upsilon_i^j-m|}$将$\widetilde\Upsilon$的中性属性$A_2$转化为高优属性。使用$(\widetilde\Upsilon_i^j)^{'}=\frac{1}{\widetilde\Upsilon_i^j}$将$\widetilde\Upsilon$中的低优属性$A_3$，$A_4$转化为高优属性。从而得到属性趋同矩阵$\widetilde\Upsilon^{'}$。

由于属性处于不同量纲的和数量级。为了消除属能够在决策过程中的影响的差异化。对$\widetilde\Upsilon^{'}$进行归一化处理。

对$A_0$ ，$A_1$，令$(\widetilde\Upsilon_i^j)^{"}=\frac{\widetilde\Upsilon_i^j}{\sqrt{\sum(\widetilde{\Upsilon}_i^j)^2}}$。对$A_2$ ，$A_3$，$A_4$令$(\widetilde\Upsilon_i^j)^{"}=\frac{(\widetilde\Upsilon_i^j)^{'}}{\sqrt{\sum((\widetilde\Upsilon_i^j)^{'})^2}}$。得到归一化处理后的指标矩阵$\widetilde\Upsilon^{"}$。

根据$\widetilde\Upsilon^{"}$得到有限方案的最优方案和最劣方案，即最优值向量和最劣值向量。

最优方案:$\widetilde{\Upsilon}^+=(max(\widetilde\Upsilon_i^0)^",max(\widetilde\Upsilon_i^1)^",...,max(\widetilde\Upsilon_i^{M-1})^")$。

最劣方案:$\widetilde{\Upsilon}^-=(min(\widetilde\Upsilon_i^0)^",min(\widetilde\Upsilon_i^1)^",...,min(\widetilde\Upsilon_i^{M-1})^")$。

计算V个评价对象的属性值与最优方案距离和最劣方案的距离,$D_i^+$,$D_i^-$。由于在做方案选择时，不同的主体对属性的重要程度有不同的认识,令$\lambda_j$为指标j的权重系数。
$\widetilde{\Upsilon}_i$
$$
D_i^+=\sqrt{\sum_{j=0}^{M-1}\lambda_j(\widetilde{\Upsilon}_i^+-\widetilde{\Upsilon}_i^j)^2}$$
$$
D_i^-=\sqrt{\sum_{j=0}^{M-1}\lambda_j(\widetilde{\Upsilon}_i^--\widetilde{\Upsilon}_i^j)^2}
$$
计算V个评价对象与$\widetilde{\Upsilon}^+$的接近程度$C_i$，$C_i\in[0,1)$。$C_i$越趋进1，评价对象$\widetilde{\Upsilon}_i$越接近最优水平。$C_i$越趋进0，评价对象越接近最劣水平。 
$$
C_i=\frac{D_i^-}{D_i^++D_i^-}
$$
根据$C_i$对$\widetilde{\Upsilon}_i$进行总体排序。$C_i$越大，对象$\widetilde{\Upsilon}_i$越优。从而，近似最优解$\widetilde{\Upsilon}_i$被选出作为分发的基础币种。

## 3 Multi- Objective Distribution Decision Making

一个基本的分发策略必须对分发数量，分发规则，快照时间，截止时间，领取方式进行准确的描述。此外，可以对分发做附加条件和附加的奖励。本文结合基本的分发策略以及附加的条款，对每个条目给出了两种方式，表1所示。
|           选项    |0                          |1                        |
|----------------|-------------------------------|-----------------------------|
|分发数量|Lumens总量的一定比例            |根据Lumens一段时间的交易量，分发该交易量的一定比例           |
|分发规则         |按分发对象的持仓比例            |按分发对象持仓比例，过滤部分用户           |
|快照时间         |历史时间|未来时间|
|截止时间         |固定|无限|
|领取方式         |手动领取|生成新密钥|
|附加条件         |分发前锁仓|分发前不锁仓|
|附加奖励        |识别优质账户，给予奖励。识别劣质账户，给予惩罚|无奖励和惩罚|

则根据必选项的组合情况能够衍生出$2^4$种分发策略，则分发策略至少有16种。我们将附加的可选项加入到分发策略中，共生成$2^6$种分发策略。一个优化的分发策略，在分发后，能够使Lumens的分散度，流通市值，地址数量，账户活跃度，币龄等方面有所改善。因此，分发策略的选择是在多个目标的约束下，以及多个条件的限制下进行的。目标集O={分散度，流通市值，持币地址数量，账户活跃度，币龄}={$\Omega(\Upsilon,t)$,$\dot{\Psi}(\Upsilon,t)$,$\Zeta(\Upsilon,\Lambda)$，$\Beta(\Lambda)$，$\dot{M}(\Upsilon,\Lambda)$}。

其中,$\Beta(\Lambda)=\sum_{i=0}^{\Zeta(\Upsilon)-1}count(\Gamma,\Lambda)$为$\Lambda$的一次交易。$\Lambda$是对时间的离散函数，表示在任意时刻持有的币种以及相应的数量$\Zeta$。
$$
\Lambda(t)=\begin{bmatrix}\Upsilon_0&\Zeta(\Upsilon_0,\Lambda)\\\ ...&...\\\Upsilon_{n-1}^0&\Zeta(\Upsilon_{n-1},\Lambda)\end{bmatrix}
$$

定义2 交易$\Gamma(\Upsilon,\Lambda)$  账户$\Lambda$的在t时刻对$\Upsilon$的交易。包括2种操作，转入和转出。$\Gamma(\Upsilon,\Lambda)=\delta_i$。$\delta_i$为该笔交易的数量，$\delta_i>0$表示转入，$\delta_i<0$表示转出。

定义3 币龄$R(\Upsilon,\Lambda)$  对于任意账户$\Lambda$，在t时刻持有的$\Upsilon$的时间长度称为$\Upsilon$的年龄。$R$是一个n*2维的空间向量。当满足条件$\Zeta(\Upsilon,\Lambda)>0$时，$R=\{\Gamma(\Upsilon,\Lambda,t_j)|\delta_i>0\&t_0<t_j<t\}\bigotimes\{\Gamma(\Upsilon,\Lambda,t_j)|\delta_i<0\&t_0<t_j<t\}$。
t时刻的币龄使用下列演算过程，对于转出的交易，使用抵扣法。将转出的交易与$R$中的所有转入交易按照最近时间的进行抵扣（最近时间过滤$\bigotimes$）。
$$
\Gamma(\Upsilon,t_1,\Lambda),\delta_1>0,R(\Upsilon,\Lambda)=[\Gamma(\Upsilon,t_1,\Lambda),t-t_1]=[\delta_1,t-t_1]
$$
$$
\Downarrow$$
$$
\Gamma(\Upsilon,t_2,\Lambda),\delta_2>0,R(\Upsilon,\Lambda)=\begin{bmatrix}\delta_1&t-t_1\\\ \delta_2&t-t_2\end{bmatrix}
$$
$$  
\bigotimes
$$
$$
\Gamma(\Upsilon,t_3,\Lambda),\delta_3<0,R(\Upsilon,\Lambda)=\begin{Bmatrix} R_0 & \delta_2>\delta_3 \\ R_1& \delta_2=\delta_3 \\ R_2& \delta_2<\delta_3 \end{Bmatrix}\\,
R_0=\begin{bmatrix}\delta_1&t-t_1\\\ \delta_2-\delta_3&t-t_2\end{bmatrix},R_1=\begin{bmatrix}\delta_1&t-t_1\end{bmatrix},R_2=\begin{bmatrix}\delta_1-(\delta_3-\delta_2)&t-t_1\end{bmatrix}。
$$
计算账户中持有的币的平均年龄，$\dot{R}(\Upsilon,\Lambda)=\frac{\sum_{i=0}^{|R|}R(i,0)*R(i,1)}{\sum_{i=0}^{|R|}R(i,0)}$。
针对P种方案（P=$2^6$）的任意方案$S_i$，推导出Q个目标（Q=5）的预测值，得到目标值矩阵O(t）。
$$
O(t)=\begin{bmatrix}\Omega(\Upsilon,t)_0&\dot{\Psi}(\Upsilon,t)_0&\Zeta(\Upsilon,\Lambda)_0&Beta(\Lambda)_0&\dot{M}(\Upsilon,\Lambda)_0\\\ ...&...&...&...&...\\\Omega(\Upsilon,t)_{P-1}&\dot{\Psi}(\Upsilon,t)_{P-1}&\Zeta(\Upsilon,\Lambda)_{P-1}&Beta(\Lambda)_{P-1}&\dot{M}(\Upsilon,\Lambda)_{P-1}\end{bmatrix}
$$

与$t_0$时刻相比，计算时刻t的目标预测值的变化率$\Delta O(t)$,$\Delta O_i^j(t)=\frac{O_i^j(t)-O_i^j(t_0)}{O_i^j(t_0)}$。从而得到，每个目标下的理想方案$S^+=(O_0^+,O_1^+,...,O_{M-1}^+)=(max(\Delta O_i^0),max(\Delta O_i^1),...max(\Delta O_i^{Q-1}))$。
计算任意方案$S_i$与理想方案$S^+$的距离$\vec{S}=\sqrt{\sum_{j=0}^{M-1}\xi_j(O_i^+-O_i^j)^2}$。$\xi$为目标j的权重。
从而，可以推导出近似最优的方案$S_i$,$S_i=argmin_{S_i}(\vec{S_i})$ 。
## 4 下一步工作计划
（1）分析分发方案的结果

    使用模型$\Pi$对Lumens 进行模拟分发，得出分发后的市场动向和账户动向等结果，将使用该模型分发与2016年10月和2017年8月已经进行的2轮免费分发结果进行对比。
（2）增加账户识别依据

将分发后Lumens的流向目的地识别，为分发策略的附加奖励中识别出滥用账户，有效账户，和优质账户提供依据。

（3）稳定性分析

账户稳定性分析：对于账户分发后的$\Delta t$时间内，其转出频率、数量和转入频率、数量等进行分分析。判断该账户在该段时间的稳定性。
系统稳定性分析：对于Stellar网络，分发操作对系统触发了扰动后的$\Delta t$时间内，分析流通率的增幅，与分发总量带给分发前流通率的影响。建立系统的状态方程，使用李雅谱诺夫稳定性理论分析该系统在受到扰动后是否能趋近或返回到原来的平衡状态。从而判断系统的稳定性。

（4）增加分发的触发条件

根据恒星的持有账户的动态，对持有账户进行分析，来决策是否分发和分发时机。


