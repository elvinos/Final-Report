
# Battery Storage Technology Key Advantages and Challenges

Table \ref{AdChalltab} identifies the key values and challenges of using Li-ion technology. Overcoming challenges with high severity by developing a comprehensive understanding of their effects is the focus of the model developed in this project. This is necessary to create an effective cost based analysis of using a Li-ion energy storage system. To create strong arguments to how the system will overcome these challenges, assumptions used overcome these issues are discussed in this section.

\begin{table}[H]
\vspace{-10pt}
\caption{Showing the Advantages and Challenges of Using Energy Storage}
\vspace{-5pt}
\centering
\includegraphics[trim = 0 0 0 0, clip, width=0.9\textwidth]{AdvantChallTab.pdf}
\label{AdChalltab}
\vspace{-15pt}
\end{table}

## Battery Economics
The primary objective of this project is to create a cost-based analysis business case for using a battery system giving a valid prediction of the value an ESS could generate. There are three ways the model will assess the value of the storage system; *net present value*, *pay-back period* and  *total-savings*. Each of these results will be compared, crediting their merits and pitfalls, to give a full understanding of the battery's value.

### Net Present Value
Net Present Value (NPV) describes the difference between the current value of cash inflows and outflows \cite{NetPrese35:online}. NPV is used in capital budgeting to analyse the profitability of an investment over the long-term.  Batteries are a significant upfront investment, seeing little financial value for many years. As a consequence, purchasing the battery through finance is likely, adding an interest rate to the cost of the battery. Battery degradation and inflation are also factors, increase the discount rate required to correctly value financial performance over time.

The Internal Return Rate (IRR) is a method for finding the maximum discount rate before that an asset generates a negative NPV. This is found by setting the net present value to 0 and calculating the return rate. Equation \ref{eq:IRR}, defines the secant numerical method used for calculating the IRR.
\begin{align}
r_{ n+1 }=r_{ n }-{ NPV }_{ n }\cdot \left( \frac { r_{ n }-r_{ n-1 } }{ { NPV }_{ n }-{ NPV }_{ n-1 } }  \right)
\label{eq:IRR}
\end{align}
Where $r_{ n }$ defines the $n^{th}$ approximation of the IRR \cite{xxxdvi44:online}.

Using Equation \ref{eq:IRR} the maximum discount rate can be found using batteries at the extremities of the results (lowest and highest performers). If the IRR is found to be too low, the battery strategies will need revising otherwise it can be concluded that it is not feasible to invest in an ESS \footcite[An IRR below 5\% is considered unfeasible, although unquantified benefits may be present][]{diorio2015economic}.  
Total savings is the measure of NPV when the discount rate is set to zero; providing a clear understanding of the cash flow which the system generates.

### Payback Period

\begin{wrapfigure}{r}{0.35\textwidth}
  \begin{center}
    \vspace{-45pt}
 \includegraphics[trim = 0 0 0 0, clip, width=0.34\textwidth]{BatPrice.eps}
  \end{center}
  \vspace{-5pt}
  \caption{Plot of Li-ion Battery Prices 2010-2016 \cite{mckBat}}
  \vspace{-30pt}
  \label{mckBatPrice}
\end{wrapfigure}

The Payback Period (PBP) is the time for project savings to equal or exceed the cost of the investment \cite{diorio2015economic}. This metric is used to measure risk. Minimising the payback period diminishes many high severity challenges of the battery, reducing the likelihood of energy billing change and the likelihood of the battery failing. The Tesla Power-pack 2 has 10 years warranty, reducing the risk of additional costs to replacement/repair the battery before it becomes profitable. As the battery will be viewed first as a financial investment by the University, having a short enough payback period will be essential to proving the battery systems viability.

## Li-ion Battery Costing

Over the last decade, Li-ion technology has advanced significantly, partly due to the rise in electric vehicles, slashing the price while improving efficiencies and energy densities. Figure \ref{mckBatPrice} shows the trend in prices for the last six years and the predictions for the next 15. Between 2010 to 2016, battery pack prices fell ~77% from $1,000/kWh to $227/kWh. Current projections put the price of Li-ion battery pack prices below $190/kWh by the end of the decade, corresponding with the construction of the new campus, an further 16\% reduction, consequently the feasibility of investing in the technology will continue to increase.

Data readily available on the Powerpacks's based on the battery's capacity (kWh) and maximum power (kW) \cite{Powerpac95:online}. This makes it possible to evaluate the optimum specification of battery for an energy profile. Unit costs start at £51,940 and scale infinitely. After purchasing the product, installation is the next largest cost to consider. The Powerpack comes almost as plug and play, including an inbuilt inverter simplifying the process extensively. The cost to install will be significantly greater when retrofitting to existing infrastructure as it is  assumed a suitable foundations are necessary due for the battery fully operational in a university environment. In the case of the new campus, it is assumed that there are little additional costs in installing the battery system due to installation requirements, placed on the site's design.

Maintenance/operations costs are another factor to consider. The Powerpack uses a health checking system, requiring little training to monitor the battery. It seems likely that the University can use a member of the Estates team monitor the battery infrequently. Section \ref{payback-period}, discussed the Powerpack ten-year warranty, eliminating any costs in the first 10 years. For these reasons maintenance/operations are assumed negligible.

By using today's battery prices, it is assumed the battery's cost will be under-estimated compared to when it will be installed in the new campus. This will reduce the uncertainty around the costing assumptions made.

## Battery Lifetime Assessment - Understanding Battery Degradation

\begin{wrapfigure}{r}{0.4\textwidth}
  \begin{center}
\includegraphics[trim = 0 0 0 0, clip, width=0.39\textwidth]{CapCycle.eps}
  \end{center}
    \vspace{-5pt}
\caption{Plot of the General Relationship Between Battery Capacity and Cycle Number Extracted From \cite{spotnitz2003simulation} }
  \vspace{-20pt}
  \label{batCapGen}
\end{wrapfigure}

Sections \ref{forecasting-and-the-use-of-ess-in-load-shifting} and \ref{battery-sizing-and-financial-modelling}, highlighted the importance of battery health in increasing the longterm value of an ESS. By operating the battery in a way that considers its longevity, further value can be generated. To correctly model how the Li-ion batteries degrade over time, the following section explains the different parameters which effect on battery health discussing how they should be regarded in the model.

Figure \ref{batCapGen} shows the typical capacity degradation profile of a Li-ion battery. After the battery degrades below 80\% (C) of it is original capacity, it is regarded to be in its end of life phase \cite{REIEC61465:online}. After this point, degradation becomes more rapid and unpredictable \cite{spotnitz2003simulation}. There is still potential for more energy to be delivered beyond this point \cite{Renaultt62:online}, however, for the model to remain representative, after the battery's health reaches 80\%, the battery should be regarded as dead.

The following list of parameters, gives a brief overview of these effect battery degradation, highlighting how they are regarded in the model

### Temperature

 By running the battery at a temperature too hot or too cold, increases a batteries rate of degradation significantly \cite{rong2006analytical}. The Tesla Powerpack incorporates an internal liquid cooling and heating system which allows for pinpoint temperature control. A dual coolant and refrigerant loop system minimises the effects of temperature degradation, climates providing better efficiency than traditional HVAC systems. \cite{Powerpac95:online}. Due to safety reason, it is recommend that the battery is installed outside, making the battery susceptible to climate. England experiences a mild climate all year round, spending most of it is time between 3\degree C and 22\degree C \cite{WeatherA0:online}. These cooler temperatures favour the battery's performance. For both these reasons, the model will assume temperatures effect on degradation is negligible.

### Depth of Discharge (DoD)

\begin{wrapfigure}{r}{0.5\textwidth}
\vspace{-40pt}
  \begin{center}
\includegraphics[trim = 0 0 0 0, clip, width=0.49\textwidth]{dodplot22.eps}
  \end{center}
    \vspace{-5pt}
  \caption{Plot of Depth of Discharge vs Rated Capacity, Interpolated From \cite{BatteryL10:online}}
  \label{dodLog}
  \vspace{-10pt}
\end{wrapfigure}

Depth of discharge is related to the number of active chemicals transformed with each charge/ discharge cycle \footnote{See Figure \ref{BatteryImage}, for a detailed description of battery cycling}. Figure \ref{dodLog} shows experimental results of the effect of DOD on Lead-Acid batteries capacity, holds true for Li-ion \cite{BatteryL10:online}. At the rated cycle life of 5000, is was assumed a 70% DOD was used to test the battery lifespan \cite{Teslawil27:online}. This value was scaled accordingly. By restricting the possible DoD cycle life of the battery can be dramatically improved. It is common practice to select cells with more capacity than required. The battery's average depth of discharge over its lifetime should be recorded and used as a metric for the validity of the selected batteries expected lifetime.

### Usage
\begin{wrapfigure}{r}{0.5\textwidth}
\vspace{-40pt}
  \begin{center}
\includegraphics[trim = 0 0 10 0, clip, width=0.49\textwidth]{dischargetime.pdf}
\vspace{-5pt}
  \caption{Plot of the Relationship Between Discharge Time and Rated Capacity, Interpolated from \cite{Effectso69:online}}
    \end{center}
  \label{disRate}
  \vspace{-20pt}
\end{wrapfigure}

_Over Depletion_: Fully depleting a battery for extended periods can have detrimental effects on capacity. It is common for battery management systems (BMS), particularly in consumer electronics to power devices off above zero; negating some of the effects of depleted storage levels \cite{Prematur82:online}. The model should prevent the battery from being depleted below 10% to offset this effect.

_Discharge Time_: When discharging batteries quickly, the effective capacity of the cell can be reduced \cite{BatteryP62:online}. The Peukert Equation is a method used to characterise cell behaviour with regards to capacity offset, when depleting the battery at high discharge rates. It is unclear what the Powerpack's Peurket number is, but it can be assumed to be between 1-1.02, where 1 is perceived as the battery performing well. \cite{omar2012rechargeable}, \cite{omar2013peukert} \footnote{Li-ion's low Peurket number is another strong supporting factor why using Li-ion is well suited reducing peak demand where there may be instantaneous high levels in demand}. The low Peurket number means discharge rate up to the rated power, has little effect on the battery's perceived capacity.
Rate of discharge also effect the batteries lifetime\cite{BatteryL10:online},\cite{Effectso69:online}. Using the experimental trend shown in Figure \ref{disRate}, an equation for the effect of speed of depletion can be used to validate the effect of average discharge time. This parameter should be recorded by the model.

### Charging

\begin{wrapfigure}{r}{0.4\textwidth}
\vspace{-55pt}
  \begin{center}
\includegraphics[trim = 0 0 0 0, clip, width=0.4\textwidth]{SoCgraph.png}
  \end{center}
  \vspace{-5pt}
\caption{Relationship Between State of Charge and Cycle Life \cite{xu2016modeling}}
  \label{SoCgraph}
  \vspace{-20pt}
\end{wrapfigure}

_Charging Level_: The cycle life of a battery can be increased by reducing the cut-off voltage of the battery. Battery voltage will be fixed at either high voltage three phase or at single phase 240V, where current drawn into the battery will vary. Decreasing the battery's voltage will extend its life (partial charging) \cite{Choi2002130} \footnote{ See Figure \ref{capVol} in the Appendix, showing the relationship of cell capacity and charge voltage, where  a dramatic decrease in cell performance for cells charged to higher levels is visible}. By charging the battery too its' full capacity, or overcharging, the battery capacity will degrade quicker, becoming unstable. Cell chemistry causes pressure to rise, increasing temperature inside the cell, further reducing in the battery's capacity. The cell also has a lower thermal runaway temperature and will vent its temperature quicker than one that is partially charged. Consequently, Li-ion batteries are safer at a lower charge \cite{Charging53:online}. Due to these two issues, the battery should stop charging before reaching this threshold.

_Charging Rate_: Similar to discharge time, a reduction in battery capacity occurs at high discharge rates; due to the transformation of the active chemicals inside the cell being unable to keep pace with the current drawn, reducing cell capacity \cite{BatteryL10:online}. The model should maximise the charge time of the battery, to reduce this effect.

Figure \ref{SoCgraph} shows testing conducted on Li-ion cells combining the ideas found from battery charging and depth of discharge to increase the lifetime of the battery. Using this result, a charging range can be selected which optimises the payback period of the battery against the battery's lifetime.
