
# Results
This project aims to evaluate whether the value gained from purchasing batteries outweighs its large upfront costs and other challenges that battery technology faces. This section analyses the data gathered from zero-dimensional model and discusses the plausibility of using a battery and which battery is optimum based on a demand profile for both Senate House and the new University campus.

## Senate House Battery Optimisation

\hl{
  * Graphs of NPV, Total Savings and Payback Time
  * Discussion on installation costs
  * Optimum battery to choose
}

## New Campus Battery Optimisation

Using the input values defined in section \ref{definition-of-new-campus-requirements}, the model was used generated results for 113 different battery types. Due to the size demand profile of the battery requiring  up to \hl{xkW} in a during a red rate period, and requiring a capacity of up to \hl{ykWh}, meant that many different solutions were plausible for providing the most value. By simulating for a range of batteries over a period of time, key trends between capacity and max power could be seen. A 25 year period was selected to evaluate the battery performance over. It is expected that after this period of time, technology will have significantly changed, refurbishments on the buildings will be under consideration and unpredictability on the long term use of the batteries will be reduced. The following results will talk through the three key value measurements discussed in section \ref{battery-economics}.

### Total Savings and Payback Period

Due to the 25 year limit placed on the batteries, the largest batteries did not necessarily deliver the greatest savings due to their high purchase price not being converted into additional savings from the battery strategies having no further load to be shifted. Figure \ref{SRTS2} shows the parabolic shape with a local maximum between the battery size and the total savings for a 25 year period. For the new campus, a battery size of around 2000 kWh appeared to be the best choice battery to select. The max power needs to be very high, with a 1.2-1.3 MW power response, to access these maximum total savings.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.7\textwidth]{SRTS2.eps}
 \caption{Battery Size Vs Total Savings}
 \label{SRTS2}
\end{figure}

Looking at the payback period shown in Figure \ref{SRPB2}, a different story is told. The correct combination of max power and battery size is required to get a payback period between 6.3 and 8 years. Battery Sizes all remain below 2000kWh and provided that the battery size is paired with the correct maximum power, the shortest payback period can be accessed. After the 2000kWh mark, capacity rather than max power has the greatest effect in increasing the payback time.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.7\textwidth]{SRPB2.eps}
 \caption{Graph of Battery Size vs PayBack Time}
 \label{SRPB2}
\end{figure}

Figures \ref{SPA2} and \ref{SRTSPB5} look to use a graphical approach, of choosing the optimum battery system based on both its capacity and power rating.

\begin{figure}[H]
\centering
\includegraphics[trim = 0 0 0 0, clip, width=0.9\textwidth]{SPA2.eps}
\caption{Graph Showing Top 30 Batteries with Fitted Curves for both Payback Time and Total Savings}
\label{SPA2}
\end{figure}

A small region either-side of where the two plots cross in Figure \ref{SPA2}, can be approximated to be the optimum battery battery parameters. A designer aiming to select a battery based on these two parameters would look here to make a selection then find the nearest corresponding battery on the market that fits these values. It is apparent that the is a very steep drop off in total savings for batteries that fall outside these bounds. For both max power and total capacity selecting a battery with a lower rating than this bound will minimise the payback time, whilst selecting above this region will increase the payback time exponentially.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.9\textwidth]{SRTSPB5ed2.eps}
 \caption{Comparison Between Fit Curves for Payback Period and Total Savings}
 \label{SRTSPB5}
 \end{figure}

 Payback period is important measure when evaluating the investments risk. The longer the pay back period the more time there is for the battery to fail. For the Tesla Power-pack modelled, the batteries have a 10 year warranty. These reduces the risk significantly if the investment were to fail before this period. There are other risks associated with long payback periods are  energy pricing changing significantly reducing the value that the battery creates. Energy contracts typically last no longer than 4 years,\hl{find reference} in which billing structure could result in the batteries value dropping to zero - \hl{add sensitivity analysis}. Knowing that $\frac{2}{3}$ of the investment has been paid back as opposed to only a $\frac{1}{2}$ or less can have dramatic effects on the risk of the investment. These factors should be considered when choosing the design region of battery selection.

### NPV

An alternate way which tries to quantify risk, is by using net present value. Three rates of 3\%, 7\% and 12\% were selected to understand the value of the different batteries. Figure \ref{SRNPV1}, shows the NPV of the different batteries at these different rates.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.9\textwidth]{SRNPV1.eps}
 \caption{Net Present value at Different Discount Rates - Comparison}
 \label{SRNPV1}
\end{figure}

For discount rates of 3\% and 7\% the battery with the highest value was the same, having a power rating  of 1100 kW and a capacity of 2090kWh. When the discount rate is increased much above 7\%, it can be seen that the number of batteries that have a positive value is significantly reduced. The best value battery also becomes smaller rated to only 900kW and 1710kWh.

Selecting an appropriate discount rate is therefore key for deciding which is the best investment if using net present value. As the battery will degrade each year until it reaches its end of life value, it could be argued that the value of the asset decreases proportionally with this the remaining life of the battery. Looking at the the optimum battery at a discount rate of 7\% (see Table \ref{BestNPVTable} below), it can be seen that the specific battery ran for 4904 cycles. Based on this assumption the value of the battery would be 98% of it's original rate, this works out at a discount rate of roughly 3.92\%. As this will be different for each batteries the discount rate based on remaining value alone must approximate all batteries a value of 3\% therefore seems fair. Discount rate also takes into account inflation. For the UK this rate has varied between  -0.1\% and 3.5\% for the last 5 years \cite{UnitedKi95:online}.An approximate value of 2\% could be added to the discount rate to incorporate how money now is worth more than money later.

Finally discount rates can be used to incorporate interests on loans. As the battery would be a large one off payment that could be included in the mortgage on the new campus. This would keep the interest rate low, which can be approximated to 2\%. Using these three approximations gives a discount rate of around 7\% shown in figure \ref{SRNPV1}.

### Discussion on Optimum Battery
Below is a table showing the results of the battery which held the best NPV at a discount rate of 7\%:
\begin{table}[H]
\begin{tabular}{p{3.4cm}p{3cm}p{3cm}}
\textit{Parameter} & \textit{NPV Value} & \textit{Best Value}\\
\textbf{Battery Power Rating}:& 1100 kW\\
\textbf{Battery Capacity}:& 2090 kWh\\
\textbf{Total Saved}:& £1,953,706 & £1,966,697\\
\textbf{Payback Period}:& 7.0959 Years & 6.3562 Years\\
\textbf{Mean DoD}:& 31.5759\% \\
\textbf{Cycles}:& 4904\\
\textbf{Years}:& 25\\
\end{tabular}
\label{BestNPVTable}
\caption{Table Showing the Best Battery Results based on a Net Present Value of 7\%}
\end{table}

Comparing the results between Net Present Value and the Total Saving Vs Payback plots (see Figure \ref{SRTSPB5}),shows that the recommendation of NPV at 7\% is larger than the recommendation from the total saving payback plot. This suggests that at this discount rate, total savings is worth more than a reduced payback time.

### Battery Usage and Secondary Analysis

Due to the way the model was created some secondary analysis could be conducted on how the battery was run over it's lifetime. By measuring the batteries usage on weekdays, the mean depth of discharge could be measured. Based on the research conducted in section \ref{battery-lifetime-assessment---understanding-battery-degradation}, it is believed that the battery will wear much quicker when its average depth of discharge is higher, than when the depth of discharge is kept smaller. Figure \ref{DOD1} shows the relationship between depth of discharge and the battery type.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.8\textwidth]{DOD1.eps}
\caption{Depth of Discharge For Battery Lifetime}
 \label{DOD1}
 \end{figure}

 It can be observed from Figure \ref{DOD1} that the 


* Battery depth of discharge can vary greatly depending on the power rating and capacity, a trend can be seen as two separate
