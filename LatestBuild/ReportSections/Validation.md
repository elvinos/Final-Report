
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
