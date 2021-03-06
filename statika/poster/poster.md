---
title: 'Statika: managing cloud resources, bioinformatics tools and data'
author: 
    - Alexey Alekhin,
    - Evdokim Kovach,
    - Pablo Pareja-Tobes,
    - Marina Manrique,
    - Eduardo Pareja,
    - Raquel Tobes,
    - Eduardo Pareja-Tobes
date: 17.09.2014
institute: 'Oh no sequences! Research Group. Era7 bioinformatics, Granada, Spain.'
---

\begin{columns}[t] 

\begin{column}{\sepwid}\end{column}

\begin{column}{\onecolwid}


\begin{alertblock}{Introduction}

Statika is a set of Scala libraries

\begin{itemize}
\item which allows building \textit{well-structured} module systems
\item where dependencies are \textit{correct by construction}
\item and you know it \textit{before you run} anything
\end{itemize}

\end{alertblock}

\vspace{1cm}

\begin{block}{Basic notions}

\begin{center}\textbf{Bundle}\end{center}

A \textbf{bundle} is a thin wrapper for a tool, library, resource or any other component of your system:

\begin{itemize}
\item it may have dependencies on other bundles
\item it may do something in runtime, e.g. install a program or download some data
\end{itemize}

Bundles can be \textit{applied}, i.e. deployed to an EC2 instance

\vspace{1cm}

\begin{center}\textbf{Distribution}\end{center}

A \textbf{distribution} is a bundle, which can deploy other bundles (its members):

\begin{itemize}
\item it represents some environment, where you're going to use your bundles
\item being a member of a distribution means to work fine with this environment
\item distribution takes care of installing member dependencies first, and then the member itself
\end{itemize}

Distributions abstract over the \textit{cloud infrastructure}

\end{block}

\vspace{1cm}

\begin{alertblock}{Availability}

\begin{center}
\begin{tabular}{m{0.5\linewidth} m{0.48\linewidth}}
\includegraphics[width=\linewidth]{resources/logos/agplv3-logo.pdf} \newline Statika is free and open-source under the \mbox{AGPLv3} license & \includegraphics[width=\linewidth]{resources/images/qrcode.png}
\end{tabular}

See \href{http://ohnosequences.com/statika}{http://ohnosequences.com/statika}
\end{center}

\end{alertblock}



\end{column}


\begin{column}{\sepwid}\end{column}
\begin{column}{\onecolwid}

\begin{block}{Abstract module system}

\begin{itemize}
\item Bundles are represented as Scala types.
\item Their dependencies on each other are validated by the compiler --- i.e. \textbf{statically}.
\item Statika linearizes the types graph to get them in the right order.
\end{itemize}

\end{block}

\begin{center}
\includegraphics[width=\linewidth]{resources/images/StatikaLinearization.png}
\end{center}

\vspace{2cm}


\begin{block}{Artifacts management}

\textbf{sbt-statika} --- an sbt (simple build tool) plugin, which takes care of

\begin{itemize}
\item packing bundles into versioned artifacts (jars)
\item reusing sbt infrastructure to track dependencies on the artifact level
\item standardizing common settings, versioning and release process
\end{itemize}

\end{block}

% \vspace{1.5cm}

\begin{block}{Usage in bioinformatics}

\vspace{1.5cm}

First of all, there is a Statika distribution for bioinformatics tools, such as Velvet, Cufflinks, Tophat and Bowtie(2). See github.com/statika/bioinfo-dist/.

\vspace{1cm}
\begin{center}
\includegraphics[width=0.5\linewidth]{resources/logos/nispero-logo.png}\\
\large{\textbf{Cloud-computing System}}
\end{center}
% \vspace{1cm}

Nispero is a toolset for declaring scalable cloud-based systems for bioinformatics computations. It has pretty complex inner commponents structure, which is managed with the help of Statika.

% \begin{center}
% \includegraphics[width=0.9\linewidth]{resources/images/NisperoBundles.png}\\
% \vspace{1cm}
% \rule{0.9\linewidth}{.1pt}
% \vspace{1cm}
% \end{center}

\end{block}



\end{column}




\begin{column}{\sepwid}\end{column}
\begin{column}{\onecolwid}

\begin{block}{Usage in bioinformatics}

\vspace{1cm}
\begin{center}
\begin{tabular}[c]{m{0.3\linewidth}cc}
\includegraphics[width=\linewidth]{resources/logos/bio4j-logo.png} & \hspace{0.5cm} & \Large{\textbf{Graph Database}}
\end{tabular}
\end{center}
\vspace{1cm}

Bio4j is a bioinformatics graph database which integrates data from a lot of different sources:

\includegraphics[width=\linewidth]{resources/images/Bio4jModules.png}

% \vspace{1.5cm}

Every module has some inner structure:

\begin{itemize}
\item raw data from a data source
\item data importing process to the graph database
\item nodes and relationships type definitions
\item some abstract interface representing what you can do with this data
\end{itemize}

% \includegraphics[width=\linewidth]{resources/images/Bio4jModulesExampleIncremental.png}

So with Statika Bio4j achieves 
\begin{itemize}
\item simple data-import process
\item automized dependencies management
\item easy and robust deployment to AWS
\end{itemize}

\end{block}


\vspace{1.60cm}


\begin{alertblock}{Acknowledgments}

Statika is developed by the R\&D team of the Era7 Bioinformatics company\\

\vspace{1cm}
\begin{center}
\includegraphics[width=0.7\linewidth]{resources/logos/era7-logo.png}\\
\vspace{1cm}
\includegraphics[width=0.7\linewidth]{resources/logos/ohnoseq-logo.png}\\
% \vspace{1cm}
\end{center}

This project is funded in part by the ITN FP7 project INTERCROSSING (Grant 289974)\\

\begin{center}
\begin{tabular}{m{0.4\linewidth} m{0.4\linewidth}}
\includegraphics[width=\linewidth]{resources/logos/intercrossing-logo.png} & \includegraphics[width=\linewidth]{resources/logos/marie-curie-logo.png}
\end{tabular}
\end{center}

\end{alertblock}

\end{column}
\begin{column}{\sepwid}\end{column}


\end{columns}
