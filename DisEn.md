
# Lumens Distribution Decision Making
**Abstract**：In order to achieve distribute Lumens effectively and achieve better distribution results, a two-stage distribution model is proposed. The model varies with time, which can be used smoothly by Lumens distribution strategy choosing.First, select suitable distribution object. The weighted TOPSIS method is used to analyze and sort the currencies in circulation. So suitable distribution objects are chosen. Next, the elements of distribution strategy are proposed on various perspectives, which constitute $2 ^ {6}$ distribution strategy. The ideal distribution strategy is deduced, and the nearest strategy may be served as the optimal distribution strategy. The validity and adaptability of the proposed model will be verified either theoretically or experimentally. We will further theoretically analyze the stability of Stellar system before and after distribution. The model would be used to simulate distribution in different scenarios,which results are analyzed from the perspective of economics.


## 1 Distribution Model
Ideally, we would like Lumens be distributed to users who have enthusiasm with Lumens. Its coverage and using range could be improved after distribution, as well as a positive impact on the flow would be produced. Howeverm, a fixed distribution strategy cannot adapt to different market conditions.

This paper analyses the basic situation of digital assets in circulation, then chooses the currency suitable for Lumens distribution. We propose multiple distribution strategies to distribute Lumens for the object after determining the distribution object. A distribution strategy closest to the ideal strategy according to the simulation results. Therefore, the distribution and activity of accounts can be significantly improved after distribution. In this paper, we propose a Lumens distribution model which varies with time.
$$
\Pi(\Theta,P).                                $$
Among of which, $\Theta$ is the object, $P$ is the strategy. $\Pi$ is the Lumens distribution model for $\Theta$ by $P$.

The model consists of two stages. (1) Analyzing the basic situation of currency and selecting objects for Lumens distribution. (2)Among several distribution strategies, an approximate optimal distribution strategy is deduced after comparation of the advantages and disadvantages of each strategy.
## 2 Choose Distribution Objects
A is made from $\Upsilon$ 's attributions on $t$. Basic attribution: number of holder address, circulation rate, turnover rate, ranking of circulation value. Deduced attrbution: dispersity. A=（$\Psi(\Upsilon,t)$， $N(\Upsilon,t)$ ，$\Chi(\Upsilon,t)$ ， $\Phi(\Upsilon,t)$  ，   $\Omega(\Upsilon,t)$). A is used for analyzing of each currency.

Definition 1(Dispersity) It is the quantization of $\Omega(\Upsilon,t)$ 's distribution. It implicates the holding circumstances of $\Upsilon$ from the macro perspective.
$$
\Omega(\Upsilon,t)=\sqrt{\frac{1}{m}\sum_{i=1}^{m-1}(\Xi_{i}(\Upsilon,t)-\frac{N(\Upsilon,t)}{\Xi_{i}(\Upsilon,t)})^2}
$$

A smaller $\Omega(\Upsilon,t)$ stands for that $\Upsilon$ is more dispersed. It shows that $\Upsilon$ is well-distributed among all holders. A bigger $\Omega(\Upsilon,t)$ shows that $\Upsilon$ is held by a small part of holders. $\Upsilon$'s holding situation on $t$ can be expressed by choosing $\Upsilon$ from account $\Lambda(t)$. $\Xi(\Upsilon,t)$ is a holding account matrix.   

$$
\Xi(\Upsilon,t)=\Lambda(t)\land\Upsilon$$

The relation  $N^{'}(\Upsilon,t)=\sum\Xi(\Upsilon,t)$ is established.  $N^{'}(\Upsilon,t)$ is the total circulation of $\Upsilon$.

Decision analysis is carried out among a limited number of currencies. TOPSIS method can analyze the original data flexibly and simply. It deduces the comprehensive disparity among different currencies accurately. At last, we will get a good comparability evaluation ranking. At the same time, because of the difference of attributes, different influence will act on results. Therefore, we use the weighted TOPSIS method to make analysis.

Make convergence treatment for A. The $A_0$ and $A_1$ of object $\Theta$ belong to high-priority attribute. The currency is better with a bigger number of holder address, as well as a bigger circulation rate. $A_2$ belongs to neutral attibution. It could not guide the good or bad of a currency. $A_3$，$A_4$ belong to low-priority. The currency would be in a bad situation with a smaller ranking of circulation value and a smaller dispersity.

The original data matrix for M attributes of V evaluation objects is
$$ 
 \widetilde\Upsilon=\begin{bmatrix}\widetilde\Upsilon_0^0 & ...&\widetilde\Upsilon_0^{M-1}\\ ...& ...&...\\\widetilde\Upsilon_{V-1}^0 & ...&\widetilde\Upsilon_0^{M-1}\end{bmatrix}.
$$
It is obviously that $M=5$. $V$ is the numbert of currency chosen.

$A_2$ of $\widetilde\Upsilon$ is transfered to high-priority attribute by  
$(\widetilde\Upsilon_i^j)^{'}=\frac{m}{m+|\widetilde\Upsilon_i^j-m|}$. 
$A_3$ and $A_4$ of $\widetilde\Upsilon$ are transfered to high-priority by $(\widetilde\Upsilon_i^j)^{'}=\frac{1}{\widetilde\Upsilon_i^j}$. Then we get the convergence matric $\widetilde\Upsilon^{'}$。  
Because attributes are in different dimensions and orders of magnitude. In order to eliminate the difference in the influence of attributes in decision-making process. $\widetilde\Upsilon^{'}$ should be normalized.

For $A_0$ and $A_1$, let $(\widetilde\Upsilon_i^j)^{"}=\frac{\widetilde\Upsilon_i^j}{\sqrt{\sum(\widetilde{\Upsilon}_i^j)^2}}$。For$A_2$, $A_3$ and $A_4$, let $(\widetilde\Upsilon_i^j)^{"}=\frac{(\widetilde\Upsilon_i^j)^{'}}{\sqrt{\sum((\widetilde\Upsilon_i^j)^{'})^2}}$. Then an normalized attribute matrix $\widetilde\Upsilon^{"}$ is achieved 。

 An optimal and a worst ones of the finite schemes are deduced by $\widetilde\Upsilon^{"}$. They are also called as the optimal and worst vectors.

Optimal:$\widetilde{\Upsilon}^+=(max(\widetilde\Upsilon_i^0)^",max(\widetilde\Upsilon_i^1)^",...,max(\widetilde\Upsilon_i^{M-1})^")$.

Worst:$\widetilde{\Upsilon}^-=(min(\widetilde\Upsilon_i^0)^",min(\widetilde\Upsilon_i^1)^",...,min(\widetilde\Upsilon_i^{M-1})^")$.

Calculate the distance between the attribute value of all $V$ evaluation objects and the optimal scheme ($D_i^+$), as well as the worst scheme ($D_i^-$).  Because different subjects have different opinions on the importance of attributes when choosing schemes, the weight coefficient $lambda_j$ of $j$ will be used.
$$
D_i^+=\sqrt{\sum_{j=0}^{M-1}\lambda_j(\widetilde{\Upsilon}_i^+-\widetilde{\Upsilon}_i^j)^2}$$
$$
D_i^-=\sqrt{\sum_{j=0}^{M-1}\lambda_j(\widetilde{\Upsilon}_i^--\widetilde{\Upsilon}_i^j)^2}
$$

Calculate the proximity $C_i$ of all evaluation objects to $\widetilde{\Upsilon}^+$. $C_i\in[0,1)$. The closer the $C_i$ goes to 1, the closer the evaluation object $\widetilde{\Upsilon}_i$ is to the optimal scheme. So the closer the evaluation object is to the optimal level. The closer the $C_i$ goes to 0, the closer the evaluation object is to the worst level.
$$
C_i=\frac{D_i^-}{D_i^++D_i^-}
$$
根据$C_i$对$\widetilde{\Upsilon}_i$进行总体排序。$C_i$越大，对象$\widetilde{\Upsilon}_i$越优。从而，近似最优解$\widetilde{\Upsilon}_i$
从而，近似最优解被选出作为分发的基础币种。


Sort $\widetilde{\Upsilon}_i$ by $C_i$ on  whole. The larger the $C_i$ is, the better the object $\widetilde{\Upsilon}_i$ is. Then,the approximate optimal solution $\widetilde{\Upsilon}_i$ can be obtained. Thus, the approximate optimal solution is selected as the base currency for distribution.
## **3 Multi- Objective Distribution Decision Making**
A basic distribution strategy must accurately describe the number of distribution, distribution rules, snapshot time, deadline, and mode of collection. Further more, additional conditions and incentives should be made. Tabel 1 shows two ways for each item on basic distribution strategy with additional terms.

|          Item   |0                          |1                        |
|----------------|-------------------------------|-----------------------------|
|Number|A part of Total Lumens | A proportion of transaction amount in a span of time|
|Rules      |According to holdig proportion  |According to holdig proportion. A part users are not included|
|Snapshot        |History time|Future time|
|Deadline       |Fixed|Infinity|
|Collection mode         |By hand|Generate new secret key|
|Additional condition       |Lock befor distribution|Unlock befor distribution|
|Additional incentive       |Reward high-quality accounts. Punish bad ones|No reward and punish|

Then $2^4$ distribution strategies can be derived according to the combination of the required options. And there are at least 16 distribution strategies. We added additional options to the distribution strategy to generate $2^6$ distribution strategy. An optimized distribution strategy can improve Lumens'Dispersity, Circulation value, Number of holding address, Account activity and Currency age after distribution. Therefore, the selection of distribution strategy is carried out under the constraints of multiple objectives and multiple conditions. Target Set O={Dispersity, CirValue, Number of holding address, Account Activity, Currency Age}={$\Omega(\Upsilon,t)$, $\dot{\Psi}(\Upsilon,t)$, $\Zeta(\Upsilon,\Lambda)$, $\Beta(\Lambda)$, $\dot{M}(\Upsilon,\Lambda)$}.

Among of which, Account Activity is $\Beta(\Lambda)=\sum_{i=0}^{\Zeta(\Upsilon)-1}count(\Gamma,\Lambda)|\Delta t$. $\Gamma(\Upsilon,\Lambda)$is a transaction of $\Lambda$. $\Lambda$ is a discrete function of time,representing the currency held at any time and the corresponding amount $\Zeta$.
$$
\Lambda(t)=\begin{bmatrix}\Upsilon_0&\Zeta(\Upsilon_0,\Lambda)\\\ ...&...\\\Upsilon_{n-1}^0&\Zeta(\Upsilon_{n-1},\Lambda)\end{bmatrix}
$$

Definition 2 (Transaction$\Gamma(\Upsilon,\Lambda)$) Account $\Lambda$'s transaction for $\Upsilon$ on $t$. It contains 2 kinds of operation, In and Out.$\Gamma(\Upsilon,\Lambda)=\delta_i$, $\delta_i$ represents the number of the transaction. $\delta_i>0$ represents In,$\delta_i>0$ represents Out.
 
Definition 3 (Currency age $R(\Upsilon,\Lambda)$) For any account $\Lambda$, the time length of $\Upsilon$ held at time $t$ is called the age of $\Upsilon$. $R$ is an n*2 dimensional space vector. When the condition $Zeta ( Upsilon, Lambda) > 0$ is satisfied, $R=\{\Gamma(\Upsilon,\Lambda,t_j)|\delta_i>0\&t_0<t_j<t\}\bigotimes\{\Gamma(\Upsilon,\Lambda,t_j)|\delta_i<0\&t_0<t_j<t\}$. 

The Currency Age at time $t$ is derivated by the following process. For transactions-Out, the deduction method is used. Deduct the Out transactions from all In transactions in $R$ according to the latest time (filtered by the latest time $\bigotimes$).

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
Calculate the average age of a currency, $\dot{R}(\Upsilon,\Lambda)=\frac{\sum_{i=0}^{|R|}R(i,0)*R(i,1)}{\sum_{i=0}^{|R|}R(i,0)}$.

For any scheme $S_i$ of the $P$ schemes ($P=2^6$), the predicted values of $Q$ objectives $(Q=5)$ are derived. And the target value matrix $O(t)$ is obtained.
$$
O(t)=\begin{bmatrix}\Omega(\Upsilon,t)_0&\dot{\Psi}(\Upsilon,t)_0&\Zeta(\Upsilon,\Lambda)_0&Beta(\Lambda)_0&\dot{M}(\Upsilon,\Lambda)_0\\\ ...&...&...&...&...\\\Omega(\Upsilon,t)_{P-1}&\dot{\Psi}(\Upsilon,t)_{P-1}&\Zeta(\Upsilon,\Lambda)_{P-1}&Beta(\Lambda)_{P-1}&\dot{M}(\Upsilon,\Lambda)_{P-1}\end{bmatrix}
$$

Calculate the change rate of target predicted value on $t$ compared with $t_0$ $\Delta O(t)$,$\Delta O(t)$. $\Delta O_i^j(t)=\frac{O_i^j(t)-O_i^j(t_0)}{O_i^j(t_0)}$. Therefore，we get the best strategy on each target, $S^+=(O_0^+,O_1^+,...,O_{M-1}^+)=(max(\Delta O_i^0),max(\Delta O_i^1),...max(\Delta O_i^{Q-1}))$。
Calculate the distance between an arbitrary $S_i$ and the best strategy$S^+$, $\vec{S}=\sqrt{\sum_{j=0}^{M-1}\xi_j(O_i^+-O_i^j)^2}$. $\xi$ is the weight of target $j$.
Therefor, an approximate strategy $S_i$,$S_i=argmin_{S_i}(\vec{S_i}) is deduced.

## 4 Further plans
（1）Analysis of the results of the distribution scheme

We prepare to use the model $Pi$ to make simulation for Lummens distribution for several times. We will make simulation for the market and account trends after distribution. We will make comparasion of the simulation results with two rounds of Lummens free distribution that have been carried out in October 2016 and August 2017.

（2）Improve account identification basis

We will make identification of flow destination after distribution simulation. This will provide a basis for dentifying abusive accounts, valid accounts and high-quality accounts. The account identification is important in the additional incentive of distribution strategy.

（3）Stability analysis

Account stability analysis: We will make analysis for In frequency and amount, Out frequency and amount of accounts in $\Delta t$ after distribution of the account are analyzed separately. Judge the stability of the account during this period.

System stability analysis: For Stellar network, distribution operation may lead to disturbance. We will analyze the change rate of circulation in $\Delta t$. As well as the infuluence of total distribution on circulation. We will establish the state equation for system. We will use the Lyapunov stability theory to analyze whether the system can approach or return to its original equilibrium state after disturbance. So the stability of the system can be judged.

（4）Add trigger conditions for distribution

Make analysis for the dynamics of the Lummens holding account to decide whether to distribute and when to distribute.

References

1 The Stellar Consensus Protocol: A Federated Model for Internet-level Consecus

2 TOPSIS ANALYSIS METHOD

3 Distributed System

4 Load Balance in Distributed System

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5OTIzNjcyNDVdfQ==
-->