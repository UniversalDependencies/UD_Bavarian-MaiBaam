# Summary

MaiBaam is manually annotated with part-of-speech tag, syntactic dependencies, and German lemmas.
The treebank encompasses diverse text genres (wiki articles and discussions, grammar examples, fiction, and commands for virtual assistants) and dialects from the North, Central and South Bavarian areas as well as the dialectal transition areas in between.

# Introduction

Although Bavarian is closely related to Standard German, there are morphosyntactic differences, several of which are reflected in the UD annotations. We detail these differences in the documents linked below. As there is no standard orthography for Bavarian, the spelling reflects the phonetic variation between different Bavarian dialects, as well as idiosyncratic spelling-related differences.

We include sentence-level metadata:
- `genre`: One of *wiki* (Wikipedia articles), *social* (Wikipedia discussion pages), *fiction* (fairy tales), *grammar examples* (Tatoeba sentences, example sentences from Wikipedia pages about Bavarian grammar), *non-fiction* (queries for virtual assistants).
- `dialect_group`: One of *north, northcentral, central, southcentral, south* if we know the dialect group (where, e.g., *southcentral* is the transition area between the South Bavarian and Central Bavarian dialect regions), *unk* (unknown) if we do not have any information on the dialect group, and a code like *unk (southcentral/south)* if we can narrow down the options to, in this case, South Bavarian or the South/Central transition area.
- `location`: The city or municipality if known, else the state or province, else the country, else *unk* (unknown).
- `source`: For sentences from Wikipedia or Tatoeba, we include the source URL.
- `author`: The username of a Tatoeba sentence’s author, per [Tatoeba's usage conditions](https://tatoeba.org/en/terms_of_use#section-6).
- `text_en`: The original English sentence, for sentences translated from English (xsid, cairo).

The `sent_id`s indicate what source a sentence was taken from (see below).

The `MISC` column contains manually annotated German-language lemmas (`GermanLemma=...`). Unknown lemmas are annotated with `GermanLemma=<unknown>`.

# Acknowledgments

## Sources and licenses

We include sentences from the following sources, as indicated by different `sent_id` prefixes:
- [Bavarian Wikipedia](https://bar.wikipedia.org/), (`wiki`, `wikitalk`, `wikisource`, `wikisample`) shared under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
- [Tatoeba](https://tatoeba.org/en) (`tatoeba`), shared under [CC BY 2.0 FR](https://creativecommons.org/licenses/by/2.0/fr/), with usage conditions also detailed [here](https://tatoeba.org/en/terms_of_use#section-6).
- Translations of [xSID](https://github.com/mainlp/xsid) ([van der Goot et al. 2020](https://aclanthology.org/2021.naacl-main.197/), Winkler et al. 2024: "Slot and Intent Detection Resources for Bavarian and Lithuanian: Assessing Translations vs Natural Queries to Digital Assistants"), shared under [CC BY-SA 4.0 International](https://creativecommons.org/licenses/by-sa/4.0/). **NOTE:** We include different data splits: *xSID dev* for South Tyrolean sentences (`xsid_de-st_dev`), *xSID test* (!) for Central Bavarian sentences (`xsid_de-ba_test`).
- [Non-translated SID data](https://github.com/mainlp/NaLiBaSID), also from Winkler et al. 2024 (`sid_de-ba_natural`).
- A translation of the [Cairo CICLing Corpus](https://github.com/UniversalDependencies/cairo/) (`cairo`).

## References

The data collection and annotation, as well as initial ML experiments are described in the following paper, which also contains a data statement.
Please cite this paper when using the treebank:

- Verena Blaschke, Barbara Kovačić, Siyao Peng, Hinrich Schütze & Barbara Plank. 2024. *MaiBaam: A multi-dialectal Bavarian Universal Dependency treebank.* LREC-COLING 2024. ([pdf](https://aclanthology.org/2024.lrec-main.953/))

For detailed annotation guidelines, please read the following report:

- Verena Blaschke, Barbara Kovačić, Siyao Peng, Barbara Plank. 2024. *MaiBaam Annotation Guidelines.* Report, LMU Munich. ([pdf](https://arxiv.org/pdf/2403.05902.pdf))


# Changelog

* 2025-11-15 v2.17
  * Added Typo=Yes to goeswith
  * Constructions like "durch/duach des" and "fir des" are no longer fixed
  * Minor corrections
* 2024-11-15 v2.15
  * German lemmas added; minor corrections to dependency/POS annotations.
* 2024-05-15 v2.14
  * Initial release in Universal Dependencies.


<pre>
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.14
License: CC BY-SA 4.0
Includes text: yes
Parallel: cairo
Genre: wiki social fiction nonfiction grammar-examples
Lemmas: not available
UPOS: manual native
XPOS: not available
Features: not available
Relations: manual native
Contributors: Blaschke, Verena; Kovačić, Barbara; Peng, Siyao; Winkler, Miriam; Plank, Barbara
Contributing: here
Contact: verena.blaschke@cis.lmu.de
===============================================================================
</pre>
