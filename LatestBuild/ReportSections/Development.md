
# Development of Model Advantages and Barriers Assessment

This section discusses and defines how the model was created and the process used to generate results.

It is important to understand how a battery system can best be utilised to maximise it's effect. The following section will highlight the advantages and barriers of using a battery system. Understanding the advantages will highlight the best way to design a system architectures which leverages these points. It is this report objective to create strong arguments to how the system will overcome barriers to entry, laying out how all the assumptions in the model overcome these issues and address any qualitative issues in the following section

**Advantages**

* Reducing Electricity Bills:
    * Reducing the DUoS Charges
    * Reducing Triad Charges
    * Playing on the frequency response market (beyond project scope)
    * Reducing capacity charges
* Supply Levelling:
    * Leveraging maximum use of PV's and other renewable energy sources
    * Providing a fully predictable energy profile for new building.  Useful in negotiating price when new power capacity has to be installed ( very relevant to the new Bristol campus), saves paying for the new connection. \cite{wpMWMD}
* Emergency Power: Providing backup generation in the case of power cuts. Can support crucial systems alleviating risks associated with loss of power
* Sustainability:
    * Reducing peak load, reduces losses on the network. There is a green argument for running diesel generators in peak times. Batteries are a highly more sustainable.
    * Ensures self consumption of renewables

**Barriers**

* Costs of Purchase too high:
    * Installation Costs too high, too complex - \hl{difficulty of retrofitting?}
    * Unit Price of the battery is too high - (kWh)
    * Additional equipment cost, inverters
    * Maintenance cost
* Lifetime/ longevity of the battery too low, replacement costs/ dismantling cost make battery installation unfeasible
    * Unpredictability in cycle life of the battery may mean that lifetime is much lower than all good predictions
* Finance not feasible
    * Loan Interest > Savings
    * Negative NPV
* Frequent change of regulation may mean that costs shift to reduce battery savings, use for reducing DUoS is still favoured by energy companies. May change if lots of people take up using batteries in this manner.
* Barriers to entry
    * Laws/ regulations
    * Penalisation from energy companies
* Negative environmental effects: Uses of large scale quantities may be hold undesired environmental risks
* Risk of injury/ explosion. Large batteries that overload, hold a very high risk of explosion. Battery system monitoring is key to ensuring the battery operates with in it's limits
* Technology still maturing, Li-ion batteries have not been used in this manner before, for extended periods of time

## Battery Economics
The main objective of this project is to create a business case for using a battery system to reduce energy bills. Ultimately the model aims to produce the information required to justify whether investing in batteries is feasible and advise on the best battery to buy based on it's capacity and it's power rating. Due to the readily available commercial information of Tesla's Power-pack 2, this battery system was used to model financial feasibility and  optimal product.

There are 3 ways the model will evaluate the value of the battery system, these are: *pay-back period*, *total-savings* (over a designated period of time) and *net present value* (calculated for different discount rates). Each of these methods results will be compared to crediting the merits and pitfuls of each to understand which battery system is the optimum for the system.

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

After the battery degrades below 80\% of it's new maximum capacity, the battery is regarded to be at its' end of life phase. It is important to note that there potential for a large amount of capacity to be delivered beyond this point, however as seen in figure \ref{batCapGen}, the battery tends to degrade a lot quicker. There are also issues with power degrade

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

# Battery Model Definition

Understanding the key design parameters highlighted in section \ref{Development-of-Model-Advantages-and-Barriers-Assessment}. The model was created to capture as many of these drivers to maximise the models validity. Data was obtained for Senate house (a large University office/study space building). This data was manipulated to create a representative energy profile for the Senate and then the New Campus.

## Model Development Requirements

### Fixed vs Variable Optimisation Model

### Code Optimisation
### User Interface
### Ease of Development

## Creation of Senate House Billing Model

Data was received for Senate house, giving usage in kWh for the previous half hour period. A bill was also provided for a months energy use at the Victoria rooms (another Bristol University building used for lecturing, offices and teaching classes). A meeting with John Brenton \hl{add reference} clarified that billing profiles for both buildings were identical.

In order to gauge the size and power requirements needed for a building the size of Senate house, a minute by minute usage profile needed to be created and then cross checked against a representative bill to understand how the different charges are broken down and highlight charges to target the design of the battery system architecture too.

Using the half hourly usage data of senate house for a year, usage plots were created for different days in the year. It was clear that the was a major difference between energy demand during the weekend and during the week, shown in \ref{Development-c4}. Total energy consumption was 3 times greater over the weekdays than the weekend.  When creating at usage data, it was imperative to make sure that weekday's and weekend matched completely in order to give an accurate representation about the energy usage.  
 \begin{figure}[H]
 \centering
 \includegraphics[trim = 50 50 30 50, clip, width=0.5\textwidth]{Development-c4.eps}
 \caption{Plot of Mean Senate House Weekday and Weekend Usage}
 \label{Development-c4}
 \end{figure}
 This data was good at giving a rough estimation of the battery size needed to produce some impact on the Universities energy bills.

### Representative Bill Creation
\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{Development-38.png}
 \caption{Image of Energy Bill For Victoria Rooms}
 \label{Development-38}
 \end{figure}
Figure \ref{Development-38} shows a typical electricity bill for a University building. It is clear the red unit rates make up the largest part of the DUoS Charge and roughly 20\% of that months total recorded charges. Instead capacity charges made up only 4\% of the total bill. This realisation meant that the focus of the model would be to start by reducing the red rate charge through load shifting, and explore other charges if this proved to not be effective to offset investment costs. Figure \ref{Development-50} highlights the significance of the different unit costs.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.5\textwidth]{Development-50.eps}
 \caption{Difference in Unit Charge Rates}
 \label{Development-50}
 \end{figure}

Using this data a model was created taking into account DUoS charges and multiplying them by their respective rate. This charge makes up and large % of the total bill showing roughly how much the unit rate costs.

To achieve this, the date of the usage data was scanned to find which day the bill began, then assigning the next 6 days, to be either weekdays or weekends. This was important as there are different DUoS rate at different times of day between weekdays and weekends. Creating a counter that loops through each half hour period, logic can be applied to categorise each half hour period into their respective unit rate. Total units consumed in red, amber and green periods were found allowing for some simple calculations to find the effect of load shifting. By shifting the load in red units to green rate charges, a significant saving could be made. By measuring the amount of units consumed in red periods gave a good estimation for the size range of the battery that would be required.

## Representative Demand Profile
The second performance parameter of the battery is the maximum power it can supply, rated in kW. By applying to much load on a battery can ultimately cause it to fail, severely reducing the batteries cycle life. As there was no demand data available, a few assumption had to be made in order to generate an valid demand profile. First the half hourly usage data was split into a minute by minute representation, creating points at every minute by finding the gradient and constant between two points then splitting the distant into 30 equidistant points. This produced an identical graph to the fit, applied by Matlab. However as each point int he original graph represented usage for the previous 30 minutes, this was divided by 30 to give the usage per minute This can be validated by summing all the points and compare to the original graph.

This profile however assumes that all usage varies linearly between time periods. In reality this is not true. To generate a more realistic demand profile. The start, end and midpoint between two values were used as means in which a random number with a normal distribution was applied to give normally distributed values in intervals of 10 minutes, modelling how usage varies randomly minute by minute but holding the trend of the original data. Scaling by two, coverts usage from kWH into demand KW. This graph was then validated by integrating the area of the graph and comparing it against the summation of the original data. A standard deviation $\sigma$, was then selected which would fairly represent the change in usage. After trailing with a range of different scales of data, $\sigma$ was set to the mean between the average usage and max usage. This gave a fair, but conservative representation of how energy usage may look.

__*Assumptions:*__ Usage will have a peaky profile due to a large number of people in the buildings , switching numerous devices on and off frequently. For an office style building like Senate it is unlikely that there is any large equipment that could cause a major spike in demand.

The demand profile could then be plotted as both as histogram and as a cumulative distribution plot, identifying the typical demand of Senate house over the year, as well as the max demand the building experiences. Figures  \ref{Development-dd} and  \ref{Development-a8} show the demand profile of the building.
\begin{figure}[H]
 \centering
 \includegraphics[trim = 140 80 140 20, clip, width=0.95\textwidth]{Development-dd.eps}
 \caption{Plots of Usage and Demand Profile Generation and Histogram of Year Data}
 \label{Development-dd}
 \end{figure}

It can be observed from in the histogram in Figure \ref{Development-dd}, that the demand of the building typically falls between two points. One low peak representing morning and evening of 30KW and a second peak constituting the energy usage in the middle of the day, averaging around 80KW, but rarely ever exceeding 90KW.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.7\textwidth]{Development-a8.eps}
 \caption{Load Duration Plot of Year Usage Data}
 \label{Development-a8}
 \end{figure}

 The Load Duration Curve in Figure \ref{Development-a8} takes demand for each hour and plots this in descending order, this shows the annual demand that can be met for a battery at a given power rating [@combined-heat-power-buildings]. For Senate house, a battery rated to 40KW would cover, 5000 hours of the year roughly 55% of the years usage.

 Taking both graphs together, selecting a battery which covers the mean power demand, may act be a good trade off.

## Definition of New Campus Requirements

To fulfil the objectives of this project, an understanding of the design of the new campus needed to be assessed. As the building plans are still in their early stage, many assumptions about the likely size and use of the campus had to be understood in order to create a representative energy profile. Table \hl{*Insert Table of campus size/ rooms*} in the Appendix shows the predicted new campus size and use stating relevant assumptions.

The campus will constitute around 1500 students in halls of residence and have around 5000 staff and students on site during term time. Although there have been a range of facilities proposed that the University campus will house, it is most likely that the building will constitute mainly of tutorial rooms, a few lecture halls and offices. A meeting with John Brenton [@Jbrentmeet], made clear that creating infrastucure to support postgraduate business studies made the most economical sense so is most likely to make up most of the final plans.

The energy profile of Senate house will be mostly transferrable to the new campus, as it is unlikely the new campus will have any devices that will distort the load profile greatly. In addition, the campus is likely to have improved efficiency through utilising the latest technologies in its construction and services (ventilation, heating e.c.t.). Data on 125 rooms in halls of residence was also provided, it is likely that this will almost be identical to a new build, due to student usage making it difficult to manage energy demand further. Using the foot prints of both building and adding some additional laboratory data to simulate if these creates any spike in energy usage.

The scaling factors were:

* Senate House (7840sqm) - **7.9x**
* Hall data (2761sqm) - **7.6x**
* Lab data (1 Lab Use) - **4x**

Due to these data files falling under different years and running between different dates, the data needed to be adjusted in order to be correctly scaled. An algorithm was therefore created to match the date shown in figure \ref{Development-fc}.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.9\textwidth]{Development-fc.eps}
 \caption{Logic of Data Aligning Tool To Create New Campus Data}
 \label{Development-fc}
 \end{figure}

\hl{Make assumptions very clear}

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.6\textwidth]{Development-92.eps}
 \caption{Load Duration Profile for the New Campus}
 \label{Development-92}
 \end{figure}

## Definition of System Architectures / Strategies
