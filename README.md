# coracle_data
Daily updated data for the shiny app [CORACLE (COVID-19 liteRAture CompiLEr)](https://datahub.shinyapps.io/CORACLE/) from the [LitCovid](https://www.ncbi.nlm.nih.gov/research/coronavirus/) and [PubMed](https://pubmed.ncbi.nlm.nih.gov/) databases. For any questions, please contact [Dr. Chuan-Xing Li](https://staff.ki.se/people/chuli) (chuan-xing.li@ki.se) at Karolinska Institutet, Sweden.

## Table of contents

* [File List](#file-list)
* [Data Description](#data-description)
* [Licence](#licence)

## File List

| FILE NAME              | DATA TYPE | DESCRIPTION                                                  |
| ---------------------- | --------- | ------------------------------------------------------------ |
| README.md              | markdown  | readme file of coracle_data folder                           |
| fdate.csv              | character | Updated date of coracle_data folder                          |
| pmid.info.extended.csv | matrix    | Literature information (please see details below)            |
| pmid.mesh.csv          | matrix    | Literature and MeSH relationships (please see details below) |
| pmid.pub.type.csv      | matrix    | Literature and publication types relationship (please see details below) |
| cnet.csv               | matrix    | Direct citation relationship (please see details below)      |
| relMeSH.csv            | matrix    | The number of shared publications between each pair of MeSH terms **with at least 3 shared publications** (please see details below) |
| relMeSHfull.csv        | matrix    | The number of shared publications between each pair of MeSH terms (please see details below) |
| relPMID.csv            | matrix    | The number of shared citations between each pair of literature **with at least 3 shared citations** (please see details below) |
| relPMIDfull.csv        | matrix    | The number of shared citations between each pair of literature (please see details below) |
| acelist20200506.csv    | matrix    | An example PMID list for **ACE/ACE2** related articles       |

## Data Description

### pmid.info.extended.csv

| ELEMENT  | DATA TYPE | DESCRIPTION                                          |
| -------- | --------- | ---------------------------------------------------- |
| pmid     | integer   | PubMed Identifier                                    |
| title    | character | Title of the literature                              |
| journal  | character | Journal name                                         |
| date     | date      | Date in PubMed database                              |
| LitCovid | logical   | Whether included in the LitCovid Database            |
| cited    | integer   | The number of the paper is cited by other literature |
| language | character | Language of literature                               |
| country  | character | Country info from PubMed database                    |

### *pmid.mesh.csv*

| ELEMENT | DATA TYPE | DESCRIPTION         |
| ------- | --------- | ------------------- |
| pmid    | integer   | PubMed Identifier   |
| value   | character | Annotated MeSH term |

### pmid.pub.type.csv

| ELEMENT | DATA TYPE | DESCRIPTION       |
| ------- | --------- | ----------------- |
| pmid    | integer   | PubMed Identifier |
| value   | character | Publication Types |

### *cnet.csv*

| ELEMENT | DATA TYPE | DESCRIPTION                    |
| ------- | --------- | ------------------------------ |
| source  | integer   | PubMed Identifier of citations |
| target  | integer   | PubMed Identifier              |

### *relMeSH.csv ANDrelMeSHfull.csv*

| ELEMENT | DATA TYPE | DESCRIPTION                                                  |
| ------- | --------- | ------------------------------------------------------------ |
| term1   | character | MeSH term                                                    |
| term2   | character | MeSH term                                                    |
| n       | integer   | The number of publications shared by both MeSH term1 and term2. |

### *relPMID.csv AND relPMIDfull.csv*

| ELEMENT | DATA TYPE | DESCRIPTION                                             |
| ------- | --------- | ------------------------------------------------------- |
| PMID1   | integer   | PubMed Identifier                                       |
| PMID2   | integer   | PubMed Identifier                                       |
| N       | integer   | The number of shared citations by both PMID1 and PMID2. |

### *acelist20200506.csv*

| ELEMENT | DATA TYPE | DESCRIPTION       |
| ------- | --------- | ----------------- |
| PMID    | integer   | PubMed Identifier |

## Licence
This dataset is Open Source Software, that is, non-proprietary and is issued under the GPL 2.0 licence. You are free to copy or modify it as you like as long as you do not use it as part of any proprietary software. If you make any changes we would be very interested to know about them so that we can include them into the main release.
