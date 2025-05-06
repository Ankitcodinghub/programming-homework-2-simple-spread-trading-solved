# programming-homework-2-simple-spread-trading-solved
**TO GET THIS SOLUTION VISIT:** [Programming Homework 2-Simple Spread Trading Solved](https://www.ankitcodinghub.com/product/programming-homework-2-simple-spread-trading-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;97955&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;Programming Homework 2-Simple Spread Trading Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Simple Spread Trading

A spread trading strategy checks a running estimate of the displacement between two related instruments, and makes bets that this displacement will decline whenever it gets large. Here, we define that displacement in terms of recent returns.

2 Data

Obtain split- and dividend-adjusted closing prices1 for 2 Dec 2019 though 31 Dec 2021 of a pair of ETFs (which we will call X and Y ) as specified below. Estimate daily dollar volume, compute the running trailing 15-trading-day median of it over our sample period for X, and denote that running median (as of any day given t) for the less liquid of the two ETFs with the expression Nt.

Nt :=Median[{Vt−16,Vt−15,…,Vt−1}] (1) Obtain daily Fama-French factor returns2 (SMB, HML, RF and Mkt-RF)

over the same data period.

1The Quandl EOD database and Bloomberg are the best two sources for this. 2Available on Ken French’s website

1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
3 Exercise 3.1 Positions

Create code for a spread-reversion trading strategy that begins on the first day of each month, trades during the month, and closes any open positions the end of each month (i.e. the first potential day for a trade is just after January 1 2020). For this homework, make the unrealistic assumption that you can trade at end-of-day closing prices from the database.

Its trades are equal-sized dollar amounts of X and Y to the nearest integer number of shares, as close as possible to $Nt/100 of each. Note that Nt changes every day, so trade size will depend on which day you open the position. Your gross traded cash is therefore roughly $2Nt/100. Track this number on any open position for later stop loss calculations.

The strategy enters or maintains a position if the size s of difference between the M-day return on X and Y is greater than g, and flattens (exits) the position if the size of the difference is less than j (where j &lt; g). It does so by shorting the security whose recent return is higher. Note that if the change in s is large enough the position can flip from shorting the spread to being long the spread and vice versa, as discussed in class.

You only ever hold, at most, one long and one short position (i.e. one spread position). If you already have a position and the next tick is favorable to it, this simply means you continue to hold the position (except in stop loss situations). Do not adjust position size with the new Nt.

3.2 Mark To Market

When a position is open, keep track of its profits/losses (PnL). You will also want to keep track of cumulative PL across the whole series of opened and closed positions.

3.3 Stop Loss

Include a stop loss parameter s in your strategy. If your simulation ex- periences a day such that the present position value has lost more than a proportion s of the gross traded cash (|$long| + |$short| at position entry time), then force an exit at current prices, assume no new positions for the remainder of the month, and include this in your accounting.

2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
3.4 End Of Data

Force a position close at the end of the analysis period.

3.5 Capital

Set the capital K for your strategy to the maximum of Nt over the data period, times two3. You can use this to evaluate return on capital.

</div>
</div>
<div class="layoutArea">
<div class="column">
3This setting has lookahead bias but is good enough for now. We set it very large like this to avoid the nonsensical situation of negative capital.

3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
3.6 Data

ETF pairs X,Y (in order) are as given by the last digit of your student number as follows:

0. FCOM VOX 1. RYE XOP 2. PXJ OIH

3. RYU XLU 4. RTH XRT 5. SIVR SLV 6. HYLD JNK 7. RING GDX 8. FTSL SMH 9. PBE XBI

4 Analysis

Study the performance of your strategy as you vary j, g, s, and M. Include plots. You need not run a fancy nonlinear optimizer, but try to find which parameters work well, and explain how you did it. For one or more of the better settings you find, look into correlations to Fama French factor returns.

Be sure to highlight which ETF pair you are analyzing.

</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
