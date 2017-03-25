# Project Introduction and Objectives

The announcement of the new £300million University of Bristol Campus in Temple Quarter \cite{November58:online}, presents an exciting new opportunity for digital innovations in sustainable energy. The government's 2020 smart meter rollout, is the first step for creating a smart energy grid. This is key for the UK to achieve a low-carbon, sustainable and efficient energy system for the future \cite{SmartEne79:online}. The UK's vision is mirrored in the University of Bristol's new strategy, as it seeks to boost its world-class research capacity and promote innovation in policy, to increase sustainability \cite{universi93:online}. The creation of a world-leading campus is an attractive means for the University to realise its vision. Consequently, the aim of this group project is to explore new digital technologies, to reduce both energy costs and energy usage to set a precedent in university campus sustainability.

\begin{figure}[H]
\centering
\includegraphics[width=1\textwidth]{GroupDiav2.eps}
\caption{Group Design Project Diagram Showing Relationships Between Individual Projects}
\vspace{-20pt}
\label{groupDia}
\end{figure}

Figure \ref{groupDia} describes the relationships between the individual project themes, where research in occupancy sensing, smart metering and building services will evaluate how energy usage in the new campus can be optimised. Projects looking at smart thermal grids, energy system interactions and peak demand reduction, analyse methods to reduce the university's energy costs; providing financial incentives to increase the campus' sustainability. The 5^th^ year group project will unite this research, creating a smart "brain" \cite{pbmeet} through combining usage data with new technologies and strategies, providing a business case to develop sustainable energy services on the new campus, pushing the University to meet it is carbon neutral 2030 goal \cite{universi93:online}.

## Individual Project Introduction

This project report investigates the feasibility of using energy storage systems (ESS) to reduce energy charges for the University of Bristol. This will be implemented in the new Temple Quarter campus, seeking to provide a comprehensive cost based analysis for investing in energy storage technology. By focusing on reducing charges related to peak demand, (periods where load on the grid is greatest \cite{WhatisPe67:online}) overall campus sustainability will rise. Within the project, the university’s energy profile and billing structure are analysed and simulated, which defines the bespoke energy requirements of the new campus. A comprehensive technology study of the different ESSs evaluated the feasibility of various systems, down-selecting the most appropriate battery for modelling. Through further evaluation of how the selected battery system would function, a model was designed to simulate battery system strategies. To find an optimum solution for the system's design concerning the system's capital cost against savings made from energy bills.

The overall outputs of the project for use in the $5^{th}$ year group design project are:

* _Cost Based Analysis Business Case_:  for investing in battery storage technology
* _Energy Profile Tool_:  to build and understand the new university campus’ Demand
* _Optimised Battery System Model_: producing best storage solutions based on energy profile tool

## Objectives

To achieve the projects outputs, the following detailed objectives were defined:

**Literature Review**
\begin{enumerate}
\item Perform a detailed literature review, and market analysis of current energy storage technologies and modelling conducted in evaluating using ESS to reduce peak energy demands, highlighting relevant techniques and limitations.
\item Investigate the applicability of different energy storage solutions for use in the University's new campus, comparing parameters such as; power-ratings, capacity, discharge times and costs to down-select a battery system for modelling.
\end{enumerate}

**Definition of System Strategies**
\begin{enumerate}[resume]
\item Define battery system strategies, establishing the key performance variables. This objective will include an investigation into measuring the performance of the battery system over time and evaluation of the best methods of using the battery.
\end{enumerate}

**Modelling and Analysis**
\begin{enumerate}[resume]
\item Analyse the university’s current peak demand charges; understanding the university’s current demand charge structure and collecting typical energy usage data.  
\item Create a tool to generate demand profile (kW) from half-hourly usage (kWh) data provided defining energy profile of the new campus.
\item Create a model simulating the use of battery strategies to change the energy demand profile of the new campus, comprising of three stages:
\begin{enumerate}
\item A simulation of using the battery system against a current university building, analysing the effect of the system for use as a datum.
\item A simulation of using the battery system in the new university campus
\item An assessment on the optimum battery design to select based on the new campus's energy profile
\end{enumerate}
\end{enumerate}

**Evaluation**
\begin{enumerate}[resume]
\item Evaluate results of the simulation, concluding on the effectiveness of different battery systems. A cost-based analysis will be used to measure the feasibility of the different energy storage systems for the university comparing the value of the system against current challenges in using the new technology.
\end{enumerate}

# Background and Summary of Key Work and Reference

The following literature review provides a comprehensive overview of using Energy Storage Systems (ESS) to lower energy costs. Using batteries in this manner is still novel, with a broad range of ESSs and use strategies available for evaluation, where their use in different situations can produce dramatically different results. By having a comprehensive understanding, the scenario, the best strategies and energy storage technologies for the new university campus are determined. This section is broken down into the following:

* \ref{how-reducing-the-universitys-energy-bill-increases-sustainability} - How Reducing the University's Energy Bill Increases Sustainability
* \ref{university-energy-charges} - Background into the University of Bristol's current energy billing structure
* \ref{current-peak-demand-management-methods-and-energy-storage-systems-usage} - An understanding of the current methods of reducing energy bills through peak demand management and evaluation of the university's current methods
*  \ref{peak-shaving-systems-literature-review} - An overview of research conducted into using energy storage system to reduce bills; including a variety of different case studies and analysis on ESSs financial return on investment (ROI). This research will highlight specific areas to be investigated in section \ref{battery-storage-technology-key-advantages-and-challenges}how
* \ref{peak-shaving-technologies---electrical-storage-system-ess} -  Analysis of the applicability of different ESSs, down-selecting the most viable candidate for modelling

## How Reducing the University's Energy Bill Increases Sustainability

The UK's energy grid uses many methods of generating the power to meet demand. This energy comes from both clean (hydro, wind solar e.t.c.) and dirty energy (coal, gas e.t.c.). Due to the nature of most clean technologies, these sources are used to meet the UK's base load (power usage during off-peak periods) \cite{GBNation22:online}. When there are periods of the day when energy usage is higher, (peak- demand) additional fast-acting dirty sources like combined cycle gas turbines are used to meet this demand \cite{Reducing94:online}. These periods of a high spike in demand are charged much more significantly, for this reason, highlighted in \cite{7555793}. ESS proposes a new way of levelling out load on the grid, reducing the need for fast, responsive dirty technologies to be used. The reduction in emissions for the university by using energy storage technologies to reduce peak demand can reduce between 250 - 360gCO2/kWh \cite{Part1Att26:online}, while having the potential to save the University a significant amount of money.

## University Energy Charges
The University of Bristol's infrastructure spans across three sites; the City Centre, Stoke Bishop and Langford. Across these locations, the majority of facilities receive separate energy bills, allowing a high degree of granularity in the understanding energy charges \cite{Jbrentmeet}. The University receives charges bundled together under four distinct themes \cite{Jbrentmeet}, described below discussing how using batteries could reduce this cost.

\begin{enumerate}
\item \textbf{Distribution Use of System (DUoS)} - This section of the bill includes the capacity charge and unit charges.
\begin{enumerate}
\item \textbf{Unit Charge} - Unit charges come at three different rates, green, amber and red \footcite[See page 27 of][]{SWEB201492:online}, depending on the time of day. Energy costs during red periods are significantly higher (between 5pm-7pm). For Western Power (University's current supplier), there is a 17000\% increase in price during these periods \footcite[25.405 p/kWh in red periods against 0.147p/kWh in green periods][]{SWEB201492:online}. Reducing unit charge will be the main method of reducing peak demand charges, where an ESS should be used during Red rate periods and charge in only green periods. Unit Charges make up 22\% of the bill  (see Figure \ref{Development-38}).
\item \textbf{Capacity Charge} - this is where the customer pays for a maximum demand level in kW \cite{Deconstr52:online}. The capacity charge is set higher than the actual maximum demand, reducing the risk of breaching this threshold. If breached, the customer incurs substantial penalties, and the supplier increases the threshold for the next billing period. By levelling off peaks in energy demand, the capacity charge threshold can decrease. Capacity charges make up a 4\% of the monthly bill  (see Figure \ref{Development-38}) where the risk surpassing the threshold exceeds any savings seen through implementing an ESS.
\end{enumerate}
\item \textbf{Transmission Network Use of System (TNUoS)} - These come from three half-hour periods when the UK's National Grid demand is greatest, referred to as TRIADs. These dates lie between November and February and must be separated by at least ten days during the financial year \cite{TriadsWh7:online}. The average max peak demand across the three Triads \cite{TNUoSTra99:online}, is multiplied by a tariff for the respective zone in cost per kW \cite{TNUoScha93:online}. Combined they become the TNUoS charge, added to the customer's end of year bill. The University has become quite good at forecasting these periods \cite{Jbrentmeet}, making it possible to schedule ESSs to reduce peaks during these periods. To effectively mitigate this charge, an ESS must be able to provide substantial power demand (kW). TRIADS currently encapsulate 7\% of the monthly bill ( see Figure \ref{Development-38}).
\item \textbf{Feed-In Tariff (FIT)} - Based on feeding back energy to the grid. Dependent on the battery system selected, there is potential to increases the value of the ESS by leveraging this charge. This charge is highly complex and frequently changing so will not be evaluated in this project.
\end{enumerate}

## Current Peak Demand Management Methods and Energy Storage Systems Usage

The term "peak demand reduction" is synonymous with peak shaving; the ability to control energy usage during intervals of high demand, to limit or reduce demand charges \cite{schneiderRECPS}, \cite{baldorPS}. Traditionally there are two methods for reducing peak demand for industrial complexes \cite{schneiderRECPS}. These are:

* **Load Shedding**: This is reducing energy usage, by switching off certain systems during periods of peak demand \cite{6199851}. An intelligent scheduling system or a simple forecasting tool can be used to execute load shedding \cite{Reducing37:online}, where systems are switched off autonomously or manually. Often load shedding is calculated daily using a schedule to set a fixed maximum energy limit  \cite{6938948}.Load shedding predictions methods will be useful in defining the strategy that the energy storage system will use.
    * *Limitations*: Forecasting errors can significantly reduce the effectiveness of this system, where reactive methods are often better \cite{6938948}. Getting university staff and students to change their usage habits, to shift load in peak times appears unfeasible and potentially more costly \cite{Jbrentmeet}. Experiments conducted by the University of Copenhagen have further supported this opinion \cite{copenmeet}.
* **On-site Generation**: Adding off-the-grid capacity to the consumer \cite{schneiderRECPS}. The University currently uses some generator to reduce TRIAD charges. Generators are run roughly ten times a year during periods when the UK's energy load is greatest. \cite{shen2016} shows research supporting the financial feasibility of running diesel generators during these times. Due to the environmental impact of using diesel generators, an ESS would act as an improved replacement for this method for reducing TRIAD charges.
    * *Limitations*: The University currently has 0.5MW of PhotoVoltaic (PV) installed using nearly all available space \cite{Jbrentmeet}. These PV's provide only 0.5\% of the total energy demand, meaning the use of on-site generation to offset peak demand has a negligible effect in flattening the University's demand. Pairing batteries with PV as a method of supply levelling appears unfeasible in the context of the University.

In addition to these limitations, statistics such as "40% of energy consumption in the campus comes from 5% of the space, predominantly labs” \cite{brentemail}, make the University campus a unique case study for peak demand saving, where energy storage systems appear more attractive than traditional techniques.

IODICUS, is a current University project, looking at reducing energy costs, by improving the amount of sensing data around the university's usage. This project produced middleware for an IoT deployment of energy sensors/actuators, and software to explore the resulting ‘big data’ of the sensors \cite{priestemail}.  Although the project did not evaluate using ESSs, the outcome of improving sensing data will help to improve the chosen ESS performance.

There are a limited number of commercially available solutions that use ESSs to reduce peak loads directly. ABB offers energy-storage, smart-grid, products which perform load levelling at grid level \cite{abbpeakshave}. These systems are designed primarily for supply levelling, using forecasting methods and extensive ESSs to offset excess energy supply produced from renewable energies \cite{5559470}, rather than focusing on reducing its customer's energy bills. One Cycle Control have created technologies to regulate peak-load and mitigate peak demand charges for commercial/industrial facilities using Li-ion batteries \cite{peakload38:online}. The technologies proved effective at reducing peak demand charges, but highlight that the steep cost of the ESSs reduces the system's financial feasibility \cite{Demonstr51:online}. Being able to sense peak loads and respond actively will maximise the performance of the system, while the ESS chosen will have the greatest effect on the systems cost. Section \ref{peak-shaving-technologies---electrical-storage-system-ess} evaluates these two different technologies. Based on there being no direct commercial solution this report sets to understand the components required to create an effective energy storage solution for reducing the university's new campus energy bills.

##  Peak Shaving Systems Literature Review
Acknowledging limitations in commercial peak-shaving ESSs, it is crucial to understand current research in using ESS technology to design an efficient system architecture. Research is grouped, highlighting each section's significance and relevance to the development of the modelling the energy storage system.

### Forecasting and the Use of ESS in Load Shifting
Using energy price forecasts, an ESS can be switched on to shift energy costs; purchasing energy at a cheaper rate, using this energy during peak times. Due to the gap in energy prices, demand charges and investment costs for an ESS, NaS, Li-ion and Flow batteries, a basic on/off algorithm to shift energy purchasing from peak to off-peak times has not been proven to meet a viable return on investment (ROI) \cite{7555795}. This Italian case study had very different pricing schemes to the university, meaning further investigation may find that this technique is feasible. \cite{5590194} used real hourly spot prices to decide the best times to turn on and off Vanadium Redox Batteries (VRB) and Polysulfide Bromide Batteries (PSB). Through sequential quadratic programming (SQP), battery sizes were optimised, finding PSB's had a better business case for load shifting. The fundamental differences between \cite{7555795} and \cite{5590194}, were the energy saving strategy and granularity of the pricing data used. \cite{6938948} evaluated different control strategies combining many forecasts to reduce errors in peak shaving over a monthly period. Weighted and lowest error forecasts were the best strategies for an energy management system and should be added to the system strategy if forecasting is used. \cite{Bennett2015122} added a real-time operator to create an intelligent scheduling system for home prediction. This system significantly improved the state of charge of the battery, freeing more energy for use in reducing peaks, highlighting that forecasts combined with real-time information can increase the performance of the system further.  Modelling development will research:

* the implications of battery health on the lifetime value of the battery, for the battery selected
*  understand if the University's energy usage data is responsive enough for a real-time intelligent scheduling system

### Supply Levelling
Supply levelling is the most common use for ESS \cite{iearoadmapes}, using large batteries to reduce power fluctuations brought by the use of renewable technologies \cite{7324861}, \cite{7564619}. Supply levelling works by storing excess supply, reducing peaks in the grid rather than in demand. The technology is, therefore, similar to peak demand shaving. \cite{Allik20161116} looked at improving supply for a residential home. Shiftable water heating was identified to account for 50% of household electricity use, so was used as the primary storage device. Excess load from wind turbines was used to heat water in excess supply periods bypassing an inverter improved energy losses. \cite{Leadbetter2012685} supports this research. Minimising conversion through inverters makes a large difference in the efficiency of the system. Modelling development will therefore investigate:

* the effect energy conversion on the ESS performance
* using heat as a secondary storage method

### Battery Sizing and Financial Modelling
There are numerous studies, analysing the business cases for ESSs. \cite{7555795} and \cite{7555793} model the use ESSs broadly, to reduce the cost of all energy charges, revealing that the ROI is unlikely to be feasible beyond 2020. Papers including \cite{1300158} and \cite{6175723} evaluated financial models for particular case studies, showing that bespoke solutions achieved greater peak shaving reductions than returns promised by current generic products \cite{abbpeakshave}. \cite{7555795}, \cite{7555793}, \cite{1300158}, \cite{6175723} and \cite{20164002874437} all present a strong arguments that a bespoke solution for the University will provide a better business case for ESS than generic commercial technology.

Investigating the benefits of a decentralised system, reducing peaks on a small scale rather than using one large central ESS,  \cite{6604477} analysed both peak shaving and battery longevity for a large data centre.  Through both experimentation and modelling,  \cite{6604477} showed that when regarding the batteries lifespan, the ability to regulate load through a series of batteries can be more favourable than a centralised system. Research conducted by \cite{6348200} and \cite{Demonstr51:online} also both support using a decentralised system. A simulation of the impact of lithium-ion batteries operated under a peak-shaving control algorithm identified cost-optimal battery configurations and their impact on grid demand, revealing that small short duration batteries were more favourable and cost effective for the customer, further supported by \cite{20164002874437}.

\cite{20160601898032}, \cite{Levron201280} all \cite{5371839} all show alternate ways of optimising the battery sizing configurations. \cite{5371839}, used a non-numeric modelling method, focusing on ultra-capacitors to find the optimal ESS. The results emphasised the constraint of storage capacity, showing an exponential decrease in value gained after a particular size of ESS. Finding the required battery size and power for different University scenarios will be the primary focus of this project's model.  \cite{Levron201280} created an analytical model, using energy bands to regulate peak load, giving an optimum storage size for a given system;  this was a straightforward and efficient method of modelling battery usage. \cite{20160601898032} looked specifically at Vanadium Redox Flow Batteries (VRFB) arguing benefits over other ESS methods, producing a MATLAB/Simulink for a residential use case, showing that VRFB can regulate its frequency efficiently, due to its fast response time, while still performing peak-shaving services. This project proposes using a similar modelling technique to \cite{20160601898032}, incorporating more ESSs. This research highlights:

* modelling techniques to consider when developing the optimal configuration of the battery to purchase
* that the model should assess the effect of labs on the energy profile of the building, to see if there is a business case for purchasing multiple batteries than just one


## Peak Shaving Technologies - Electrical Storage System (ESS)

The selected Electrical Storage System (ESS) will govern the cost and feasibility of a peak shaving system. An ESS converts electrical energy into a form stored for later use \cite{Chen2009291}.  Electrochemical batteries characterise low maintenance, high round-trip efficiency, long cycle lives and high energy density's; arguably being the most appropriate technology for peak shaving \cite{liao2016a}, \cite{Dunn928}. Batteries, therefore, have been chosen as the main focus for this study. The various storage methods can be characterised for different uses summaries below:

* **Energy Management:** for large scale storage, typically used by power plants for load levelling and ramping/load following.
    * Pumped Hydroelectric Storage (PHS), Compressed Air Energy Storage (CAES) and Cryogenic Energy Storage (CES) are the conventional technologies for high generation above 100MW. All these methods are on a scale too large to be considered for this project.
    * Large-scale batteries, flow batteries, fuel cells, solar fuels, CES and Thermal Energy Storage (TES) are suitable for medium-scale energy management with capacities of 10 – 100 MW. These are appropriate for consideration for this project.
* **Power quality:** fast response times improve power quality allowing techniques such as the instantaneous voltage drop, flicker mitigation and short duration uninterrupted power supply
    * Flywheels, Batteries, Superconducting Magnetic Energy Storages (SMES), capacitors and ultracapacitors have millisecond response time lower for storage sizes less than 1 MW - suitable perhaps in addition to large scale battery. Flywheel efficiency is too low for operational use, so has been removed from this study.
* **Bridging power:** Relatively fast response (< 1 s) but also have relatively long discharge time (hours). The typical power rating for these types of applications is about 100 kW – 10 MW.
    * Batteries, flow batteries \cite{flowbatstan}, fuel cells and Metal-Air Cells\cite{Chen2009291}, \cite{batuni}.

By removing energy storage methods that would not be appropriate for the system a table was created \footnote{See table \ref{battabs}, in the Appendices} comparing ESSs. Batteries along with capacitors provide the response time \cite{Choudar201521} and efficiencies required to make the system justifiable, where only rechargeable batteries were compared.

## Battery Selection - Tesla Power-pack 2

Due to the maturity of the technology, the fast frequency response in delivering power, Li-ion batteries were selected as the most viable option for achieving the project's aims.  Due readiness in information around performance and price, the Tesla Powerpack 2 was chosen for this model; where competitors EOS and BYD lacked information about their pricing structures making it difficult to validate any results the model would produce. The model will use Teslas current costs but will evaluate the effect of competition and improvements in  Li-ion performance in driving costs down further.

\begin{figure}{H}
\caption{Tesla Powerpack 2 Specification}
  \centering
     \includegraphics[trim = 0 0 0 0, clip, width=0.49\textwidth]{PP2spec.pdf}
\end{figure}

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

# Validation of Model

## Data File

By using the model with real data first taken from Senate house, the tool which creates live data could be validated through integration and direct comparison to the original usage data. As no data could be gathered on how the demand profile looks for Senate house, assumptions were made on the type of operations the building fulfils (see the table below); this was compared to demand data at Princeton [@LiveData90:online].  

## Model

\hl{ADD Model validation thoughts, short as Assumptions hope to capture why the model is valid based on what has been used, validation table (excel) place simple calculation in body, additional thoughts on sensitivity analysis}

## Limitations / Assumptions

\hl{Create Full Table of Assumptions - ADD TOO HERE}

* Office buildings are unlikely to have highly peaky demand profiles as there is no large devices that could cause spikes
* Red rate times remain the same for the entirety of the batteries lifetime
* Normal distribution of energy demand between each half hour period
    * Sigma = average between mean of data and max of data
* Trickle charging and minimum charge rate employed
* Daily Variation- negligible
    * Other variation in energy use ignored
    * Weather the only contributor worth noting
    * TRIAD dates kept as close as possible to the original (no weekends)     
* Battery operation assumptions
  * Does not overheat
  * Run within normal working parameters
* Battery chemistry assumptions
    * Cycle life rating of battery indicates degradation in normal use case
* Battery efficiency losses lost on charging
    * Figure quotes both battery transformation

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

 It can be observed from Figure \ref{DOD1} that batteries whose capacity if less than 3000kWh, fall into two categories; one of high mean depth of discharge between 70-80\% and one with a mean depth of discharge around 50\%. This is a result of the relationship between capacity and max power, limiting the possible depth of discharge that the battery could reach in the two hour period that the battery is run.

 It is recommended that the designer should consult this graph in order to gauge how accurate the degradation estimate may be.

# Conclusions and Future Work

## Conclusions on Modelling Tool

* This project set out to create multiple tools that would be useful in both evaluating the value of a battery system whilst being flexible tools that can be used in the 5th year group project.
* _Energy Profile Tool:_  to build and understand the New University Campus’s Demand
* _Optimised Battery System Model:_ producing best storage solutions based on energy profile tool
* _Business case:_ for battery technology investment



## Conclusions on Results

* Model confirms that it is financially feasible to purchase and use a battery to reduce energy bills
* Optimum battery can be selected using different values metrics based on the usage profile inputed.
* A 7 year payback period is lower than warranty on the battery, eliminating any risks in incorrectly modelling the batteries degradation
* After the battery has paid itself back there is nothing stopping it continuing to run until it ceases to function. Little maintenance is required after its is installed, so nearly all savings are instantly realised, this means the battery could theoretically continue to generate savings for the lifetime of the building (50 years)
* Due to the modular design of the Tesla Powerpack, after the system is initially installed it is feasible to swap the batteries out after they have worn out.
* The simulation is ran for a long period of time (25 years), there is a large amount of unpredictability particular in energy tariffs, that could dramatically alter the value of the battery system over it's life time. \hl{the sensitivity study showed.....}.

\hl{Refer Back To Challenges and Compare how these challenges are either overcome or still barriers}

* _Costs of Purchase too high_: the model proves that this barrier has been over come. As the battery will be purchased as an asset along with the buildings, land and other equipment that will be purchased for the new campus, it can be assumed that a very low interest rate will be taken on the battery.
* _Lifetime/ longevity of the battery too low_: Model of degradation shows that the lifetime of Li-ion is now feasible based on the battery being run in a controlled manner optimising it's longevity.
* _Frequent change of regulation and barriers to entry_: This is still the largest barrier to entry. Discussions with Western Power \cite{wpMWMD}, noted that DUoS prices are very likely to change over this period. Due to the added flexibility that fast frequency response energy storage methods such as Li-ion batteries bring, it is in the energy suppliers interest to encourage customer to purchase this technology rather than penalise this. Much of further change in regulation may therefore support using Li-ion batteries, which could increase the batteries value further in the future.
* _Negative environmental effects:_  \hl{expand further using references } \cite{daniels2013financial}
* _Technology still maturing_, Li-ion batteries have not been used in this manner before, for extended periods of time. However Tesla has been using batteries for over 10 years and has gathered some of the best minds to understand how their batteries will function. A lot of research around Li-ion has been conducted showing that on a smaller scale the technology is mature enough. The nature of scaling should have no additional effects on the batteries performance. As the way in which the battery will be operated is well modelled, using strategies working in the batteries design parameters no undesired load scenarios should be place on the battery.

## Future Work

* Can apply this model directly into 5th year, using the data tool to understand energy demand on a range of different sources including heat and gas. Transferrable to evaluating smart thermal grids with the use of CHP
* Further development of the degradation model and testing, to validate assumptions, work to be completed with Tesla
* Evaluate other methods such as frequency response to determine if additional value can be created
* Model the value of having a fixed demand profile for the new campus could have in reducing it's connection fee (there will be large upfront costs incurred on building the supply lines for the new campus, if this can be reduced by using batteries, how much could be saved ?)

\newpage
\section{Appendices}

\begin{figure}[H]
\centering
\includegraphics[width=1\textwidth]{battypes}
\caption{Diagram Showing Batteries Catorgised for Their Use Case \cite{Dunn928}}
\label{battypes}
\end{figure}

\begin{landscape}

\begin{table}[H]
\centering
\includegraphics[width=1.3\textwidth]{battab.eps}
\caption{Table Showing Battery Performance}
\label{battabs}
\end{table}

\end{landscape}
