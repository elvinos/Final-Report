
# Validation of Model

## Data File

By using the model with real data first taken from Senate house, the tool which creates live data could be validated through integration and direct comparison to the original usage data. As no data could be gathered on how the demand profile looks for Senate house, assumptions were made on the type of operations the building fulfils (see the table below); this was compared to demand data at Princeton [@LiveData90:online]. Section \ref{battery-model-definition} describes how the model was initially tested on Senate House to validate whether the model produced expected results. After being validated on Senate House the model was then run of the new campus energy profile.

## Assumptions and Limitations
Table \ref{BatterAssump}, summarises all the assumptions discussed in section \ref{battery-model-definition}. To create a valid model, all assumptions must be based on logical expectations on all parameters that may effect the system, thereby using the following assumptions, the model is validated.

\begin{table}[H]
\vspace{-10pt}
\caption{Showing All Assumptions Made for Simulation}
\vspace{-5pt}
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=0.95\textwidth]{assumpp1.pdf}
 \label{BatterAssump}
 \vspace{-30pt}
 \end{table}

 \begin{table}[H]
 \vspace{0pt}
  \centering
  \includegraphics[trim = 0 0 0 0, clip, width=0.95\textwidth]{assumpp2.pdf}
  \vspace{-20pt}
  \end{table}

 The model is limited to working to these parameters only. Section \ref{ease-of-development}, set an objective for the model to be developed so these parameters can be easily changed, allowing for the model to be easily customised to work with a different set of assumptions. Peaks in demand being higher than modelled, energy pricing changing and DOD and discharge rate effect on capacity all have high levels of uncertainty in the model. These were sensitivity checked to understand the effects of these assumptions being incorrect.
