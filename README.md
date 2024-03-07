# Summary

MaiBaam is manually annotated with part-of-speech tags and syntactic dependencies.
The treebank encompasses diverse text genres (wiki articles and discussions, grammar examples, fiction, and commands for virtual assistants) and dialects from the North, Central and South Bavarian areas as well as the dialectal transition areas in between.

# Introduction

Although Bavarian is closely related to Standard German, there are morphosyntactic differences, several of which are reflected in the UD annotations. We detail these differences in the documents linked below. As there is no standard orthography for Bavarian, the spelling reflects the phonetic variation between different Bavarian dialects, as well as idiosyncratic spelling-related differences.

We include sentence-level metadata:
- `genre`: One of *wiki* (Wikipedia articles), *social* (Wikipedia discussion pages), *fiction* (fairy tales), *grammar examples* (Tatoeba sentences, example sentences from Wikipedia pages about
grammar), *non-fiction* (queries for virtual assistants).
- `dialect_group`: One of *north, northcentral, central, southcentral, south* if we know the dialect group (where, e.g., *southcentral* is the transition area between the South Bavarian and Central Bavarian dialect regions), *unk* (unknown) if we do not have any information on the dialect group, and something like *unk (southcentral/south)* if we can narrow down the options.
- `location`: The city or municipality if known, else the state or province, else the country, else *unk* (unknown). 
- `source`: For sentences from Wikipedia or Tatoeba, we include the source URL.
- `author`: The username of a Tatoeba sentence’s author, per [Tatoeba's usage conditions](https://tatoeba.org/en/terms_of_use#section-6).

The `sent_id`s also indicate what source a sentence was taken from.

# Acknowledgments

## Sources and licenses

We include sentences from the following sources, as indicated by different `sent_id` prefixes:
- [(Bavarian) Wikipedia](https://bar.wikipedia.org/) (`wiki`, `wikitalk`, `wikisource`, `wikisample`) shared under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)
- [Tatoeba](https://tatoeba.org/en), shared under [CC BY 2.0 FR](https://creativecommons.org/licenses/by/2.0/fr/), with usage conditions also detailed [here](https://tatoeba.org/en/terms_of_use#section-6)
- Translations of [xSID](https://bitbucket.org/robvanderg/xsid/src/master/) ([van der Goot et al. 2020](https://aclanthology.org/2021.naacl-main.197/), Winkler et al. 2024), shared under [CC BY-SA 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/). **NOTE:** We include different data splits: *xSID dev* for South Tyrolean sentences (`xsid_de-st_dev`), *xSID test* (!!!) for Central Bavarian sentences (`xsid_de-ba_test`).
- Non-translated SID data from Winkler et al. 2024 (`sid_de-ba_natural`), shared under [CC BY-SA 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/).
- A translation of the [Cairo CICLing Corpus](https://github.com/UniversalDependencies/cairo/) (`cairo`).

## References

The data collection and annotation, as well as initial ML experiments are described in the following paper, which also contains a data statement.
Please cite this paper when using the treebank:

- Verena Blaschke, Barbara Kovačić, Siyao Peng, Hinrich Schütze & Barbara Plank. 2024. *MaiBaam: A multi-dialectal Bavarian Universal Dependency treebank.* LREC-COLING 2024.

For detailed annotation guidelines, please read the following report:

- Verena Blaschke, Barbara Kovačić, Siyao Peng, Barbara Plank. 2024. *MaiBaam Annotation Guidelines.* Report, LMU Munich.

The paper and the report include the references we used for creating this dataset.


# Changelog

* 2024-05-15 v2.14
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.14
License: CC BY-SA 4.0
Includes text: yes
Genre: wiki social fiction nonfiction grammar-examples
Lemmas: not available
UPOS: manual native
XPOS: not available
Features: not available
Relations: manual native
Contributors: Blaschke, Verena; Kovačić, Barbara; Peng, Siyao; Plank, Barbara
Contributing: here
Contact: verena.blaschke@cis.lmu.de
===============================================================================
</pre>
