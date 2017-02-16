Mavenized Java API to the Semantic Knowledge Representation (SKR) Scheduler facility
====================================================================================

Quote from the original introduction of the Semantic Knowledge Representation (SKR) at http://ii.nlm.nih.gov/Web_API/index.shtml

> This Java-based API to the Indexing Initiative Scheduler facility was created to provide users with the ability to programmatically submit jobs to the Scheduler Batch and Interactive facilities instead of using the web-based interface. Three programs are accessible via the Web API: MetaMap, the NLM Medical Text Indexer (MTI), and SemRep. The functionality in these programs includes: automatic indexing of MEDLINE citations, concept-based query expansion, analysis of complex Metathesaurus strings, accurate identification of the terminology and relationships in anatomical documents, and the extraction of chemical binding relations from biomedical text.

This version uses [SKR_Web_API_V2_3](https://ii.nlm.nih.gov/Web_API/SKR_Web_API_V2_3.jar).

Additional change has made to fix the error "Returned: ERROR MESSAGE: Error - Text file empty", possibly due to a different HttpClient version. See [the commit](https://github.com/ziy/skr-webapi/commit/7530362f93662fbbd606078e83dc064dc25d2af1) for detail.

Use in a Maven project
-------------------------

Configure your pom.xml by adding this repository

```xml
<repository>
  <id>ziy-mvnrepo-releases</id>
  <name>ziy GitHub Personal Repo</name>
  <url>https://raw.github.com/ziy/mvn-releases/master/</url>
</repository>
```

and adding this dependency

```xml
<dependency>
  <groupId>edu.cmu.lti.oaqa.bio</groupId>
  <artifactId>skr-webapi</artifactId>
  <version>0.0.6</version>
</dependency>
```
