[Source](http://ii.nlm.nih.gov/Web_API/index.shtml "Permalink to Indexing Initiative: Web API")

# Indexing Initiative: Web API

This Java-based API to the Indexing Initiative Scheduler facility was created to provide users with the ability to programmatically submit jobs to the **_Scheduler Batch_** and **_Interactive_** facilities instead of using the web-based interface.

Three programs are accessible via the Web API:  [MetaMap][1], the  [NLM Medical Text Indexer (MTI)][2], and  [SemRep][3]. The functionality in these programs includes: automatic indexing of MEDLINE citations, concept-based query expansion, analysis of complex Metathesaurus strings, accurate identification of the terminology and relationships in anatomical documents, and the extraction of chemical binding relations from biomedical text.

Whenever you see  ![Information Mark Symbol][4] in the text below, it means that additional information is available by selecting the symbol.

**_Contents:_**  

For specifics on the licensing and copyright information on each of these packages, please visit their respective link. Notices/Attributions will also be found in the source code when and where required.

The Web API has been designed to allow you to interact with our web-based  Scheduler using our Batch and Interactive facilities. Interactive access is currently only available for the MetaMap and SemRep programs.

There are six example programs included in the "examples" directory to illustrate how to incorporate the Web API into your application. Two of the examples (GenericBatch.java and GenericBatchNew.java) show how to access the Scheduler Batch facility. MMInteractive and SRInteractive.java examples show how to access Interactive MetaMap and Interactive SemRep respectively. The last two examples GenericBatchUser.java and MMInteractiveUser.java illustrate how to specify the username and password within the program to eliminate the need for prompting when running.

For a list of the available options, please select the appropriate program name: [MetaMap][5] and  [MTI][6].

| ----- |
| **GenericBatch.java** Example program for submitting a new Generic Batch with Validation job ("GenericObject(true)" turns on validation) request to the Scheduler to run. You will be prompted for your username and password and if they are alright, the job is submitted to the Scheduler and the results are returned in the String "results" below.

This example shows how to setup a basic Generic Batch with Validation job with a small file (sample.txt) with ASCII MEDLINE formatted citations as input data. You must set the Email_Address variable and use the UpLoad_File to specify the data to be processed. This example also shows the user setting the SilentEmail option which tells the Scheduler to NOT send email upon completing the job.

This example is set to run the MTI (Medical Text Indexer) program using the -opt1L_DCMS and -E options. You can also setup any environment variables that will be needed by the program by setting the Batch_Env field.

**NOTE:** The "-E" option/argument is very important and should be included with whatever program (MetaMap, SemRep, MTI) you decided to run! The reason is that this version of the Generic Batch does validation and the -E option tells the various programs to include a marker denoting when a successful result has been found.

 |
| &nbsp; |
| **GenericBatchNew.java** Same as GenericBatch.java above, except you can enter any of the options and the inputfile on the command line. The usage of the program and available options are listed below:

    usage: GenericBatchNew [options] inputFilename
      allowed options:
        --email <address> : set email address. (required option)
        --command <name> : batch command: metamap, semrep, etc. (default: MTI -opt1_DCMS -E)
        --note <notes> : batch notes
        --silent : don't send email after job completes.
        --silent-errors : Silent on Errors
        --singleLineInput : Single Line Delimited Input
        --singleLinePMID : Single Line Delimited Input w/ID
        --priority : request a Run Priority Level: 0, 1, or 2

**NOTE:** The "-E" option/argument is very important and should be included with whatever program you decided to run! The reason is that this version of the Generic Batch does validation and the -E option tells the various programs to include a marker denoting when a successful result has been found.  |
| &nbsp; |
| **MMInteractive.java** This example shows how to setup a basic Interactive MetaMap request. This runs the latest version of MetaMap with 1011 (2010AB) version of the UMLS Metathesaurus ("KSOURCE", "1011"), with "ignore_word_order" (-i) and "all_derivational_variants" (D) set as arguments to MetaMap. The default "Human Readable" output will be produced.

**NOTE:** The "-E" option/argument is _NOT_ required for Interactive use.

 |
| &nbsp; |
| **SRInteractive.java** This example shows how to setup a basic Interactive SemRep request. This runs the latest version of SemRep with Full Fielded Output (-D).

**NOTE:** The "-E" option/argument is _NOT_ required for Interactive use.

 |
| &nbsp; |
| **GenericBatchUser.java** This example is the same as "GenericBatchNew.java" above, except that the username and password are set in the program so that the user is not prompted when the program runs. **Please Note:** Although we understand the operational need for being able to specify the username and password within a program, you must also be aware of the security risks when using this setup. Please take care to secure the software you create using this option.  |
| &nbsp; |
| **MMInteractiveUser.java** This example is the same as "MMInteractive.java" above, except that the username and password are set in the program so that the user is not prompted when the program runs. **Please Note:** Although we understand the operational need for being able to specify the username and password within a program, you must also be aware of the security risks when using this setup. Please take care to secure the software you create using this option.  |

The following presentation describing the MetaMap/MTI Web API (Web API) was delivered as part of the April 10, 2012 NLM APIs webinar. For more information on other NLM APIs and/or to see the full recorded webinar, please visit the

page.

[1]: http://metamap.nlm.nih.gov "http://metamap.nlm.nih.gov"
[2]: ../MTI/index.shtml "../MTI/index.shtml"
[3]: http://semrep.nlm.nih.gov "http://semrep.nlm.nih.gov"
[4]: http://ii.nlm.nih.gov/images/quest.gif "Information Mark Symbol"
[5]: http://metamap.nlm.nih.gov/ "MetaMap Link"
[6]: ../MTI/NewMTIBatch_help_info.html "MTI Options Link"
  </notes></name></address>