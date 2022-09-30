![](https://github.com/MarkMH/wealth_health/blob/1eee2f178f036ca226e7ec672ecc4fe690817010/images/banner_wealth_health.jpg)

<p align="justify" style="text-align:justify"> 
This is a replication study of [Schwandt, H. (2018). Wealth shocks and health outcomes: evidence from stock market fluctuations. <i>American Economic Journal: Applied Economics</i>, 10(4), 349-77]. The priject uses the same dataset but a different programming language for the data analysis. More specifically, the original work was done in Stata, while this project is done in Matlab. The data is available at: 
<br/><br/>

https://www.rand.org/well-being/social-and-behavioral-policy/centers/aging/dataprod/hrs-data.html 
</p>

---


<p align="justify" style="text-align:justify"> 
1. **UseHomotopy**: This file defines the non-degenerate bimatrix game to be solved. In the example below, each player has two strategies, the entries of the matrices are the payoffs of each player for every possible outcome. Please visit my personal website if you have not already, for more details, this is the example Game 2 described there. Solving the game using the homotopy function described below leads to a Nash equilibrium where players A and B both play the first strategy, represented by sigmaH1 and sigmaH2. If the Nash equilibrium reached, would have benn a mixed strategy equilibrium instead, the entries of sigmaH1 and sigmaH2 would be less than one, but both would add up to one.   
</p>


![](https://github.com/MarkMH/wealth_health/blob/1eee2f178f036ca226e7ec672ecc4fe690817010/images/data_demographics.png)

---

<p align="justify" style="text-align:justify"> 
2. **Homotopy**: This function is the actual algorithm. In addition to the payoff matrices defined above, this function requires a starting point, denoted by *j*, which can be an arbitrary strategy from the player's strategy space. With *w* we define the learning rate. 
</p>

![](https://github.com/MarkMH/wealth_health/blob/1eee2f178f036ca226e7ec672ecc4fe690817010/images/data_assumptions.png)

---

Disclaimer: This is one of my first projects, the coding is very primitive and redundant. Should you want to use it, I strongly advise to improve the style and efficiently before using the coding. 
</p>