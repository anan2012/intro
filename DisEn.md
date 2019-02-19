
# Lumens Distribution Decision Making

Dr Y. Wang

Northeastern University, Shenyang, China

Dr Y. Wang. Who receive a PhD in Computer Application Technology from Northeastern University, Shenyang, China. Her research interests include heterogeneous computing and parallel computing. Wang has published a lot of papers on SCI & EI Journals, including Computing in Science & Engineering, The Journal of Grey System and so on. Contact her at chengcheng0203@163.com.

**Abstract**：In order to distribute Lumens$^{[1]}$ effectively and achieve better distribution results, a two-stage distribution model is proposed. The model varies with time, which can be used smoothly by Lumens distribution strategy choosing. First, select suitable distribution objects. The weighted TOPSIS method is used to analyze and sort currencies in circulation. So suitable distribution objects are chosen. Next, the basic elements of distribution strategy are proposed on various perspectives, which constitute $2 ^ {6}$ distribution strategy. We deduce the ideal distribution strategy. Then the nearest one may serve as the optimal distribution strategy. The validity and adaptability of the proposed model will be verified either theoretically or experimentally. We will further analyze the stability of Stellar system before and after distribution in theoretical. The model would be used to simulate distribution in different scenarios, which results will be analyzed from the perspective of economics. 

**Keywords**：Lumens,Ditribution,Strategy,Stellar

## 1 Distribution Model
Ideally, we prefer the circumscances that Lumens is distributed to users who have enthusiasm on it. We expect its coverage and using range could be improved after distribution. And a positive impact on its flow would be produced. Howeverm, a fixed distribution strategy cannot adapt to various market conditions.

The paper analyses the basic situation of digital currencies in circulation, then chooses the currency suitable for Lumens distribution. After determining the distribution object, we propose multiple distribution strategies to distribute Lumens for the objects. Then a distribution strategy closest to the ideal strategy according to the simulation results is deduced. Therefore, the distribution and activity of holders can be significantly improved after distribution. In the paper, we propose a Lumens distribution model which varies with time,
$$
\Pi(\Theta,P).                                $$
Among of which, $\Theta$ is the object, $P$ is the strategy. $\Pi$ is the Lumens distribution model for $\Theta$ by $P$.

The model consists of two stages. (1) Analyze the basic situation of currency, and select objects for Lumens distribution. (2)Among several distribution strategies, an approximate optimal distribution strategy is deduced after comparison of the advantages and disadvantages of each strategy.
## 2 Choose Distribution Objects
$A$ is made from $\Upsilon$ 's attributions on $t$. Basic attribution: amount of holder address, circulation rate, turnover rate, ranking of circulation value. Deduced attribution: Dispersity. $A=（$$\Psi(\Upsilon,t)$， $N(\Upsilon,t)$ ，$\Chi(\Upsilon,t)$ ， $\Phi(\Upsilon,t)$  ， $\Omega(\Upsilon,t))$. $A$ is used for analyzing each currency.

Definition 1(Dispersity) It is the quantization of $\Omega(\Upsilon,t)$ 's distribution. It implicates the holding circumstances of $\Upsilon$ from the macro perspective.
$$
\Omega(\Upsilon,t)=\sqrt{\frac{1}{m}\sum_{i=1}^{m-1}(\Xi_{i}(\Upsilon,t)-\frac{N(\Upsilon,t)}{\Xi_{i}(\Upsilon,t)})^2}
$$

A smaller $\Omega(\Upsilon,t)$ stands for that $\Upsilon$ is more dispersed. It shows that $\Upsilon$ is well-distributed among all holders. A bigger $\Omega(\Upsilon,t)$ shows that $\Upsilon$ is held by a small part of holders. $\Upsilon$'s holding situation on $t$ can be expressed by choosing $\Upsilon$ from account $\Lambda(t)$. $\Xi(\Upsilon,t)$ is a holding account matrix.   

$$
\Xi(\Upsilon,t)=\Lambda(t)\land\Upsilon$$

The relation  $N^{'}(\Upsilon,t)=\sum\Xi(\Upsilon,t)$ is established.  $N^{'}(\Upsilon,t)$ is the total circulation of $\Upsilon$.

Decision analysis is carried out among a limited number of currencies$^{[2]}$. TOPSIS method$^{[3]}$ can analyze the original data flexibly and simply. It deduces the comprehensive disparity among different currencies accurately. At last, we will get a good comparability evaluation ranking. At the same time, because of the difference of attributes, different influence will act on results. Therefore, we use the weighted TOPSIS method to make analysis.

Make convergence treatment for $A$. The $A_0$ and $A_1$ of object $\Theta$ belong to high-priority attribute. The currency is better with a bigger amount of holder address, as well as a bigger circulation rate. $A_2$ belongs to neutral attibution. It could not guide the good or bad of a currency. $A_3$ and $A_4$ belong to low-priority. The currency would be in a bad situation with a smaller ranking of circulation value and a smaller Dispersity.

The original data matrix for $M$ attributes of $V$ evaluation objects is
$$ 
 \widetilde\Upsilon=\begin{bmatrix}\widetilde\Upsilon_0^0 & ...&\widetilde\Upsilon_0^{M-1}\\ ...& ...&...\\\widetilde\Upsilon_{V-1}^0 & ...&\widetilde\Upsilon_0^{M-1}\end{bmatrix}.
$$
It is obviously that $M=5$. $V$ is the numbert of currency chosen.

$A_2$ of $\widetilde\Upsilon$ is transfered to high-priority attribute by  $(\widetilde\Upsilon_i^j)^{'}=\frac{m}{m+|\widetilde\Upsilon_i^j-m|}$. 
$A_3$ and $A_4$ of $\widetilde\Upsilon$ are transfered to high-priority by $(\widetilde\Upsilon_i^j)^{'}=\frac{1}{\widetilde\Upsilon_i^j}$. Then we get the convergence matric $\widetilde\Upsilon^{'}$。  
Because attributes are in different dimensions and orders of magnitude. In order to eliminate the difference in the influence of attributes in decision-making process. $\widetilde\Upsilon^{'}$ should be normalized$^
{[4]}$.

For $A_0$ and $A_1$, let $(\widetilde\Upsilon_i^j)^{"}=\frac{\widetilde\Upsilon_i^j}{\sqrt{\sum(\widetilde{\Upsilon}_i^j)^2}}$. For$A_2$, $A_3$ and $A_4$, let $(\widetilde\Upsilon_i^j)^{"}=\frac{(\widetilde\Upsilon_i^j)^{'}}{\sqrt{\sum((\widetilde\Upsilon_i^j)^{'})^2}}$. Then an normalized attribute matrix $\widetilde\Upsilon^{"}$ is achieved 。

 An optimal and a worst ones of the finite schemes are deduced by $\widetilde\Upsilon^{"}$. They are also called as the optimal and worst vectors.
$$
Optimal:\widetilde{\Upsilon}^+=(max(\widetilde\Upsilon_i^0)^",max(\widetilde\Upsilon_i^1)^",...,max(\widetilde\Upsilon_i^{M-1})^")
$$
$$
Worst:\widetilde{\Upsilon}^-=(min(\widetilde\Upsilon_i^0)^",min(\widetilde\Upsilon_i^1)^",...,min(\widetilde\Upsilon_i^{M-1})^")
$$
Calculate the distances between the attribute value of all $V$ evaluation objects and the optimal scheme ($D_i^+$), as well as the worst scheme ($D_i^-$).  Because different subjects have different impact on the importance of attributes when choosing schemes, the weight coefficient $\lambda_j$ of $j$ will be used.
$$
D_i^+=\sqrt{\sum_{j=0}^{M-1}\lambda_j(\widetilde{\Upsilon}_i^+-\widetilde{\Upsilon}_i^j)^2}$$
$$
D_i^-=\sqrt{\sum_{j=0}^{M-1}\lambda_j(\widetilde{\Upsilon}_i^--\widetilde{\Upsilon}_i^j)^2}
$$

Calculate the proximity $C_i$ of all evaluation objects to $\widetilde{\Upsilon}^+$. $C_i\in[0,1)$. The closer the $C_i$ goes to 1, the closer the evaluation object $\widetilde{\Upsilon}_i$ is to the optimal scheme. So the closer the evaluation object is to the optimal level. The closer the $C_i$ goes to 0, the closer the evaluation object is to the worst level.
$$
C_i=\frac{D_i^-}{D_i^++D_i^-}
$$

Sort $\widetilde{\Upsilon}_i$ by $C_i$ on the whole. The larger the $C_i$ is, the better the object $\widetilde{\Upsilon}_i$ is. Then the approximate optimal solution $\widetilde{\Upsilon}_i$ can be obtained. Thus, the approximate optimal solution is selected as the base currency for distribution.
## **3 Multi- Objective Distribution Decision Making**
A basic distribution strategy must accurately describe the amount of distribution, distribution rules, snapshot time, deadline, and mode of collection. Further more, additional conditions and incentives should be made. Tabel 1 shows each item of basic distribution strategy with additional terms.

               Tabel 1 Basic items of distribution strategy

|          Item   |0                          |1                        |
|----------------|-------------------------------|-----------------------------|
|Amount|A proportion of Total Lumens | A proportion of transaction amount in a span of time|
|Rules      |According to holdig proportion  |According to holdig proportion. Some users are not included|
|Snapshot        |History time|Future time|
|Deadline       |Fixed|Infinity|
|Collection mode         |By hand|Generate new secret key|
|Additional condition       |Lock before distribution|Unlock before distribution|
|Additional incentive       |Reward high-quality accounts. Punish bad ones|No reward and punish|

$2^4$ distribution strategies can be derived according to the combination of the required options. There are at least 16 distribution strategies. We added additional options to the distribution strategy to generate $2^6$ distribution strategy. An optimized distribution strategy can improve Lumens'Dispersity, Circulation value, Amount of holding address, Account activity and Currency age after distribution. Therefore, the selection of distribution strategy is carried out under the constraints of multiple objectives and multiple conditions. Target Set $O=${Dispersity, CirValue, Amount of holding address, Account Activity, Currency Age}={$\Omega(\Upsilon,t)$, $\dot{\Psi}(\Upsilon,t)$, $\Zeta(\Upsilon,\Lambda)$, $\Beta(\Lambda)$, $\dot{M}(\Upsilon,\Lambda)$}.

Among of which, Account Activity is $\Beta(\Lambda)=\sum_{i=0}^{\Zeta(\Upsilon)-1}count(\Gamma,\Lambda)|\Delta t$. $\Gamma(\Upsilon,\Lambda)$is a transaction of $\Lambda$. $\Lambda$ is a discrete function of time, representing the currency held at any time and the corresponding amount $\Zeta$.
$$
\Lambda(t)=\begin{bmatrix}\Upsilon_0&\Zeta(\Upsilon_0,\Lambda)\\\ ...&...\\\Upsilon_{n-1}^0&\Zeta(\Upsilon_{n-1},\Lambda)\end{bmatrix}
$$

Definition 2 (Transaction $\Gamma(\Upsilon,\Lambda)$) Account $\Lambda$'s transaction for $\Upsilon$ on $t$. It contains 2 kinds of operation, In and Out. $\Gamma(\Upsilon,\Lambda)=\delta_i$, $\delta_i$ represents the amount of the transaction. $\delta_i>0$ represents In,     $\delta_i>0$ represents Out.
 
Definition 3 (Currency age $R(\Upsilon,\Lambda)$) For any account $\Lambda$, the time length of $\Upsilon$ held at time $t$ is called the age of $\Upsilon$. $R$ is an n*2 dimensional space vector. When the condition $Zeta ( Upsilon, Lambda) > 0$ is satisfied, $R=\{\Gamma(\Upsilon,\Lambda,t_j)|\delta_i>0\&t_0<t_j<t\}\bigotimes\{\Gamma(\Upsilon,\Lambda,t_j)|\delta_i<0\&t_0<t_j<t\}$. 

The Currency Age at $t$ is derivated by the following process. For transactions-Out, a deduction method is used. Deduct the Out-transactions from all In-transactions in $R$ according to the latest time method(filtered by the latest time $\bigotimes$).

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
R_0=\begin{bmatrix}\delta_1&t-t_1\\\ \delta_2-\delta_3&t-t_2\end{bmatrix},R_1=\begin{bmatrix}\delta_1&t-t_1\end{bmatrix},R_2=\begin{bmatrix}\delta_1-(\delta_3-\delta_2)&t-t_1\end{bmatrix}.
$$
Calculate the average age of a currency, $\dot{R}(\Upsilon,\Lambda)=\frac{\sum_{i=0}^{|R|}R(i,0)*R(i,1)}{\sum_{i=0}^{|R|}R(i,0)}$.

For any scheme $S_i$ of the $P$ schemes ($P=2^6$), the predicted values of $Q$ objectives $(Q=5)$ are derived. And the target value matrix $O(t)$ is obtained.
$$
O(t)=\begin{bmatrix}\Omega(\Upsilon,t)_0&\dot{\Psi}(\Upsilon,t)_0&\Zeta(\Upsilon,\Lambda)_0&Beta(\Lambda)_0&\dot{M}(\Upsilon,\Lambda)_0\\\ ...&...&...&...&...\\\Omega(\Upsilon,t)_{P-1}&\dot{\Psi}(\Upsilon,t)_{P-1}&\Zeta(\Upsilon,\Lambda)_{P-1}&Beta(\Lambda)_{P-1}&\dot{M}(\Upsilon,\Lambda)_{P-1}\end{bmatrix}
$$

Calculate the change rate of target's predicted value on $t$ compared with $t_0$, $\Delta O(t)$. $\Delta O_i^j(t)=\frac{O_i^j(t)-O_i^j(t_0)}{O_i^j(t_0)}$. Therefore，we get the best strategy on each target, $S^+=(O_0^+,O_1^+,...,O_{M-1}^+)=(max(\Delta O_i^0),max(\Delta O_i^1),...max(\Delta O_i^{Q-1}))$.
Calculate the distance between an arbitrary $S_i$ and the best strategy$S^+$, $\vec{S}=\sqrt{\sum_{j=0}^{M-1}\xi_j(O_i^+-O_i^j)^2}$. $\xi_j$ is the weight of target $j$.
Therefore, an approximate strategy $S_i$, $S_i=argmin_{S_i}(\vec{S_i})$ is deduced.

## 4 Further plans
（1）Analysis of the results of the distribution scheme

We prepare to use the model $Pi$ to make simulation for Lummens distribution for several times. We will make simulation for the market and account trends after distribution. We will make comparasion of the simulation results with two rounds of Lummens free distribution that have been carried out in October 2016 and August 2017$^{[5]}$.

（2）Improve account identification basis

We will make identification of the flow destination after distribution simulation. This will provide a basis for dentifying abusive accounts, valid accounts and high-quality accounts. The account identification is important in the additional incentive of distribution strategy.

（3）Stability analysis

Account stability analysis: We will make analysis for In frequency and amount, Out-frequency and amount of accounts in $\Delta t$ after distribution. Judge the stability of the account during this period.

System stability analysis: For Stellar network$^{[6]}$, distribution operation may lead to its disturbance. We will analyze the change rate of circulation in $\Delta t$. As well as the infuluence of total distribution on circulation. We will establish the state equation for system. We will use the Lyapunov stability theory$^{[7, 8]}$ to analyze whether the system can approach or return to its original equilibrium state after disturbance. So the stability of the system can be judged.

（4）Add trigger conditions for distribution

Make analysis for the dynamics of the Lummens holding account to decide whether to distribute and when to distribute.

References

1 https://www.stellar.org/lumens

2 C.L.Hwang and K.Yoon, Multiple Attributes Decision Making Methods and Applications, Springer, Berlin, 1981.

3 G.R.Jahanshahloo, F. H. Lotfi, and M. Izadikhah. Extension of the TOPSIS method for decision-making problems with fuzzy data. Applied Mathematics and Computation, 2006, 181(2):1544–1551.

4 Reverter, A., et al. Validation of alternative methods of data normalization in gene co-expression studies. Bioinformatics, 2005,21(7):1112-1120.

5 https://www.stellar.org/about/mandate/#Lumen_distribution

6 https://stellar.org 

7 V. Egorov and S. Mondi. Necessary conditions for the exponential stability of time-delay systems via the Lyapunov delay matrix. Nonlinear Analysis Hybrid Systems, 2014, 24(16): 1760-1771.

8 Liu X, Zhong S M, Ding X Y. Robust exponential stability of impulsive switched systems with switching delays: A Razumikhin approach. Communications in Nonlinear Science & Numerical Simulation, 2012, 17(4):1805-1812.