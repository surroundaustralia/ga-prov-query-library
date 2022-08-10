# GA Provenance Query Library

This repository contains [SPARQL](https://www.w3.org/TR/sparql11-query/) queries for RDF data stored in GA's _Provenance Database_.

The _Provenance Database_ aggregates provenance data produced by workflows within GA that report their actions according to the [ProvWF profile of the PROV-O povenance data model](https://w3id.org/profile/provwf). These queries extract useful provenance from the databases total holdings where "useful" is determined through experience: what are commonly asked provenance queries? Of course, altered queries to these here can be asked of the provenance store in via its standard SPARQL query facility.


## Queries

The queries within this library are organised into themes and the individual queries are IDed alongside the question the aim to answer below:

* common element
    * [CE-E](common-element/CE-E.sparql) What workflows used a given data object?
    * [CE-A](common-element/CD-A.sparql) What workflows used common sub-workflow activities?
* influence
    * [I-E](influence/I-E.sparql) What data objects are dependent on a given data object?
    * [I-S](influence/I-S.sparql) What products are dependent on a particular version of software?
* status
    * [S-A](influence/S-A.sparql) What are the start & end times and success statuses of all workflows?
    * [S-P](influence/S-P.sparql) What are all the start & end times and success statuses of a particular workflow?
    * [S-AG](influence/S-AG.sparql) What workflows did a given Agent run?


## Query variants

Some of the queries in this library are presented in two main forms:

1. standard SPARQL
    * the files linked to above
2. Sankey diagram form

The first is just the basic SPARQL query using the PROV-O/ProvWF model to answer a common provenance query.

The second uses the same logic as the standard query but produces 'nodes' and 'edges' results for easy display of results via a [Sankey diagram](https://en.wikipedia.org/wiki/Sankey_diagram) which is a form of diagram often mentioned as being useful for provenance data exploration.

The queries are linked by identifier `CE-A` etc.


## Provenance Store

The provenance stored currently used for GA Provenance is a [Jena Fuseki instance hosted on AWS](http://digital-atlas-lb-1137864764.ap-southeast-2.elb.amazonaws.com:3200/#/).

## Contact
Developers:  

**Nicholas Car**  
*Data Systems Architect*  
SURROUND Australia Pty Ltd  
<nicholas.car@surroundaustralia.com>
<https://orcid.org/0000-0002-8742-7730>  

**David Habgood**  
*Application Architect*  
SURROUND Australia Pty. Ltd. 
<david.habgood@surroudaustralia.com>  
<https://orcid.org/0000-0002-3322-1868>
