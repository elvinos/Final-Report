
# Battery Model Definition

Through understanding the key design parameters highlighted in section \ref{battery-storage-technology-key-advantages-and-challenges}, a viable model of the battery system was defined. Data was obtained for Senate house (a large University office/study space building). This data was manipulated to create a characteristic energy demand and usage profiles for Senate; then developing insights from this into creating a representative New Campus energy profile. This section will define how the model was created, talking through the methodology used and any assumptions made. Figure \ref{SystemLogic1} describes an overview of the primary inputs, process and outputs of the model, discussed in greater detail in this section.

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=1\textwidth]{SystemLogic1.eps}
 \caption{Diagram Showing Key Inputs and Outputs of Model}
 \label{SystemLogic1}
 \end{figure}

## Model Development Requirements

A distinct set of modelling requirements were essential to ensuring that a functional model was created which corresponded to the project's objectives. By building a flexible, simple model, any unnecessary complexity was removed. This increased performance in execution, sparing both time and computational expense. A robust set of requirements also provides a basis for assessing the completeness of work. The following section defines these requirements.

### Zero-Dimensional vs. Three-Dimensional Modelling Approach

The zero-dimensional modelling approach is a technique widely used in the development cycle of a product, typically in the early stages. The objective of the zero-dimensional model is to define the key features and performance of the products, providing a detailed snapshot rather than a complete picture [@ZeroDMod80: online]. Three-dimensional models are implemented later in the product's development cycle where detailed analysis is necessary; this is done to predict any potential risks and failures before product production. In a zero-dimensional model, the system dynamics is a function of the time while in a three-dimensional model, the system dynamics is a function of the time and space. For this reason, a zero-dimensional model is much simpler and faster to solve, still providing an accurate picture; enabling a much large number of simulations.  This report assesses the value and feasibility of using battery systems, a zero-dimensional model is more appropriate, allowing for more battery configurations and strategies to be simulated.

### Code Optimisation

A time-based iterative modelling method, based on a zero-dimensional approach, was selected to model a large variety of different battery specifications. Running the simulation through time requires calculating large matrices:
\begin{align*}
\text{Length of Simulation}  \times 1440 (\text{minutes in a day})
\end{align*}
The model should be optimised for performance to minimise running times; helping improve the model performance and reduce data collection time, allowing for a greater amount of different battery specifications to be modelled. Possible methods to optimise the performance of MATLAB model are:

* _Vectorisation_: storing data within multidimensional arrays and using vector operations, can improve model performance.
*  _Variable Initailisation_: all matrices should be initialised to reduce memory.
* _MATLAB Function Reduction_: functions such as linear interpolation are. These should be recreated and simplified, recreating the task more efficiently.
* _Parallel Processing_: use multiple cores on the processor to iterate through independent battery specifications in large multi-battery simulations.

### User Interface

There is a strong likelihood of using this model for next year's group design project. The modelling functions outlined in the project's outputs, should operate independently from each other and work with a broad range of data. Being able to manipulate the model easily will mean others will be able to use the tools developed, making the model much more useful. The model, consequently, must allow for a range of inputs, which should be easily configurable. Desing the model in this way, will also simplify data collection reduce the risk of introducing a systemic error, associated with the user entering incorrect inputs or false logic. Dates and times of the energy usage data inputted in the model will have a large effect on the results. It is important therefore that the model can read data files and use their dates, to create accurate runtime usage data. This function on its own will be useful for the group in the following year so has been set as a secondary output of this project.  Being able to manipulate lots of data files easily will simplify the creation of detailed energy profiles for the new campus. The data outputted by the model must be clear and easy to interpreted by any user, with minimal post-processing; this will improve the model's ability to be a design tool is choosing optimum strategies and battery specifications.

### Ease of Development
Due to the nature of mathematical modelling, it is essential the model remain structured to allow for expansion as the project progresses. Model development will start simply and then be built upon, incorporating more strategies, and more detailed methods for modelling battery degradation; where each function will improve the validity of the results. Developing the model in this format will enhance the speed at which changes can be implemented within the model, allowing different strategies to be tested quickly. A  function based approach must be taken throughout the development process to allow the model reach to its expected size and complexity. Without functions, the model will have a poor structure,  becoming much harder to develop and debug.


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
