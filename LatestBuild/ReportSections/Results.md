
# Results
The objective of this report was to evaluate whether there is the strong business case for investing in energy storage technology for the New University Campus. This section analyses the data gathered from the zero-dimensional model, discussing the value which optimum batteries specifications could bring to the new Temple Quarter campus. Figures \ref{histredload} and \ref{redloadperc}, describes the energy profile for the new campus's usage during Red rate periods.

\begin{figure}[H]
\centering
\begin{minipage}{.495\textwidth}
  \centering
 \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{histredload.eps}
 \vspace{-20pt}
 \caption{Histogram Showing Red Periods Total Daily Usage Frequency}
 \label{histredload}
\end{minipage}
\hfill
\begin{minipage}{.495\textwidth}
  \centering
 \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{redloadperc.eps}
 \vspace{-20pt}
   \caption{Time Spent at Power Demand Level}
  \label{redloadperc}
\end{minipage}
\vspace{-30pt}
\end{figure}

These energy profile plots, described the range of battery specifications which should be simulated. Figure \ref{histredload}, that how a battery with a usable capacity greater than ~1800kWh will have excess capacity to demand. By taking into account end of life degradation, battery's up to and end of life capacity of 2000kWh were modelled. Figure \ref{redloadperc}, describes the percentage of time the battery would spend at max load. A battery rated at 920kW would be only run at max load 10\% of the time. As discharge rate effects capacity, battery's rated up to 1300kW were simulated. Based on this analysis 65 different Powerpack 2 battery specifications were identified as plausible solutions.

A 25 year runtime period was used to evaluate the battery performance over \footcite[See Page 27 of][]{heatcibse};  chosen on the assumption that most technology in the building will be replaced by this point, as the building begins to receive some refurbishment. Li-ion battery technology will have also significantly advanced, or at least drop significantly in price \footnote{See Figure \ref{mckBatPrice} for a prediction in battery prices}. Using a set period will also reduce uncertainty in battery health and prevent favouritism for larger batteries. An investor is unlikely to look beyond 25 years, so savings made after these periods will not be considered. The following results will talk through the three key value measurements discussed in section \ref{battery-economics}.

## Total Savings and Payback Period

 Figure \ref{SRTS2} shows the parabolic shape with a local maximum between the battery size and the total savings. For the new campus, a battery size of around ~2.2MWh generated the maximum total savings over the simulation run time. In contrast, Figure \ref{SRPB2}, highlights that a much larger range of batteries fell close shortest payback time of 6.3years, where power and capacity increased proportionally.

\begin{figure}[H]
\centering
\begin{minipage}{.495\textwidth}
  \centering
   \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{batsts.eps}
 \caption{Battery Size Vs Total Savings}
 \label{SRTS2}
\end{minipage}
\hfill
\begin{minipage}{.495\textwidth}
  \centering
\includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{batspb.eps}
   \caption{Graph of Battery Size vs PayBack Time}
  \label{SRPB2}
\end{minipage}
\vspace{-10pt}
\end{figure}

Figures \ref{SRTS2} and \ref{SRPB2}, begin to give a good insight into the financial performance of the battery, however, presented in this form, it difficult for a designer to choose the optimum battery. To make the results more useful, an algorithm was made, which generated best-fit plots over the maximum battery specifications for the different total saving and payback time plots. Figures \ref{SPA2} shows how these curves plotted over the maximum values.

\begin{figure}[H]
\centering
\includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{mxfit.eps}
\caption{Graph Showing Top 40 Batteries with Fitted Curves for both Payback Time and Total Savings}
\label{SPA2}
\vspace{-20pt}
\end{figure}

By superimposing these max-fit curves, a graphical tool was created, allowing a designer to visualise the tradeoff between total savings and payback time, shown in Figure \ref{SRTSPB5}. A small region around the cross over point of the two plots shows the specifications of the optimum batteries. By creating a set of rules (e.g. the battery must have a payback period less than seven years), all the solutions become immediately apparent. A small shortlist of the batteries can be made, referring back to the original list of Powerpack specifications.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{mxfitplt.eps}
 \caption{Comparison Between Fit Curves for Payback Period and Total Savings}
 \label{SRTSPB5}
 \vspace{-20pt}
 \end{figure}

Analysing Figure \ref{SRTSPB5}, the regions where the best trade-off between payback time and total savings (around where the two plots intersect) has been highlighted. The results show that a battery around 1762kWh and 744.4kW, produces a good compromise. Increasing capacity beyond increases total saving at the result of quickly decreasing the pay back period. Alternatively, when looking at max power, payback time is increases slightly for as power decreases. Up top 950kW, total savings dramatically increase, with very little decrease in payback time. The green region highlights the region after the intersection point, showing a battery larger than 745kW but less that 950kW, is optimum.

Measuring the payback period is necessary when evaluating the risk of investing in a battery. The longer the payback time, the greater the risk in either the battery failing or regulation changing diminishing the batteries value \footnote{See Table \ref{AdChalltab} for a more detailed description of the challenges that an ESS system faces}. The Powerpack 2 specifications modelled, have a 10 year warranty; this eliminates any risk if the battery were to fail before this period. Changes in energy billing are therefore the biggest risk the technology faces. Energy contracts typically last no longer than four years \cite{wpMWMD},  after which a change in pricing scheme could reduce the battery's value to zero. Knowing that $\frac{2}{3}$ of the investment has a very low risk of uncertainty rather than $\frac{1}{2}$, makes the investment much more attractive. These factors should be considered when choosing the design region of battery selection. For a structural investment, a payback period between 5 and 7 years is deemed good. The optimum battery payback time is 6.3 years falling within this range. From this analysis investing in Li-ion appear feasible.

## NPV

Net present value was the second method used to assess the battery systems value. As long payback periods are inherently risky, NPV uses discount rates to devalue cash that is made further in the future. As discussed in section \ref{net-present-value}, the Internal Return Rate was found. This calculation found for the range of battery assessed that the average IRR was 11\%,falling between 2 and 15\%. Three discount rates of 3\%, 7\% and 12\% were selected to understand the value of the different batteries based of the IRR calculation. Figure \ref{SRNPV1} shows the net present values of the various simulated batteries at these different rates.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{npv1.eps}
 \caption{Net Present value at Different Discount Rates - Comparison}
 \label{SRNPV1}
 \vspace{-20pt}
\end{figure}

Using the different NPV rates, presented conflicting optimum batteries. Increasing discount rate favoured smaller. Looking across the result of it was decided that a batteries a 7\% discount rate the following assumptions:

* __Battery Health__: As the battery will degrade each year until it reaches its end of life value, an assumption can be made that the value of the asset decreases proportionally to the battery's health. Looking at the optimum battery at a discount rate of 7\% (see Table \ref{BestNPVTable} below), it can be seen that the specific battery ran for 4904 cycles. Based on this assumption the value of the battery would be 98% of its original value, equating to a discount rate of  ~3.92\% over the 25 year period. As each battery degrades differently, the discount rate due to battery healthy can be approximated to 4\%.
* __Inflation__: Inflation is another factor of the discount rate. For the UK, this rate has varied between  -0.1\% and 3.5\% for the last five years \cite{UnitedKi95:online}. It is expected that the price of energy bills will increase with inflation, therefore this interest was neglected.
* __Interest Rates__:  Discount rates can be used to incorporate interests on loans. As the battery would be purchased at the same time as the rest of the new campus it is assumed that the battery will be bought under the new campus's mortgage;  keeping the interest rate low, approximated to 3\%.

Using these approximations gives a discount rate of around 7\% shown in figure \ref{SRNPV1}.

## Battery Health Analysis

In order to reduce computational time and simplify the model, assumptions were made to confine the battery to never work outside of normal working parameters. Section \ref{battery-lifetime-assessment---understanding-battery-degradation}, discussed how discharge time and depth of discharge effect the battery lifetime. Based of experimental data, equations for how these factors effect were found. The way the model was created to measure average depth of discharge and discharge time, allowing the effect of these parameters to be analysed after completing the simulation. Understanding the effect of these parameters increases the validity of results. Figure \ref{DOD2mbs} and \ref{Dist1} show the trend between depth of discharge and discharge for the different batteries.

\begin{figure}[H]
\centering
\begin{minipage}{.495\textwidth}
  \centering
  \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{DOD1bs.pdf}
 \caption{Depth of Discharge For Battery Lifetime}
 \label{DOD2mbs}
\end{minipage}
\hfill
\begin{minipage}{.495\textwidth}
  \centering
   \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{Dist1bs.pdf}
   \caption{Expected Capacity Offset Due to Discharge Rate and Depth of Discharge}
  \label{Dist1}
\end{minipage}
\vspace{-10pt}
\end{figure}

The patterns observed in Figures \ref{DOD2mbs} and \ref{Dist1} occur due to the difference between maximum power and maximum capacity. Comparing this result to Figure \ref{SRTS2}, it can be seen that the batteries achieving the maximum total savings have DOD greater than 70%, but are not always fully discharged.  Batteries appear to fall into two categories; one of high mean depth of discharge between 70-80\% and one with a mean depth of discharge around 50\%. This is a result of the relationship between capacity and max power, limiting the possible depth of discharge that the battery could reach in the two hour red rate period. With regards to the discharge rate in Figure \ref{Dist1}, As capacity increases, discharge rate tends also increase, almost doubling against the high power lower capacity batteries.

Using the polynomial equations outlined in Figures \ref{disRate}, \ref{SoCgraph} and  an additional performance parameter describing a more realistic end cycle life size was found based on these two measurements. The results are shown in Figure \ref{capnew}.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{capnew2.eps}
 \caption{Showing the Expected Effect of Depth of Discharge and Discharge Time on Predicted Cycle Life}
 \label{capnew}
 \vspace{-20pt}
 \end{figure}

  It is clear from Figure \ref{capnew} that taking into account DOD and discharge time , the lifetime of the battery can either be reduced or increased significantly. As not all batteries will fully degrade by the end of the 25 year lifetime, slightly reduced capacity may not be a problem as the battery should still be functional beyond the end of life value. From research, it appears depth of discharge can have a more dramatic effect on the batteries lifetime. To make experimental effects of DOD comparable for the Powerpack, a conservative assumption of the battery being rated at 70\% DOD was used. \cite{Teslawil27:online}, however notes that it is possible higher DOD were used to achieve the 5000 cycle life. This would decrease the effect of DOD significantly, meaning many more batteries would increase in cycle life rather than decrease. For both these reasons it is unclear whether error in predicting battery will have a significant effect on the battery's value.

## Discussion on Optimum Battery
Table \ref{Bestbat}, show the optimum battery configurations based on the metrics discussed perviously.
\begin{table}[H]
\centering
\caption{Table Showing the Best Battery Results Comparing the different Economic Measurements}
\includegraphics[trim = 0 0 0 0, clip, width=0.8\textwidth]{topbatstab.pdf}
\label{Bestbat}
\vspace{-20pt}
\end{table}

The following observations can be made on the results:

* The difference in NPV between the best NPV, total savings and max plot values is around £40,000, this is relatively marginal against the total cost of the investment
* A difference of only a years payback time can be observed by all the best performing batteries.
* All the batteries are run towards their maximum working threshold with high DOD and mean discharge times
* The maximum plot specification battery gives the highest Return on Investment (ROI), this measure helps understand how much money is made, compared to how much was invested.
* Annualised savings of all the battery excluding lowest payback ranges by £6,000 only. Between max plot and total savings, an increase in 35\% in upfront cost creates only 9\% more yield a year.
* Selecting a battery based on the lowest payback period has a significantly lower NPV and the likelihood of it failing before it reaches 5000 cycles is likely
* By selecting the battery with the largest total savings has the highest probability of not wearing out before it reaches the end of life


## Sensitivity on Key Assumptions

* Graph of effect of peak demand rise by 25%
* Graph on the effect of change in pricing structure - decrease DUOS - increase Capacity ?
