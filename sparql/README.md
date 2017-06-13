# SPARQL Endpoint User Guide
**Vanderbilt University Semantic Web Working Group**

## How can I interact with the endpoint?

There are two ways you can interact with our graph database using the W3C [SPARQL Query Language](https://www.w3.org/TR/sparql11-overview/).  If you are a human, you can use the GUI query form at [https://sparql.vanderbilt.edu](https://sparql.vanderbilt.edu/#query) to submit queries by typing or pasting them into a box.  If you are a machine, you can use HTTP GET to interact with the endpoint at https://sparql.vanderbilt.edu/sparql.  

For more details, see the [querying information page](querying.md).

## How can I know enough about the graphs in the triplestore to construct queries?

The pages linked below contain descriptions of graphs included in the database.  They also include some sample queries that can be used to explore those graphs.

| Project | Project URL | Status* | Description |
| ------- | ----------- | ------ | ----------- |
| [Bioimages](bioimages.md) | http://bioimages.vanderbilt.edu | stable | Image collection and biodiversity database |
| [Traditional Chinese Architecture Digital Research Tool](tcadrt.md) | http://tcadrt.org | testing | Tool for exploring the architecture of historical Chinese religious buildings|

\* Status descriptions:

Stable = graph model unlikely to change significantly; probably safe to use API calls in applications

Testing = graph model somewhat settled but subject to change; check for changes if your API calls stop Working

Experimental = graph model under construction; don't expect any sort of stability

## How does this work?

The graphs are modeled using the [World Wide Web Consortium](https://www.w3.org/) (W3C) [Resource Description Framework (RDF) Recommendation](https://www.w3.org/TR/rdf11-primer/). The graph database and SPARQL REST API are an implementation of the freely-available [Blazegraph](https://www.blazegraph.com/) application.  The web server is hosted on a Jelastic-based cloud service using an Nginx front end server to manage security and a Tomcat back end server to manage Blazegraph. This resource was developed by the [Vanderbilt University Semantic Web Working Group](https://heardlibrary.github.io/semantic-web/) supported by a grant from the [Vanderbilt Institute for Digital Learning](http://www.vanderbilt.edu/vidl/) (VIDL).  For more information, contact [Steve Baskauf](mailto:steve.baskauf@vanderbilt.edu).