---
title: 'Bio4j: the bioinformatics data platform'
author: 
    - Pablo Pareja-Tobes,
    - Alexey Alekhin,
    - Evdokim Kovach,
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

        \vspace{2cm}

        \begin{alertblock}{What is Bio4j?}

            \textbf{Bio4j} is a bioinformatics graph-based data platform  
            \textbf{integrating} the most representative \textbf{open data sources}  
            around \textbf{protein information}

        \end{alertblock}

        \vspace{1cm}

        \begin{block}{Data sources}

            \begin{itemize}
            \item \textbf{UniProt KB (SwissProt + Trembl)}
            \item \textbf{Gene Ontology (GO)}
            \item \textbf{UniRef (50,90,100)}
            \item \textbf{RefSeq}
            \item \textbf{NCBI Taxonomy}
            \item \textbf{Expasy Enzyme DB}
            \end{itemize}

        \end{block}

        \vspace{1cm}

        \begin{block}{Data as a service}

            \begin{tabular}{m{0.5\linewidth} m{0.48\linewidth}}
            \begin{itemize}
            \item Data distribution
            \item Scalability
            \item Cost-effectiveness
            \end{itemize}
            & \includegraphics[width=\linewidth]{resources/logos/aws-logo.png}
            \end{tabular}

        \end{block}

        \begin{block}{Graph databases}

            \begin{itemize}
            \item Data is stored in a way that \textit{semantically represents its own structure}
            \item Incorporating new data is easy $\Rightarrow$ it's \textit{scalable}
            \item \textit{Vertex-centric} (local) indexes allow to overcome the supernode problem
            \end{itemize}

        \end{block}

        \vspace{1cm}

        \begin{alertblock}{It's free and open!}

            \begin{center}
                \begin{tabular}{m{0.5\linewidth} m{0.48\linewidth}}
                    \includegraphics[width=\linewidth]{resources/logos/agplv3-logo.pdf} \newline Bio4j is free and open-source under the \mbox{AGPLv3} license & \includegraphics[width=\linewidth]{resources/logos/bio4j-logo.png}
                \end{tabular}
            \end{center}

            Developement process is \textbf{100\% public}. \\ 
            Only \textbf{Open Data} is integrated. See \\

            \begin{center}
                \huge{bio4j.com}
            \end{center}

        \end{alertblock}

    \end{column}


    \begin{column}{\sepwid}\end{column}

    \begin{column}{\twocolwid}

        \vspace{2cm}

        \begin{center}
        \includegraphics[width=\linewidth]{resources/images/domain-model.png}
        \end{center}

        \begin{columns}[t]

            \begin{column}{\onecolwid}

                \begin{block}{Bio4j domain model}

                    Bio4j database has a \textit{well-defined} domain model and all nodes and relationships comply with this abstract model.

                    \begin{itemize}
                    \item $10^9$ edges of $\sim150$ types
                    \item $2 \times 10^8$ nodes of $\sim40$ types
                    \item $6 \times 10^8$ properties
                    \end{itemize}

                \end{block}

                \vspace{1cm}

                \begin{block}{Different layers of Bio4j}

                    Different \textit{graph topologies} at the storage level,  
                    same \textit{domain model} in the client's code.

                    \begin{itemize}
                    \item Abstract \textit{domain model} with precise typing.
                    \item Universal \textit{Blueprints} implementation.
                    \item \textit{Technology-specific} versions:
                        \begin{itemize}
                        \item \textbf{Neo4j DB} 
                        \item \textbf{TitanDB}
                        \item \textbf{DynamoDB} (WIP)
                        \end{itemize}
                    \end{itemize}

                \end{block}

                \vspace{1cm}

                \begin{block}{Use cases}

                    \begin{itemize}
                    \item Era7 Bioinformatics:
                        \begin{itemize}
                        \item \textbf{BG7} genome annotation
                        \item \textbf{Metapasta} metagenomics analysis
                        \item Comparative genomics, network analysis, genome assembly
                        \end{itemize}
                    \item Ohio State University:
                        \begin{itemize}
                        \item Integration and analysis of Chip-seq data
                        \item Modeling genomic information and gene regulatory networks
                        \end{itemize}
                    \item Berkeley Phylogenomics Group:
                        \begin{itemize}
                        \item Graph database for Big Data challenges in genomics developed on top of Bio4j
                        \end{itemize}
                    \end{itemize}

                \end{block}

            \end{column}

            \begin{column}{\sepwid}\end{column}

            \begin{column}{\onecolwid}

                \begin{block}{Flexible module system}

                    \textbf{Statika} helps to manage dependencies between modules and simplifies import and deployment in the cloud.

                    The importing process is \textit{modular} and \textit{customizable} allowing you to import just the data you are interested in.

                \end{block}

                \vspace{1cm}

                \begin{block}{Some technical details}

                    \begin{itemize}
                    \item Java + Scala source code
                    \item \textbf{Statika}-based module system
                    \item \textbf{SBT} for building sources and automated tests \& release
                    \item \textbf{Git + Github}: versioning, docs, collaboration, coordination
                    \end{itemize}

                \end{block}

                \vspace{1cm}

                \begin{alertblock}{Acknowledgments}

                    Bio4j is developed by the R\&D team of the Era7 Bioinformatics company\\

                    \vspace{1cm}

                    \begin{center}
                        \includegraphics[width=0.7\linewidth]{resources/logos/era7-logo.png}\\
                        \vspace{1cm}
                        \includegraphics[width=0.7\linewidth]{resources/logos/ohnoseq-logo.png}\\
                    \end{center}

                    This project is funded in part by the ITN FP7 project INTERCROSSING (Grant 289974)\\

                    \begin{center}
                        \begin{tabular}{m{0.4\linewidth} m{0.4\linewidth}}
                            \includegraphics[width=\linewidth]{resources/logos/intercrossing-logo.png} & \includegraphics[width=\linewidth]{resources/logos/marie-curie-logo.png}
                        \end{tabular}
                    \end{center}

                \end{alertblock}

            \end{column}

        \end{columns}

    \end{column}

    \begin{column}{\sepwid}\end{column}

\end{columns}
