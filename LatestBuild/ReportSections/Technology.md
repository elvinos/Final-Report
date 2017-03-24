
# Battery Storage Technology Key Advantages and Challenges

This section discusses and defines how the model was created and the process used to generate results.

It is important to understand how a battery system can best be utilised to maximise it's effect. The following section will highlight the advantages and barriers of using a battery system. Understanding the advantages will highlight the best way to design a system architectures which leverages these points. It is this report objective to create strong arguments to how the system will overcome barriers to entry, laying out how all the assumptions in the model overcome these issues and address any qualitative issues in the following section


\begin{table}[H]
\centering
\includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{AdChallTab2.pdf}
\caption{Showing the Advantages and Challenges of Using Energy Storage}
\label{AdChalltab}
\end{table}


## Battery Economics
The main objective of this project is to create a business case for using a battery system to reduce energy bills. Ultimately the model aims to produce the information required to justify whether investing in batteries is feasible and advise on the best battery to buy based on it's capacity and it's power rating. Due to the readily available commercial information of Tesla's Power-pack 2, this battery system was used to model financial feasibility and  optimal product.

There are 3 ways the model will evaluate the value of the battery system, these are: *pay-back period*, *total-savings* (over a designated period of time) and *net present value* (calculated for different discount rates). Each of these methods results will be compared to crediting the merits and pitfalls of each to understand which battery system is the optimum for the system.

**NPV Calculation:**
As the battery is a large up front cost, it is likely that the battery will be purchased on financing this means that interest on the loan has to be paid each year reducing the battery value. Additionally the battery will degrade in performance over time, this is key to understanding the value of the product over its life time. Using an Initial return rate \hl{Add return rate calc here} the maximum discount rate can be found for a few batteries (using the extremes). This can then be used to set different discount rates, where 0 is used to illustrate the payback of the battery. Even with the battery degrading, it can be predicted that the battery will continue to degrade until failure.
\hl{The net present value (NPV) is a way to examine costs and revenues while accounting for the time value of money. If the NPV of a system is positive, then the investment is predicted to provide a return on investment greater than the initial and ongoing cash expenditures associated with ownership of the system. A negative NPV indicates the returns are worth less than the cash outflows and the investment does not show a financial benefit, although unquantified benefits may be present.} \cite{diorio2015economic}
Total-savings is the measure of net present value when the discount rate is 0.

**Payback Period:**
\hl{The payback period (PBP) is the time in years it takes for project savings to equal or exceed the initial cost of the investment. This metric is included because of its ability to quickly communicate tangible value of a project. A system which yields a very short payback period is typically a profitable one because subsequent years of the project result in pure revenue for the system owner. A system which cannot be paid back over the lifetime of the system is a poor investment because money is still owed when the system is retired and no longer able to generate revenue. The payback period is reported as the first time where the project savings exceeds the debt, but care must be taken to also consider additional cash expenditures in later years.} \cite{diorio2015economic} The this model looks at the lifetime of investing in one battery system over a period of time so additional cash expenditure is ignored in this model.

## Battery Costing
\hl{explanation of the Power-pack 2 costs, including warranty, maintenance, installation and any other additional costs. Discussion of the falling costs of lithium battery prices, refer to Diagram}

\begin{figure}[H]
  \centering
  \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{mckBatPrice.png}
  \caption{Plot of Battery Prices Reduction for 2010-2016 and Predictions for Future battery Prices \cite{mckBat}}
  \label{mckBatPrice}
\end{figure}

\hl{Discussion of Li-ion Battery Falling costs, why now or the 5 year time period of the campus is a good time to buy, installation costs, probably large when retrofitting to an existing building, although the technology comes as almost plug and play, assume will need to be connected to where the mains supply enters the building in order to work in tandem with mains supply Other technology required such as inverters e.c.t.}

## Battery Lifetime Assessment - Understanding Battery Degradation

The below figure shows the typical profile a Li-ion battery follows as it degrades over time:

\begin{figure}[H]
  \centering
  \includegraphics[trim = 0 0 0 0, clip, width=0.35\textwidth]{batCapGen.png}
  \caption{Plot of the General Relationship between battery capacity and cycle number \cite{spotnitz2003simulation} }
  \label{batCapGen}
\end{figure}

After the battery degrades below 80\% of it's new maximum capacity, the battery is regarded to be at its' end of life phase. It is important to note that there potential for a large amount of capacity to be delivered beyond this point, however as seen in figure \ref{batCapGen}, the battery tends to degrade a lot quicker. There are also issues with power degradation

The literature review revealed these factors to have the greatest effect on the rate in which the battery decays:

- Temperature: By running the battery at a temperature too hot or two cold, the battery will degrade much quicker \hl{Include numerical prediction here with reference} \cite{rong2006analytical}
- Charging:
    - Charging Level: The cycle life of a battery can be increased by reducing the cut off voltage of the battery. \hl{Battery voltage will be fixed at either high voltage three phase or at single phase 240V, instead current drawn by the battery will very.} Decreasing the current drawn therefore will extend the battery cycle life, give the battery a partial charge instead of fully charing it. This has a similar effect to working at a lower DoD.
    \cite{Choi2002130}
    \begin{figure}[H]
    \centering
    \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{capVol.jpeg}
    \caption{Plot of the Relationship Between Battery Cycle Life and Voltage of Charge \cite{Choi2002130} }
    \label{capVol}
    \end{figure}
    - Overcharging: By charging the battery too its' full capacity the battery or continuing to charge the battery beyond its designed voltage, the battery capacity can quickly degrade. \hl{The battery becomes unstable if inadvertently charged to a higher than specified voltage. Prolonged charging above 4.30V on a Li-ion designed for 4.20V/cell will plate metallic lithium on the anode. The cathode material becomes an oxidising agent, loses stability and produces carbon dioxide (CO2). The cell pressure rises and if the charge is allowed to continue, these can cause the temperature inside the cell to increase, furthering the reduction in the batteries capacity. A fully charged battery has a lower thermal runaway temperature and will vent sooner than one that is partially charged. All lithium-based batteries are safer at a lower charge.} \cite{Charging53:online} Due to these two issues the battery should stop charging once it reaches a threshold below its maximum value.
    - Charging Rate: \hl{The capacity reduction at high discharge rates occurs because the transformation of the active chemicals cannot keep pace with the current drawn. The result is incomplete or unwanted chemical reactions and an associated reduction in capacity} \cite{BatteryL10:online}

- Useage
    - Over Depletion: Leaving the battery fully empty for too long can have detrimental effects on capacity. It is common for battery management systems (BMS), particularly in consumer electronics to power the device off at a threshold above 0, to negate some of effects of low energy storage \cite{Prematur82:online}. \hl{Add further evidence here}
    - Speed of Depletion: The rate in which the battery is discharge can have a strong effect on the battery life time. The images below shows the effect on discharge rate on the rated capacity of a battery.
     \cite{BatteryL10:online},\cite{Effectso69:online}
     \begin{figure}[H]
       \centering
       \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{disRate.png}
       \caption{Plot of the Relationship Between Discharge Time and its' Effect on the Rated Capacity of a Battery \cite{Effectso69:online}}
       \label{disRate}
     \end{figure}

- Depth of Discharge (DoD): Depth of discharge is related to the number of **active** chemicals transformed with each charge/ discharge cycle. One full cycle is seen as when the battery is charged to its full current capacity (noting that the capacity will degrade over time, making each cycle length smaller). It has been cited that there is a logarithmic relationship between depth of discharge and the cycle life of the battery \cite{BatteryL10:online}.\hl{Note the graph above is for Lead-Acid batteries, but also holds true for Li-ion by restricting the possible DOD in the application, the designer can dramatically improve the cycle life of the product. Similarly the user can get a much longer life out of the battery by using cells with a capacity slightly more than required or by topping the battery up before it becomes completely discharged.} \cite{BatteryL10:online}

    \begin{figure}[H]
      \centering
      \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{dodLog.png}
      \caption{Plot of Depth of Discharge vs Cycle Life \cite{BatteryL10:online}}
      \label{dodLog}
    \end{figure}
  \begin{figure}[H]
    \centering
    \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{SoCgraph.png}
    \caption{Plot of the Measured  Relationship between battery State of Charge and it's Effect on the Cycle Number lifetime \cite{xu2016modeling}}
    \label{SoCgraph}
  \end{figure}

\newpage
