# DBpedia-entity-CAR
Dataset DBpediaV2-entity projected onto TREC CAR Y2 entities

# Description
This dataset is derived from the [DBpedia-entityV2](https://github.com/iai-group/DBpedia-Entity) dataset. 
The qrel files are projected onto the Wikipedia dump used in [TREC Complex Answer Retrieval v2.1](http://trec-car.cs.unh.edu/datareleases/), which is provided as allButBenchmark.cbor.

As the original dataset was based on DBpedia from 2015, but TREC CAR is using a dump from 2016, some entities have been deleted or renames. 
The projection used name matches in the fields Title and Redirect. This way the vast majority of entities could be aligned, albeit possibly under a different name/id.

The original dataset also provided baseline runs as a reference point for comparison. The same alignment and projection was applied to entries in the ranking. Rank entries to entities that were deleted, were removed from the ranking.

This projection (both runs and qrels) affected the quality metrics of the rankings, but the overall ranking of methods is preserved.


# Queries

Queries provided as TREC CAR title queries (CBOR). These are based on the "stopped_v2" version of the queries. Each query is represented as title of the stub. No headings are provided.

# Qrels

The qrels are projected to TREC CAR ids. Entities that are not present in the allButBenchmark v2.1 release are removed.

# Baseline Runs

Baseline runs (provided by the original dataset), are projected onto TREC CAR entity ids. Entities that are not alignable, are removed.


