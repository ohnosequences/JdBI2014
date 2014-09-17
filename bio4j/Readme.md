## Bio4j: the bioinformatics data platform

### _Pablo Pareja-Tobes, Alexey Alekhin, Evdokim Kovach, Marina Manrique, Eduardo Pareja, Raquel Tobes and Eduardo Pareja-Tobes_

Bio4j (http://bio4j.com) is a cloud-based high-performance bioinformatics graph database. It is one of the first and most important graph databases for biological data with a special focus on data integration: it integrates most data available in UniProt KB (SwissProt + Trembl), Gene Ontology (GO), UniRef (50, 90, 100), RefSeq, NCBI taxonomy, and Expasy Enzyme DBs. All this data in Bio4j is organized in a semantically equivalent graph structure. It allows having many different types of nodes and relationships, making it perfect for highly interconnected complex biological data. Graph databases allow fast local access to all the elements related with each entity, through the edges that connect them with others. So, from a performance point of view, queries which would even be impossible to perform with a standard relational database take no more than a couple of seconds with Bio4j.

Bio4j is in active development and grows rapidly: it includes now 1,216,993,547 relationships and 190,625,351 nodes, which is close to triplicating the figures from one year ago. A flexible module system based on Statika is provided with Bio4j enabling the user to build and deploy only the modules needed for the analysis. 

Bio4j is now based on an abstract domain model which decoupling the inner database implementation from the relationships among entities themselves. This allowed us to have a default implementation using Blueprints, the de-facto standard for graph data modeling, thus making the domain model independent from the choice of database technology. Building on that, we now offer binary distributions for Neo4j and TitanDB backends, yielding a dramatic increase of performance using the backend-specific optimizations, such as vertex-local edge-typed indexes in TitanDB for instance. 

Bio4j is open source, available under the AGPLv3 license. 

This project is funded in part by the ITN FP7 project INTERCROSSING (Grant 289974).
