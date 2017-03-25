
# Battery Storage Technology Key Advantages and Challenges

The following section sets out the key advantages and challenges of using a battery system. By understanding the value of battery technology in a University context, a leveraged system strategy was produced. The literature review in section \ref{background-and-summary-of-key-work-and-reference} identified key areas of further research, where their understanding is paramount to overcoming many of the challenges of using battery storage. Through developing this detailed understanding, a viable model of an optimised battery system could then be designed. This report aims to create strong arguments to how the system will overcome all challenges, laying out how all the assumptions in the model overcome these issues.

\begin{table}[H]
\centering
\includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{AdChallTab2.pdf}
\caption{Showing the Advantages and Challenges of Using Energy Storage}
\label{AdChalltab}
\end{table}


## Battery Economics
The primary objective of this project is to create a cost-based analysis business case for using a battery system. Ultimately the model will evaluate whether to invest in a battery storage system, finding the best solution based on an energy profile. There are three ways the model will assess the value of the storage system; *pay-back period*, *total-savings* (over a selected period) and *net present value* (calculated for different discount rates). Each of these methods results will be compared, crediting their merits and pitfalls, to give a full understanding of the battery's value.

### Net Present Value
Net Present Value (NPV) describes the difference between the current value of cash inflows and outflows \cite{NetPrese35:online}. NPV is used in capital budgeting to analyse the profitability of an investment acting as a useful tool for understanding the long-term value of a battery system.  Batteries are a significant upfront investment, seeing little financial value for many years. As a consequence, purchasing the battery through finance is likely, adding a loan's interest to the cost of the battery.  The battery will also degrade in performance over time, reducing the value it can generate.  Both of these factors, increase the discount rate required to correctly value to the batteries financial performance over time on top of interest rate (a traditional metric used)

The Initial Return Rate (IRR) is a method for finding the maximum discount rate before that an asset generates a negative NPV. This is found by setting the net present value to 0 and calculating the return rate. Equation \ref{eq:IRR}, defines the secant numerical method used for calculating the IRR.
\begin{align}
r_{ n+1 }=r_{ n }-{ NPV }_{ n }\cdot \left( \frac { r_{ n }-r_{ n-1 } }{ { NPV }_{ n }-{ NPV }_{ n-1 } }  \right)
\label{eq:IRR}
\end{align}
Where $r_{ n }$ defines the $n^{th}$ approximation of the IRR \cite{xxxdvi44:online}.

Using Equation \ref{eq:IRR} the maximum discount rate can be found using batteries at the extremities of the results (lowest and highest performers). The IRR can be used to select appropriate different discount rates, where zero is used to illustrate the payback of the battery. After selecting an appropriate discount rate, if the NPV of a system is found to be positive, then the investment is predicted hold greater value than the expenditures associated with ownership of the system. Whereas, a negative NPV indicates that there is no financial benefit in the system, although unquantified benefits may be present \cite{diorio2015economic}. Total savings is the measure of NPV when the discount rate is zero; providing a better understanding of the actual cash flow which the system generates and is a simple measure of the system's value.

### Payback Period
The Payback Period (PBP) is the time in years for project savings to equal or exceed the initial cost of the investment  \cite{diorio2015economic}. This metric is useful due to its ability to communicate the tangible value of a project. A system which yields a short payback period is typically profitable because subsequent years of the project result in positive revenue for the system owner. Long payback periods make the battery a poor investment; money may still be owed if the system is retired. Reducing the payback period diminishes many risks associated with the batteries challenges. The batteries lifetime will have a warranty, meaning that if the battery were to fail before this time, there is no financial cost in replacement/repair.

As the battery will be viewed first as a financial investment by the University, having a short enough payback period will be essential to proving the battery systems viability.

## Li-ion Battery Costing

Over the last decade, Li-ion technology has advanced significantly, partly due to the rise in electric vehicles; resulting in slashing the price of batteries while improving their efficiency and energy density.  Figure \ref{mckBatPrice} shows the trend in prices for the last six years and the predictions for the next 15. Between 2010 to 2016, battery pack prices fell by roughly 80% from $1,000/kWh to  $227/kWh. Current projections put the price of Li-ion battery pack prices below $190/kWh by the end of the decade, corresponding with the construction of the new campus, an additional 16\% reduction from today prices.  By 2030 it is suggested the battery pack prices will fall below $100/kWh. The result means that the feasibility of investing in the technology will continue to increase.  

\begin{figure}[H]
  \centering
  \includegraphics[trim = 0 0 0 0, clip, width=0.4\textwidth]{mckBatPrice.png}
  \caption{Plot of Battery Prices Reduction for 2010-2016 and Predictions for Future battery Prices \cite{mckBat}}
  \label{mckBatPrice}
\end{figure}

Tesla's Li-ion Powerpack 2 was selected due to its claims in technology advancement but also due to the abundance of information on its products costing. Tesla's website makes data readily available on the purchase cost of the battery with inbuilt inverters, based on the battery's capacity (kWh) and maximum power (kW). This data makes it possible to evaluate the optimum specification of battery for an energy profile. Unit costs start at £51,940 and scale infinitely.  

After purchasing the product, installation is the next largest cost to consider. This cost will be significantly greater when retrofitting to existing infrastructure although the technology comes as almost plug and play, assume will need to be connected to where the mains supply enters the building to work in tandem with mains supply. Building a suitable foundation is also necessary due for the battery to be installed outside. In the case of the new campus, it is assumed that there are little additional costs in installing the battery system due to installation requirements, placed on the site's design.

Maintenance is another factor when looking over the lifespan of the product. As there are no moving mechanical parts, any issues with the ESS will likely be with the cells themselves. These will likely need to be replaced, rather than repaired. Telsa gives a ten-year warranty on their batteries, alleviating any risk on large maintenance costs for this period.  The Powerpack control system uses many sensors for systems health checking, requiring little training to monitor the battery. It seems likely that the University can use a member of the Estates team monitor the battery. As these checks will be infrequent, servicing costs can be regarded as negligible.

The model will evaluate ESS using upfront costs alone, as this will incorporate most of the systems lifetime cost, particularly for the new university campus. To understand the sensitivity of installation and maintenance costs, these will be incorporated into the model, to check the sensitivity of the model to these additional costs.

## Battery Lifetime Assessment - Understanding Battery Degradation

Sections \ref{forecasting-and-the-use-of-ess-in-load-shifting} and \ref{battery-sizing-and-financial-modelling}, in the literature review both highlighted the importance of battery health on the longterm  value of the battery. By operating the battery in a way that optimises its longevity and total savings, more value can be created from the asset. To correctly model how the Li-ion batteries degrade over time, the following section explains the parameters, their effect on battery health and how they should be regarded in the model. Below Figure \ref{batCapGen} shows the typical profile a Li-ion battery follows as it degrades over time.

\begin{figure}[H]
  \centering
  \includegraphics[trim = 0 0 0 0, clip, width=0.35\textwidth]{batCapGen.png}
  \caption{Plot of the General Relationship between battery capacity and cycle number \cite{spotnitz2003simulation} }
  \label{batCapGen}
\end{figure}

After the battery degrades below 80\% of it is original maximum capacity, the battery is regarded to be in its end of life phase. After this point, the battery tends to degrade more rapidly, making it much harder to predict how the battery will degrade beyond this point \cite{spotnitz2003simulation}. There is still potential for more energy to be delivered beyond this point, however as seen in figure \ref{batCapGen}, the battery tends to degrade a lot quicker. For the model to be representative, after the battery's health reaches 80\%, it should be seen as dead, reducing uncertainty.

### Battery Degradation Parameters
The following list of parameters, gives a brief overview of these effect battery degradation, highlighting how they are regarded in the model

- **Temperature**: By running the battery at a temperature too hot or too cold, the battery will degrade much quicker \cite{rong2006analytical}. The Tesla Powerpack incorporates an internal liquid cooling and heating system which allows for pinpoint temperature control. A dual coolant and refrigerant loop system ensure maximum performance in all climates with better efficiency than air cooling \cite{Powerpac95:online}. England experiences a relatively mild climate all year round, spending most of it is time between 3\degree and 22\degree \cite{WeatherA0:online}. These cooler temperatures favour the battery's performance, being more better for battery health than the Californian hot weather which the batteries were originally tested. The combination of milder temperatures and temperature regulation technology inside the battery means the model will not need to incorporate temperatures effect.
- **Charging**:
    - *Charging Level*: The cycle life of a battery can be increased by reducing the cut-off voltage of the battery. Battery voltage will be fixed at either high voltage three phase or at single phase 240V, where current drawn into the battery will vary.  By decreasing the voltage held inside the battery will extend the battery cycle life, resulting in the battery having a partial charge. This has a similar effect to working at a lower depth of discharge \cite{Choi2002130}. Figure \ref{capVol} shows the relationship to cell capacity and charge voltage, showing a dramatic decrease in cell performance for cells charged to higher levels. By charging the battery too its' full capacity the battery or continuing to charge the battery beyond its designed voltage, the battery capacity will degrade quicker. The battery becomes unstable if inadvertently charged above its specified voltage, where prolonged charging above the Li-ion designed voltage will plate metallic lithium on the anode. The cathode material becomes an oxidising agent, losing stability and producing carbon dioxide ($CO_2$). Within the cell, the pressure rises, which can cause the temperature inside the cell to increase, furthering the reduction in the batteries capacity. The cell has a lower thermal runaway temperature and will vent its temperature quicker than one that is partially charged. Consequently, Li-ion batteries are safer at a lower charge \cite{Charging53:online}. Due to these two issues, the battery should stop charging before reaching this threshold.
    \begin{figure}[H]
    \centering
    \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{capVol.jpeg}
    \caption{Plot of the Relationship Between Battery Cycle Life and Voltage of Charge \cite{Choi2002130} }
    \label{capVol}
    \end{figure}
    - *Charging Rate:* A reduction in battery capacity occurs at high discharge rates; due to the transformation of the active chemicals inside the cell being unable to keep pace with the current drawn. The results in an incomplete or unwanted chemical reducing the cells capacity \cite{BatteryL10:online}.  The model should maximise the charge time of the battery, to reduce this effect.

- **Usage**:
    - *Over Depletion*: Fully depleting the battery for extended periods can have detrimental effects on capacity. It is common for battery management systems (BMS), particularly in consumer electronics to power the device off at a threshold above zero; this negates some of the effects of depleted storage levels \cite{Prematur82:online}. The model should prevent the battery from being depleted below 10% to offset this effect.
    - *Speed of Depletion*: The rate in which the battery is discharged can have a strong effect on the battery life time. Figure \ref{disRate}  shows the effect on discharge rate on the rated capacity of a battery \cite{BatteryL10:online},\cite{Effectso69:online}. The effect of depletion rate is complex to model accurately, so a limitation should be placed on the the rate of battery depletion in the model, below the designed level.
     \begin{figure}[H]
       \centering
       \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{disRate.png}
       \caption{Plot of the Relationship Between Discharge Time and its' Effect on the Rated Capacity of a Battery \cite{Effectso69:online}}
       \label{disRate}
     \end{figure}

- **Depth of Discharge** (DoD): Depth of discharge is related to the number of active chemicals transformed with each charge/ discharge cycle. One full cycle is seen as when the battery is charged to its full current capacity (noting that the capacity will degrade over time, making each cycle length smaller). It has been cited that there is a logarithmic relationship between the depth of discharge and the cycle life of the battery \cite{BatteryL10:online}. Figure \ref{dodLog} below is for Lead-Acid batteries, but also holds true for Li-ion \cite{BatteryL10:online}. By restricting the possible DoD cycle life of the battery can be dramatically improved. It is common practice to select cells with slightly more capacity than required, or by topping up the battery before it fully discharges. The battery's average depth of discharge over its lifetime should be recorded and used as a metric for the validity of the selected batteries expected lifetime

    \begin{figure}[H]
      \centering
      \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{dodLog.png}
      \caption{Plot of Depth of Discharge vs Cycle Life \cite{BatteryL10:online}}
      \label{dodLog}
    \end{figure}

Figure \ref{SoCgraph} shows testing conducted on Li-ion cells combining the ideas found from battery charging and depth of discharge to increase the lifetime of the battery. Using this result, a charging range can be selected which optimises the payback period of the battery against the battery's lifetime.
  \begin{figure}[H]
    \centering
    \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{SoCgraph.png}
    \caption{Plot of the Measured  Relationship between battery State of Charge and it's Effect on the Cycle Number lifetime \cite{xu2016modeling}}
    \label{SoCgraph}
  \end{figure}
