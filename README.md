Mavenized Java API to the Semantic Knowledge Representation (SKR) Scheduler facility
====================================================================================

Quote from the original introduction of the Semantic Knowledge Representation (SKR) at http://ii.nlm.nih.gov/Web_API/index.shtml

> This Java-based API to the Indexing Initiative Scheduler facility was created to provide users with the ability to programmatically submit jobs to the Scheduler Batch and Interactive facilities instead of using the web-based interface. Three programs are accessible via the Web API: MetaMap, the NLM Medical Text Indexer (MTI), and SemRep. The functionality in these programs includes: automatic indexing of MEDLINE citations, concept-based query expansion, analysis of complex Metathesaurus strings, accurate identification of the terminology and relationships in anatomical documents, and the extraction of chemical binding relations from biomedical text.


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
  <version>0.0.4</version>
</dependency>
```