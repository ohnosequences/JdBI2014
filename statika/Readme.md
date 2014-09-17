## Statika: managing bioinformatics tools and resource in the cloud

### _Alexey Alekhin, Evdokim Kovach, Pablo Pareja-Tobes, Marina Manrique, Eduardo Pareja, Raquel Tobes and Eduardo Pareja-Tobes_

Next Generation Sequencing has revolutionized the bioinformatics landscape, reshaping fields such as genomics and transcriptomics, by offering huge amounts of data about previously inaccessible domains in a cheap and scalable way. Thus, biological data analysis demands, more than ever, high performance computing architectures. Cloud Computing, a comparable breakthrough in the IT world, holds promise for being the foundation on which a solution could be built (as already demonstrated by pioneering efforts such as Galaxy or CloudBioLinux). It provides a perfect framework for high throughput data analysis: deploying architectures with as much computing capacity as needed, scaling in a horizontal way, being also able to scale down adjusting to the computing needs real time, with the pay-as-you-go model.

However, fast and cost-effective data analysis in the cloud at such scale remains elusive. High throughput analysis, where a lot of resources are to be used and paid for, critically needs to have an ability to manage both the tools and data in a robust, reproducible and automated way. As in bioinformatics analysis often a pretty complex and unstable chain of dependencies underlies tools and data, knowing beforehand that all the resources to be used are properly configured is invaluable.

Statika (http://ohnosequences.com/statika) aims to be a basic tool for the declaration and automated deployment of composable cloud infrastructures for the bioinformatics space. Using Statika data, tools and infrastructure are treated on an equal basis with a expressive domain specific language that allows the user to express complex dependency relationships. Statika will automatically check for possible version conflicts and choose a safe resource creation order.

Statika has been applied in different scenarios: from a cloud-based system for scalable and composable parallel computations in the bioinformatics domain as in Nispero tool, to modular automated deployments of complex databases as Bio4j. Bio4j (bio4j.com)is a graph database integrating all data from key resources in the bioinformatics data space, including UniProt, Gene Ontology, the NCBI Taxonomy or UniRef. We use Statika internally for the integration and automated deployment of all sort of bioinformatics tools and data.

Statika is open source, available under the AGPLv3 license. 

This project is funded in part by the ITN FP7 project INTERCROSSING (Grant 289974).





