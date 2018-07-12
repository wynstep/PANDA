# PANDA
PANDA, the Population Analysis Database

## Overview

PANDA (**P**opulation **An**alysis **Da**tabase) is the first manually-curated database which aims at capturing the expression profiles of selected markers in primary cells by integrating multiple layers of information in a user-friendly web portal. The curation process is conducted by experts that retrieve and interpret expression data from the literature.

PANDA mainly focuses the curation effort on the immune system and on the cell populations participating in skeletal muscle regeneration. The current release contains **79** different cell types in *H. sapiens*,*M. musculus*, *R. norvegicus* and *G. gallus* but aims at increasing the amount of curated data, extending curations to other tissues, organs and organisms.

## One portal, multiple layers of information

Since a well-defined and universally accepted standard is not yet available, informations are extracted, mapped and homogenised according to several leading database:

| Information | Database | Reference |
| ------------- |:-------------:| -----:|
| Protein names | [Uniprot](https://www.uniprot.org) | [Apweiler et al., 2004](https://www.ncbi.nlm.nih.gov/pubmed/14681372) |
| Tissues and Organs | [BRENDA](https://www.brenda-enzymes.org) | [Scheer et al., 2011](https://www.ncbi.nlm.nih.gov/pubmed/21062828) |
| Primary Cells | [Cell Line Ontology (CLO)](https://www.ebi.ac.uk/ols/ontologies/clo) | [Sarntivijai et al., 2014](https://jbiomedsem.biomedcentral.com/articles/10.1186/2041-1480-5-37) |
| Taxa IDs | [NCBI taxonomy](https://www.ncbi.nlm.nih.gov/taxonomy) | [Federhen, 2012](https://www.ncbi.nlm.nih.gov/pubmed/22139910) |

In PANDA, cells that are in a different state (i.e. quiescent, activated, proliferating) or belonging to several tissues or organisms are represented as distinct entities, because of differences in expression levels for specific markers.

## The curation process

PANDA can be considered the **first systematic effort** to capture relationships between primary cells and their markers expression profiles, integrating different layers of information, from several sources. 

The curation process starts with the selection of manuscripts reporting molecular characterization, mainly by flow cytometry experiments, of intracellular and surface proteins of functionally characterized and (relatively) homogeneous cell populations. The second phase is the actual “data interpretation”: sentences, expression values, flow cytometry, scatterplots and other types of information have to be critically reviewed for the categorization of marker profiles.

To this aim, a list of guidelines has been prepared to simplify the procedure. 
  * if a marker is reported to characterize a specific population or it has a key role in its cellular function, this is annotated as *“high / very high”* expression range;
  * if the marker is stated to be positive or negative in a specific cell lineage but this sentence is not supported by any experimental quantification approach, the curator evaluates this as *high, very high or low, absent*. 
  * When scatterplots or other quantitative data are available, the usual procedure to interpret flow-cytometry data [Herzenberg et al., 2006](https://www.ncbi.nlm.nih.gov/pubmed/16785881) is applied.

## PANDA file format

Curated cells can be browsed through the web resource or downloaded as a comma-separated (CSV) file. CSV file contains the annotation necessary to represent data in a consistent way and each entry is a unique string with the following format:

` cell,clid,marker,uniprot,tissue,tid,organism,taxid,min,max,min_label,max_label,PMID,curator`

| Field | Description | 
| ------------- |:-------------:|
| cell | Name of the cell, together with the status (quiescent, activated etc.) |
| clid | Cell Line Ontology ID -- it uniquely describes the cell |
| marker | Official Gene Name (HGNC) for the marker |
| uniprot | Uniprot Id for the marker |
| tissue | Tissue name (according to BRENDA nomenclature) |
| tid | BRENDA tissue ID |
| organism | Organism name |
| taxid | Taxon ID (according to NCBI) |
| min | minimum expression level for the marker (0-90) |
| max | maximum expression level for the marker (0-90) |
| min_label | category of expression for min level (*null,low,medium,high,very-high*)|
| max_label | category of expression for max level (*null,low,medium,high,very-high*)|
| PMID | List of PubMed articles that support the curation |
| curator | Name of the scientist(s) which performed the curation |

## How to contribute to PANDA project

We support **shared and social science**. 
PANDA is entirely open-source, this means the entire scientific community can contribute to its growth.

If you want to report errors, make suggestions or share your previous knowledge with us, you are very welcome! Feel free to [contact us](mailto:s.pirro@qmul.ac.uk)




