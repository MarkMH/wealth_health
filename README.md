![](https://github.com/MarkMH/wealth_health/blob/1eee2f178f036ca226e7ec672ecc4fe690817010/images/banner_wealth_health.jpg)

<p align="justify" style="text-align:justify"> 
The data for this project is available at: 
<br/><br/>

https://www.rand.org/well-being/social-and-behavioral-policy/centers/aging/dataprod/hrs-data.html 
</p>


<p align="justify" style="text-align:justify"> 
<b>**Part 1**</b>: This file contains the required preprocessing steps. The sample is restricted to households that (i) were already retired in the previous wave of the questionnaire; (ii) begin and end the questionnaire in the same month, which allows controlling for fixed effects; and (iii) have lifetime wealth greater than $10,000. Lifetime wealth depends on life expectancy, value of business, net value of IRA, net value of stocks, mutual funds, value of checking and savings, net value of all other savings, net value of debt, and net value of primary residence and land ownership. Below are the sociodemographic scores for the corresponding sample:  
</p>


![](https://github.com/MarkMH/wealth_health/blob/1eee2f178f036ca226e7ec672ecc4fe690817010/images/data_demographics.png)

---

<p align="justify" style="text-align:justify"> 
The table below shows that the constraints on retirement and income have the most bite; in total, the resulting sample for the subsequent analysis includes 45120 observations. 
</p>

![](https://github.com/MarkMH/wealth_health/blob/1eee2f178f036ca226e7ec672ecc4fe690817010/images/data_assumptions.png)

---

<p align="justify" style="text-align:justify"> 
<b>**Part 2**</b>: This file constructs the <i>Wealth Shocks</i> according to: $\frac{s_{i,t-1}}{W_{i,t-1}}\cdot\frac{\bigtriangleup SP_{t}}{SP_{t-1}}$. Where $W_{i,t-1}$ is the previously mentioned lifetime wealth of subject $i$, $s_{i,t-1}$ is $i$'s past wave stock wealth and $\frac{\bigtriangleup SP_{t}}{SP_{t-1}}$ is the change in $S\&P500$ index between 2 waves. It is worth noting that the percentages were not reported in exact values until after 2004. Between 1998 and 2004, the percentages were measured on the basis of the respondent's answer to the question whether the IRA was invested "mostly in stocks," "mostly in interest-bearing assets," or "about evenly split." This is interpreted as 100 percent, 0 percent, and 50 percent invested in stocks, respectively. 
</p>

---

<p> 
<b>**Part 3**</b>: This file analysis the data according to the following empirical specification: 

$$
\bigtriangleup H_{i,t}=\alpha+\beta\frac{s_{i,t-1}}{W_{i,t-1}}\cdot\frac{\bigtriangleup SP_{t}}{SP_{t-1}}+\gamma\frac{s_{i,t-1}}{W_{i,t-1}}+\nu_{t}+\delta X_{i,t}+\varepsilon_{i,i}
$$
</p>

<p align="justify" style="text-align:justify"> 
Where $\bigtriangleup H_{i,t}$ is the change in health measures between two waves,  $W_{i,t}$ is the lifetime wealth, $\frac{s_{i,t-1}}{W_{i,t-1}}$ is pasts wave's share of lifetime wealth held in stocks, $\nu_{t}$ is a control for interview month and $X_{i,t}$ are several demographic controls such as age, gender, race, degree, region, cohort and past wave's marital status. Note that $i$ is an identifier for the individual household and $t$ for the corresponding wave.
</p>

<p align="justify" style="text-align:justify"> 
Note that for all following variables it applies that a lower value indicates a "healthier" household. RAND HRS offers several variables with different scales such as a "physical health index" consisting of integers between 0 and 7, a "mental health index" consisting of integers between 0 and 8, "self-report of health" consisting of integers between 1 and 5 as well as "self-report of health change" also consisting of integers between 1 and 5. For self-reported changes in health, RAND HRS offers dependent variables with 5 categories "much better", "somewhat better", "same", "somewhat worse", "much worse". This also applies analogously for self-reported health. All other regressands have values of either 0 or 1, these variables were collected asking whether a participant ever had high blood pressure, heart problem, diabetes, cancer or lung diseases. By the wording of the questionnnaire asking whether an individual ever had these conditions, one should assume that once one of these conditions takes a value of 1, the value should be one for each wave to come until the respondent dies. 
</p>

---

<p>
Disclaimer: This is one of my first projects, the coding is very primitive and redundant. Should you like to use it, I strongly advise to improve the style and efficiently before using the coding. 
</p>
