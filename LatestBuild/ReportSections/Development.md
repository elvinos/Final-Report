
# Battery Model Definition

Through understanding the key design parameters for reducing the impact of challenges set in section \ref{battery-storage-technology-key-advantages-and-challenges}, a viable model of the battery system was defined. Data was obtained for Senate House (a 7-storey University office/study building). This was used to create a characteristic demand and usage profile for Senate; then manipulated to create a representative energy profile for the New Campus. This section will define how the model was created, discussing the methodology and any assumptions made. Figure \ref{SystemLogic1} describes an overview of the primary inputs, processes and outputs of the model.
\begin{figure}[H]
 \centering
   \vspace{-7pt}
 \includegraphics[trim = 0 0 0 0, clip, width=0.9\textwidth]{SystemLogic1.eps}
  \vspace{-10pt}
 \caption{Diagram Showing Key Inputs, Processes and Outputs of Model}
 \label{SystemLogic1}
 \vspace{-30pt}
 \end{figure}

## Model Development Requirements

A distinct set of modelling requirements were essential to ensure that a functional model was created which corresponded to the project's objectives. By building a flexible, simple model, any unnecessary complexity was removed; sparing both time and computational expense. A robust set of requirements also provided a basis for assessing the completeness of work. The following section defines these requirements.

### Zero-Dimensional vs. Three-Dimensional Modelling

The zero-dimensional modelling approach is a technique used in the development cycle of a product, typically in the early stages. Zero-dimensional models are used to understand general performance of a system [@ZeroDMod80:online]. Instead three-dimensional models are implemented when detailed analysis is needed. The system dynamics of a zero-dimensional model are a function of the time while a three-dimensional model is a function of the time and space. For this reason, a zero-dimensional models are simpler and faster at generating solutions; enabling a much large number of simulations to be run.  As multiple battery systems and strategies are being evaluated, zero-dimensional modelling method was used.

### Code Optimisation and Ease of Development

A time-based iterative modelling method, based on a zero-dimensional approach, was selected to model a large variety of different battery specifications. Running the simulation through time requires performing  calculations on large matrices. The model should be optimised for performance to minimise running times; helping improve the model performance and reduce data collection time, allowing for a greater amount of different battery specifications to be modelled \footnote{See section \ref{input-parameters-and-multi-battery-simulation} the methods used to create optimised code}. It is essential that the model remains structured to allow for expansion as the project progresses. A function based approach must be taken throughout the development process to allow the model reach to its expected size and complexity. Without functions, structure will be poor increasing the difficulty in further develop and debugging.

### User Interface

There is a strong likelihood of using this model for next year's group design project. The modelling functions outlined in the project's outputs, should operate independently from each other, working with a broad range of data. Being able to manipulate the model easily will mean others will be able to use the tools developed, making the model much more useful. The model, consequently, must allow for a range of inputs, which should be easily configurable. Design the model in this way, will also simplify data collection reduce the risk of introducing a systemic error, associated with the user entering incorrect inputs or false logic. Dates and times of the energy usage data inputted in the model will have a large effect on the results. It is important therefore that the model can read data files and use their dates, to create accurate runtime usage data. The data outputted by the model must be clear and easy to interpreted by any user, with minimal post-processing; this will improve the model's ability to be a design tool.

## Creation of Senate House Billing Model

In order to validate the results of the model before testing on the new campus, the model was developed for use Senate House.

\begin{wrapfigure}{r}{0.5\textwidth}
  \begin{center}
    \vspace{-5pt}
 \includegraphics[trim = 0 0 110 0, clip, width=0.49\textwidth]{wkendwkday.eps}
  \end{center}
  \vspace{-10pt}
  \caption{Plot of Mean Senate House Weekday and Weekend Usage, and Difference in Unit Charge Rates}
  \vspace{-20pt}
  \label{wkendwkday}
\end{wrapfigure}

Data for Senate House, was provided; describing half-hourly usage between 10/08/2014 and 10/08/2015. A bill was also provided for a months energy usage at the Victoria rooms \footnote{A Bristol University building used for lecturing, offices and teaching classes, see Figure \{Development-38} for the Bill provided}. A meeting with John Brenton \cite{Jbrentmeet} clarified that billing profiles for both buildings were identical. In order to gauge the size and power requirements of a battery system for Senate House, a minute by minute energy profile was required. Corresponding this energy profile with a bill identified how energy consumption correlated with the cost, allowing quick sensitivity calculations to select strategies likely to would have the greatest impact.

Using this data, plots were used to visualise key trends in energy consumption, such as the variation of used based on time of day and period in the year. It was clear that the was a major difference between energy demand during the weekend and during the week, shown in \ref{wkendwkday}, where total energy consumption was found to be three times greater over weekdays than the weekend. It was vital all these trends were replicated when the usage file was manipulated.

### Representative Bill Creation

Section \ref{university-energy-charges} described the components of the energy bill. It's clear that Red rate charges are a significant charge which an ESS can target, incorporating ~20\% of the bill. To highlight the significance of the Red rate charge, Figure \ref{wkendwkday} shows the difference in DUoS rates. A preliminary model was designed to target Red rate charges only through load shifting. Using Senate's half-hourly data, each DUoS rate charges and unit charges was calculated. The energy profile was scanned to find which day the bill began, assigning each day as a weekends or weekday, crucial as Red rate charges aren't applicable on weekends. By creating a counter that looped through each half hour period, logic was be applied to categorise each half hour period into their respective unit rate. Total units consumed in Red, Amber and Green periods were found, where simple calculations revealed the the effect of load shifting could have. This crude model captured 79\% of the monthly energy bill charges.

## Representative Demand Profile

To simulate how a battery performs, power and capacity must be considered. Applying too much load on a battery can severely reduce the batteries cycle life, discussed in section \ref{battery-lifetime-assessment---understanding-battery-degradation}. Due to the lack of available demand data for the University, assumptions were made to generate a valid demand profile based on the original half-hourly usage profile.

First, the usage data was broken down into a minute by minute representation. Through using linear interpolation, an identical looking graph of the original data was created, containing 1440 points representing each minute, see Figure \ref{sendem}. This graph was then downscaled to give usage per minute (validated by summing all the points and comparing to the original data).

This crude profile, however, assumed that all usage varies linearly between time periods. In reality, this is not true. A more realistic demand profile was then created by finding the midpoint between values and assigning a random normally distributed number, in intervals of 10 minutes. Choosing an interval too small would deviate the total usage away from the original, while too big would subdue the shape of the graph. This method modelled how usage varied randomly minute by minute, similar to items being turned on and off frequently in a building, but held the original data's consumption trend.  A standard deviation $\sigma$ was then selected which would fairly represent the change in usage over time. For $\sigma$ to be valid for a variety of different magnitudes in data, the value was trailed against a range of different data sizes. It was found that by assigning $\sigma$ as a function of average usage and max usage, gave a fair, but conservative representation of how energy usage may look. Scaling by a factor of 2, converted usage from kWh to demand kW; producing a graph showing the peaky nature of energy demand for Senate House. By integrating the area under the demand curve, this graph was validated against the original data.

**Assumptions**: Usage will have a peaky profile due to a large number of people in the buildings, switching numerous devices on and off frequently. For an office style building like Senate, it is unlikely that there is any high-energy-consuming equipment that could cause a major spike in demand.

\begin{figure}[H]
 \centering
   \vspace{-5pt}
 \includegraphics[trim = 0 0 0 0 clip, width=0.8\textwidth]{sendem.eps}
  \vspace{-10pt}
 \caption{Plots of Usage and Demand Profile Generation and Histogram of Year Data}
 \label{sendem}
 \vspace{-25pt}
 \end{figure}

To fully understand the energy profile of the Senate house, histogram and as a cumulative distribution plots \footnote{See Figure \ref{loadprofile} in the appendix to see Senate House's load profile} were used to identify the typical demand of Senate House sees over the year, as well as the max demand the building experiences [@combined-heat-power-buildings]. Figure \ref{sendem} shows the demand profile of Senate House, providing insight into what requirements a battery system may need. It can be observed from in the histogram, that the demand of the Senate House typically falls between two points. One low peak representing morning and evening of 30KW and a second peak constituting the energy usage in the middle of the day, averaging around 80KW, but rarely ever exceeding 90KW. Insights from the load profile also identified a battery rated to 40KW would cover, 5000 hours of the year roughly 55\% of the year's usage.

## Definition of the New Temple Quarter Campus

Understanding the outline of new campus was required to create a valid assumption of its energy profile. At the time of writing, no building plans were available. Instead many assumptions about the likely size and use of the campus were used to create a representative energy profile \footnote{See Table ? In the appendix for a breakdown of how the new campus was sized}.

The campus will be designed for ~1500 resident students, having ~5000 staff and students on site during term. A range of facilities have been proposed for Temple Quarter Campus, however it is likely that the campus will constitute largely of tutorial rooms, a few lecture halls and offices. A meeting with John Brenton [@Jbrentmeet], made clear that creating an infrastructure to support postgraduate business studies made the most economical sense, and is likely to influence the Campus's design.

As tutorial rooms and office are similar to Senate House, It is assumed that the energy profile of Senate House will be transferrable to the new campus. It is unlikely the new campus will have any equipment that will distort the load profile greatly; where the campus is likely to have improved efficiency through employing the latest technologies in its construction and services (HVAC). Data on 125 rooms in halls of residence was also provided, with a higher degree of certainty of its applicability to the new campus. Footprints of both buildings were combined with laboratory data, testing the effects labs may have on any large spikes in energy usage. The final scaling factors used were:

* Senate House (7840sqm) - **7.9x**
* Hall data (2761sqm) - **7.6x**
* Lab data (1 Lab Use) - **4x**

### Energy Profile Tool

Due to energy usage data files beginning on different dates and running for various periods of time, these records required adjustment to be correctly scaled and combined. To fully meet the project's outputs and modelling requirements, a program was created to manipulate various half-hour energy use files. An algorithm was set up to read the data dates and then convert this data into realistic demand profile. To simulate lifetime energy usage, copies of the energy profile were concatenated for the length of simulation, checking that each year began on the next day in the week from the end of the previous year. It was imperative that dates aligned, to make sure results were valid as the difference in energy usage between weekdays and weekends (see section \ref{creation-of-senate-house-billing-model}), could cause the total savings to vary on a seven-year cycle pattern. Figure \ref{EnergyProfileTool} outlines the logic of this program.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.85\textwidth]{EnergyProfileTool.eps}
 \caption{Logic of Energy Profile Tool Create New Campus Data}
 \label{EnergyProfileTool}
 \vspace{-20pt}
 \end{figure}

## Definition of System Strategies

To fully understand the value of using battery storage, a representative simulations of how the battery would operate is required. This section defines the logic define the battery's operation. The model calculates both economical and technical battery performance based on the chosen battery strategies. The following section will discuss why the final strategies were selected, detailing their development.

### Red Rate Charge Avoidance Strategy

As outlined in section \ref{representative-bill-creation}, using energy consumed during Red rate periods was considerably more expensive than Amber and Green periods, making it a prime strategy. By switching the battery on during Red rate periods, then charging during Green periods, cost savings of up to 20\% could be made. Currently, for the University, Red rates apply between 5 and 7 PM on weekdays making it simple to forecast, alleviating the need for complex prediction systems highlighted in section \ref{forecasting-and-the-use-of-ess-in-load-shifting}. During this period the battery would be drained at a rate up to its maximum output power; requiring demand and usage data to be checked simultaneously. If the load exceeded max power, energy supply was capped at this value. The battery would continue to be drained until either its minimum capacity was reached, or the Red rate period elapsed. The battery would then be fully charged during green ensuring all capacity was available for the next Red rate period is entered. This method was repeated for the run-length of the simulation.

### Triad Avoidance Strategy

To correctly understand the effects of TRIAD avoidance in the model, TRIAD dates needed to be correctly identified. Using [@triad15], the dates: 4/12/14, 19/01/15, 02/02/15 were used; aligning with the original Senate House data set as the as a master template for the new campus (discussed in section \ref{energy-profile-tool}). These dates were used for the sequential years in the simulation as they were typical days in which TRIADS would fall. From observation, it was assumed that there was no increase in the University's usage during TRIAD periods, allowing for any day within that week to be used. To make sure these dates did not fall on fall weekends, days were checked and adjusted accordingly. It is assumed that daily variation in energy usage is negligible and instead energy trends are seen only on a monthly basis.

It was observed that TRIAD times all fell into Red rate periods, corresponding with the Red rate avoidance battery strategy. Using these dates and the time of 5:30, the TRIAD cost was calculated based on energy demand (kW). Battery usage was then measured against the TRIAD cost to understand the reduction in energy demand delivered by the battery. The reduction in TRIAD rate was a factor of the batteries max power supply and not capacity; due to the battery would only need to run for a few minutes to offset this charge.

At the end of each year in the simulation, usage on the three TRIAD dates were averaged to find the total cost. This was then spread evenly over the next year in the simulation, representing how TRIAD billing is split across each monthly energy bill.

### Battery Control Strategy

The importance of optimising battery longevity was highlighted in \ref{forecasting-and-the-use-of-ess-in-load-shifting} and \ref{battery-sizing-and-financial-modelling}. Section \ref{battery-degradation-parameters}, discussed the different variables which can affect a battery's longevity. An approximation of the battery degradation was taken, taking into account the effect of each of these variables as a battery control strategy.

The rated battery cycle life is taken to be the number of full cycles a battery can complete before it degrades to 80% of its original capacity \footnote{This is quoted to be 5000 cycles for the Tesla Powerpack, see Figure \ref{pp2tab}}. This figure was used as a measure for how the battery should perform based on a normal use case. Using this assumption, the battery was degraded proportionally by the fraction of its current cycle. \begin{wrapfigure}{r}{0.26\textwidth}
\vspace{-25pt}
  \begin{center}
\includegraphics[trim = 0 0 0 0, clip, width=0.25\textwidth]{BatteryImage.pdf}
  \end{center}
  \caption{Showing Battery Degradation}
   \label{BatteryImage}
   \vspace{-30pt}
\end{wrapfigure}
For each charging iteration, the new max capacity became slightly smaller, reducing the size of the cycle. A counter was used to sum each charge, resetting when its value equalled the current cycle size; signifying one complete cycle. Using this method, battery's were degraded on their on their use, degrading quicker as they deterioted. This followed the battery cycle degradation trend shown in figure \ref{batCapGen}.

By using the cycle-life metric, all battery degradation assumptions were based on the battery's operation and not the battery's chemistry. Assumptions on the batteries normal working parameters were made, limiting the battery to conform to these rules. This would prevent the battery running in a way that would majorly affect its longevity, making the prediction more accurate. These restrictions could be made greater or smaller at the expense of more or less chance of error on the battery health prediction. The following battery control measured were implemented:

* __Reduction in Depth of Discharge__: To reduce wear on the battery, the battery was confined to work within 10-90% of its current maximum capacity, allowing a maximum depth of discharge of 80%. Draining the battery can cause detrimental effects on the while overcharging can also do the same. Working within these two parameters follows similar principles applied by Tesla in their electric cars \cite{Charging49:online}.
* __Speed of Depletion__: A battery was never run above its max specified power. As the battery was rated at this value, it should be designed to cope with this level of use for no longer than 2 hours a day. The simulation will analyse the average discharge rate as a measure of the validity of the battery health
* __Temperature__: was assumed to remain within expected bounds, based on the assumptions made in section \ref{temperature}. Using the Red rate and TRIAD strategies would allow the battery to cool over weekends.
* __Charging__: The battery would only charge during Green periods, at a rate which would ensure the battery would be charged fully by the next Red period; this was based on the capacity required divided by the length of the Green rate period. Section \ref{Battery-Degradation-Parameters} suggested that charging at a lower speed, particularly during the last 10% of charge, made a large impact on the battery lifetime. It is assumed here that smart charging techniques such as trickling (seen on most modern smartphones), would be incorporated into the actual battery, but modelling these methods would not increase the accuracy of the model, so was been neglected.

* __Battery Efficiency__: This was regarded in the model by multiplying the energy drawn when charging by the additional losses caused inefficiencies. This assumption was made as it is likely that the battery once charged can supply what it has stored. The Powerpack 2 integrated inverter, supplies energy in AC, quoting its efficiency to this level (see figure \ref{pp2tab}). It is assumed that the quoted figure is very representative of the battery's efficiency in the system. Efficiency gains could also be achieved by designing the system, so it primarily sends power to DC first without transforming, this will not be evaluated in this project, see Figure \ref{pp2tab}.

\begin{wraptable}{r}{0.42\textwidth}
\vspace{-20pt}
\caption{Tesla Powerpack 2 Specification}
\vspace{-5pt}
  \begin{center}
     \includegraphics[trim = 0 0 0 0, clip, width=0.41\textwidth]{PP2spec.pdf}
  \end{center}
  \vspace{-20pt}
  \label{pp2tab}
\end{wraptable}

The model was run until the either runtime elapsed or the battery reached its end of life value (80\%), allowing results to be comparable. There are examples of batteries being used beyond their end of life cycle. Renault and connected energy have been investigating using the end of life Li-ion car batteries in home use applications \cite{Renaultt62:online}, \cite{UsedRena38:online}. It is believed there is still plenty of life remaining, and the increased probability of failure is less of a problem when used for bill reduction purposes. In the case of the new campus, there are little-associated costs with batteries after they have been installed if the battery has paid itself back, the battery will continue to generate profit. If unpredictability is seen to be an issue, this may be the case if emergency power is seen as a key value of having the battery, then it may be possible Analysing this value is out of scope for this project so an end of life battery was be classed as having no value.

## Input Parameters and Multi-Battery Simulation

To understand the optimum battery type for a given scenario, and then infer the total savings that the battery could generate; a large array of different batteries with different power ratings and capacities were modelled. Using actual data from Tesla \cite{Powerpac23:online}, the real costs of the different battery specifications were modelled. To find trends in the different battery types, the modelled required iterating through numerous different battery specifications. To reduce computation time, parallel computing was implemented to iterate each discrete battery scenario in the 0D model.

The following diagram depicts the model of the entire multi-battery system.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.8\textwidth]{largelogic.eps}
 \caption{Logic Diagram For Multi-battery Simulation}
 \label{largelogic}
 \end{figure}


To comply with the requirements set in section \ref{model-development-requirements} The following methods were used to optimise the performance of MATLAB model.

 * _Vectorisation_: storing data within multidimensional arrays and using vector operations
 *  _Variable Initialisation_: all matrices were initialised to reduce memory.
 * _MATLAB Function Reduction_: functions such as linear interpolation are cumbersome. These were recreated and simplified, solving tasks more efficiently.
 * _Parallel Processing_: Multiple cores on the processor were used to iterate through independent battery specifications in large multi-battery simulations. To achieve this successfully, code was rewritten to make all events discrete, substituted methods such as `while` and `break`. For large multi-parameter simulations, this can increased the processing time significantly,.
 *  _Profiler Tool _: Within MATLAB, the performance of code can be measured in the amount of time it takes to run. This tool was used to identify bottlenecks within the model.
 * _Single Integers_: Single integers are half the size of double integers, the default storage method for data within MATLAB. Double-precision floating point numbers allow the CPU to handle very large values. As this level of accuracy is unnecessary, use of 32bit single integers increased performance [@getreuer5685writing].
 * _Do Not Repeat Yourself (DRY)_: Coding technique to improve readability and performance of code, through use of functions.

The result of this method reduced processing time per battery from ~110 seconds to under 10 seconds. This was crucial in allowing the 113 different battery simulation run quickly. The runtime of the multi-scenario program was reduced to 220 seconds. This allowed different sensitivities studies to be run, greatly improving the functionality of the tool.
