
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

\newpage

\begin{figure}[H]
 \centering
 \includegraphics[trim = 0 0 0 0, clip, width=1.3\textwidth]{Development-38.png}
 \caption{Image of Energy Bill For Victoria Rooms}
 \label{Development-38}
 \end{figure}

 \end{landscape}
\newpage

## Battery Degredation

\begin{wrapfigure}{r}{0.5\textwidth}
   \vspace{-20pt}
  \begin{center}
  \includegraphics[trim = 0 0 0 0, clip, width=0.49\textwidth]{capVol.jpeg}
  \end{center}
  \caption{Plot of the Relationship Between Battery Cycle Life and Voltage of Charge \cite{Choi2002130} }
  \vspace{-20pt}
\label{capVol}
\end{wrapfigure}

## Senate Load Profile

\begin{figure}[H]
  \begin{center}
    \vspace{-20pt}
   \includegraphics[trim = 0 0 0 0, clip, width=0.9\textwidth]{loadprofile.eps}
  \end{center}
  \caption{Load Duration Plot of Year Usage Data}
  \label{loadprofile}
\end{figure}

## Model Operation Parameters

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
