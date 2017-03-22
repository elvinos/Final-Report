
# Battery Storage Technology Key Advantages and Challenges

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

**Challlenges**

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

# Battery Model Definition

Understanding the key design parameters highlighted in section \ref{Development-of-Model-Advantages-and-Barriers-Assessment}. The model was created to capture as many of these drivers to maximise the models validity. Data was obtained for Senate house (a large University office/study space building). This data was manipulated to create a representative energy profile for the Senate and then the New Campus.

\hl{Overview of the final system Diagram}

## Model Development Requirements

### 0 vs 3D Modelling Approach

\hl{The 0D modelling approach is a technique widely used in the development cycle of a product, typically in the early steps of the cycle. The objective of the 0D model is to define the main characteristics and performance of the products. A 3D model is implemented later in the product development cycle to get a detailed analysis, to verify the accuracy of the 0D model and to predict risks and failures. In a 0D model, the system dynamics is a function of the time while in a 3D model, the system dynamics is a function of the time and the space. A 0D model is much simpler and faster to solve than a 3D model. This enables to run a large number of simulations and explore a large design space for our product.} [@ZeroDMod80:online] Due to the level of accuracy required to achieve this reports objectives in the model and the timeframe that the model had to be constructed in a 0D model was created using the variables stated in section \ref{input-parameters-and-multi-battery-simulation}.

### Code Optimisation

\hl{A time-based iterative approach, based around a zero dimensional approach, has been selected to model a large variety of different batteries. Running the simulation through time requires calculating large matrices which are number of days $\times$ 1440 (minutes in a day). The model should be optimised for performance to ensure that running times are minimised. This will help to improve model development and reduce data collection time. Possible methods to optimise the performance of MATLAB scripts are:
• Vectorisation – data can be stored and manipulated within multidimensional arrays. Using vector operations, rather than manually moving and manipulating data inside the array, can greatly improve model speed.
• Avoiding heavy processing MATLAB functions such as the linear interpolation function. Instead, simplified versions can be developed to perform the same task.
• Initialising variables within the model. All arrays should be initialised within the memory. This prevents MATLAB from needing to create extra space within the memory each time a value is entered into an array. This is especially important when dealing with large datasets, as it can prevent running out of memory.
• Parallel processing for loops can be used for independent repeating tasks. This can be applied when multiple batteries as each loop is independent of the other.}

### User Interface

\hl{The model developed through this research project is likely to be used in the group project in the following year. Consequently, it is important that the model is easy to run and use. A range of inputs are required for each lagoon which should be easily configured and managed. This will also improve ease of data collection for this project and reduce the risk of introducing a systemic error, associated with the user entering incorrect inputs. Model inputs should therefore be largely removed from the MATLAB script and kept within input files.
A level of intelligence should also be built into the model to determine if the user inputs are valid. This would increase the robustness of the model and prevent errors from occurring within the model. It will also help to improve the stability of the model, as incorrect data will be less likely to be inputted. However, this requirement is likely to be more relevant in the following year, when multiple users are generating data from the energy model. It is important that the model is able to handle a range of variable input conditions}

### Ease of Development
\hl{Due to the nature of mathematical modelling, it is essential the model is structured to allow for development and expansion as the project progresses. This allows functionality to be added to the model without a large amount of upfront work. It also improves the speed at which changes can be implemented within the model.
The use of functions within the script allows elements of the code to be re-used across the model. Nested functions (functions defined in the body of a parent function) can also be used when a large number of variables are required to pass back and forth between functions. This also provides modularity within the function and can reduce the amount of repeated code. It is important that a function based approach is taken through the development of the model in this research project due to the expected size and complexity of the model. Without this, the model is likely to have a poor structure and will be much harder to develop and debug.}


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

Defining how the batteries would run is imperative to understanding their economic feasibility. This section will define the logic used to define the operation of the battery and how the model was created to represent this.

Using the "live demand data", created in section \ref{Representative-Demand-Profile}, a Matlab script was created simulate through a lifetime use case of the the battery for both Senate house and the new campus energy profiles. A script was created which duplicated these data input files for the length of simulation (in years), checking that each year began on the next day in the week from the end of the last year. Making sure dates aligned is imperative to making sure results were valid as the difference in energy usage between weekdays and weekends, shifts the total savings into a 7 year cycle pattern. Energy usage and demand data was then run through a second function which applied three strategies understanding battery performance from a technical and economical standpoint.

### Red Rate Avoidance

As describe in earlier sections, the battery was limited to being switched on only during red rate periods. This period is always  between 5 and 7 on weekdays and has assumed to remain the same for the entirety of the batteries lifetime. During this period the battery was allowed to drain itself at a rate up to it's maximum output power. This required demand and usage data to be checked simultaneously, to make sure the battery had remaining capacity and was not over loaded. If the load exceeded its maximum value the supply of energy was capped at this value. As the battery was used, capacity was decreased proportionally until live usage exceeded the remaining capacity and the battery was drained to its minimum capacity and switched off. Or the rate rate period elapsed.

The battery was then set to begin charging at a set rate when the red rate period was entered a green rate period. The charging rate was set based on the amount of charge required divided over the length of the green rate period. Early discussion of battery life cycle optimisation suggested that charging at a lower speed, particularly during the last 10% of charge, made a large impact on the battery lifetime. It is assumed here that smart charging techniques trickling (seen on most modern smartphones), would be incorporated into the battery. However the only value which will effect the outputs of this model is the capacity when the next red rate period is entered, therefore not necessary in this model.

This repeats for the run-length of the simulation, measuring the amount of money saved against the original costs of unit rate charges.

### Triad Avoidance

To correctly understand the effects of TRIAD avoidance in the model, the dates correlating to each day needed to be correctly applied and matched against corresponding days. Using [@triad15], the dates: 4/12/14, 19/01/15, 02/02/15 were used as aligning with the original Senate data used as a master for the new campus. These dates were used for the sequential years for days TRIADS would likely fall. Their corresponding days of the week were checked to make sure they did not fall weekends and adjusted accordingly if found to be the case. It is assumed here that daily variation in energy usage is negligible and instead energy trends are seen only on a monthly basis. This means that it does not matter if the TRIAD lands on a Monday or a Friday, and instead the date corresponds best with predicted weather pattern- the only variable likely to cause observable differences on a calendar data (any other variables have been ignored, particularly as these will cancel out over time).

These periods were all between 5 and 7 corresponding with the battery strategy already in place. Using these dates and the time of 5:30, the TRIAD cost was calculated based on energy demand at this time. Battery usage was then measured against the TRIAD cost to understand the reduction in energy demand delivered by the battery. The reduction in TRIAD rate was a factor of the batteries max power supply and not capacity. As the battery would only need to run for a few minutes to offset this charge.

At the end of each year in the simulation the three TRIAD costs were averaged to find the total cost. This was then spread evenly over the next year in the simulation, representing how TRIAD billing is split across each monthly energy bill.  

### Battery Degradation Modelling

As highlighted in section \ref{battery-lifetime-assessment---understanding-battery-degradation} discusses the different variables which can effect a batteries cycle life. An approximation of the batteries was taken, taking into account the effect of each of these variables and placing a battery usage strategy in place. The rated battery cycle life is taken to be the number of full cycles a battery can complete before it has degraded to 80% of it's original capacity. This figure was used as it is the best metric for how a battery should perform based on a normal use case. The model uses this assumption to degrade the battery by the fraction of it's cycle life that it has charged up by. For each charging iteration the new max capacity becomes slightly smaller, reducing the size of the cycle. A counter is then run summing up the amount the battery has charged. When this equals the current maximum, a complete cycle has been fulfilled. The effect of this method means that the battery will degrade faster the longer it has been applied. This follows the mean trend of battery cycle life shown in figure \ref{batCapGen}.

Any assumptions made about battery degradation were based on battery operation and not the batteries chemistry. Assumptions were made on what constitutes "normal working parameters", alleviating extremes in modes that have an exponential effect on how the battery degrades.
To reduce wear on the battery, the battery was confined to work within 10-90% of it current maximum capacity, allowing a maximum depth of discharge of 80%. Draining the battery can cause detrimental effects on the whilst overcharging can also do the same. Working within these two parameters follows similar principles applied by Tesla in their electric cars \hl{add reference here}. The battery was never run above it's demand maximum (max power KW), however no factor was used to degrade the battery quicker if it operated at this factor (a known cause of wear). As the battery was rated at this value, it should be designed to cope at this level of use for no longer than 2 hours a day.

 Temperature was also assumed to remain within expected bounds. Britain only experiences hot days a few times a year and rarely drops below freezing, making it a better climate for battery operational temperatures than the states where average temperatures are a lot hotter. Using the two strategies defined above means the battery is only ever discharging or charging 5 days a week, with some charge on a Saturday mornings dependent on the battery selected. This allows the battery too cool down and perform any life enhancing cycling activities if relevant \hl{Consider how these two days could be used to improve the batteries lifetime}.   

The model was run until either the runtime reached it's end or the battery reached it's end of life value of 80%. This meant answer were comparable. It is worth noting that there are examples of batteries being used beyond their end of life cycle. \hl{This is being seen by Nissan/ Honda in recycling their car batteries to use in homes}, as there are little associated costs with batteries after they have been installed if the battery has payed itself back, the battery will continue to generate profit. However as there is a lot of unpredictability about whether the battery will fail, this has not been regarded in the model and instead seen as the asset no-longer holding any more value.

\hl{Diagram of Battery Cycling Degradation}

### Battery Efficiencies

Battery efficiency was regarded in the model by multiplying the energy drawn when charging by the additional loses caused inefficiencies. This assumptions was made as it is likely that the battery once charged can supply what it has stored, although some losses will be incurred when transforming back to AC again. It is assumed that the efficiency figure regards both transformations. Efficiency gains could also be achieved by designing the system so it primarily sends power to DC first without transforming. Efficiency however does not play a huge part in improving costs savings due to the difference between charging in green periods and the red rate being so significant.

### Input Parameters and Multi-Battery Simulation

In order to understand the optimum battery type for a given scenario, and then infer the total savings that the battery could generate; a large array of different batteries with different power ratings and capacities was modelled. This required iterating the model numerous times. To reduce computation time, parallel computing was implemented to iterate each discrete battery scenario in the 0D model.

The following Operational Parameters Were Used to Generate the Output Results Discussed in this report. Values stated as variables were varied per battery.
\begin{table}[H]
\begin{tabular}{p{4.3cm}p{8cm}}
\textbf{Upfront Costs}:& Variable\\
\textbf{Max Power}:& Variable\\
\textbf{Upfront Costs}:& Variable\\
\textbf{Depth Of Discharge \textit{(DoD)}}:& 80\% \\
\textbf{Cycle Life}:& 5000 [@TeslaPow57:online]\\
\textbf{Max Charge}:& $\frac{1-\text{DoD}}{2+\text{DoD}} \times$ CurrentCapacity\\
\textbf{Min Charge}:& $\frac{1-\text{DoD}}{2} \times$ Current Capacity\\
\textbf{End Life Value}:& 80\%\\
\textbf{Additional Costs}:& £0 \\
\textbf{Charge Rate}:& Max Power $\times$ 0.4 (In kWh per Half Hour)\\
\textbf{TRIAD Days}:& 04-Dec-2014, 19-Jan-2015, 02-Feb-2015\\
\textbf{TRIAD Rate}:& £33.55  (price per KW)\\
\textbf{Unit Rate}:&  6.832p\\
\textbf{Red Rate}:&  24.41p\\
\textbf{Amber Rate}:&  0.287p\\
\textbf{Green Rate}:&  0.161p\\
\textbf{Usage Variation $\sigma$}:&  $\frac{\text{Max Value + Mean Value}}{2}$ (For minute by minute granularity)
\end{tabular}
\label{inputparam}
\caption{Table Showing the Input Parameters of the Model}
\end{table}

The following diagram depicts the model of the entire multi-battery system.

\hl{Large system Diagram of the Logic behind the model}

 \hl{It was important that the model was as clear and simple as possible. To improve clarity within the model, structures were used to group variables. The benefit of using structures is the ability to pass them into a function. Using structures throughout the Lagoon Energy Model function and Multiple Lagoon Model script allowed all the required variables to be passed between the function and script using one structure. This greatly improved the structure and clarity of the model script.}

## Performance Optimisation of Battery Storage Model

[@getreuer5685writing]

* Use Profiler \hl{Within MATLAB, the performance of a code can be measured in the amount of time it takes to run. The MATLAB profiler is a useful tool which records the amount of time spend in the different functions called within a script. The profiler can be used to identify bottlenecks within the model.}
* Array Preallocation
* Vectorisation
* Reference Wildcards
* Delete Sub Matrices
* Convert to column vectors
* Parallel Computing For loops
* Minimised using MATLAB functions (linear interpolation etc.)
* Used single instead of double integers (half size of memory allocation). \hl{The default storage method for data within MATLAB is a double-precision floating point number (Mathworks, 2016). This method of representing a number within CPU memory is able handle very large values, however requires 64 bits per number. By storing numbers as a single-precision data type, only 32 bits are required, reducing the data size by a half. This helps to manage memory within the model.}
* DRY coding technique
