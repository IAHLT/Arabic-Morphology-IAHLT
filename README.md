# Arabic lemmatisation -- IAHLT

האיגוד הישראלי לטכנולוגיות שפת אנוש
الرابطة الإسرائيلية لتكنولوجيا اللغة البشرية
The Israeli Association of Human Language Technologies
https://www.iahlt.org

A corpus of Modern Standard Arabic as used in Israel annotated for
part-of-speech and lemma.

## Data set

The IAHLT Arabic lemmatisation and part-of-speech corpus is a work in
progress. The dataset consists of 2013 annotations of 1357 sentences
(with a total of 52846 tokens annotated, 5524 unique lemmas) for lemma
and part-of-speech, taken from news reporting. It is released under the
CC-BY-NC-SA-4.0 license, see COPYING for details.

The annotations are stored in the popular CoNLL-U format; columns 5-9
(dependency-related) are null.

Note that although the `sentnumber` values are not necessarily consecutive, the
sentences are in fact sorted according to the original order.

## Introduction

The IAHLT Arabic corpus consists of news reporting texts.

Sentences were first segmented, tokenised, and annotated for lemma and
part-of-speech by the Stanza Arabic model; annotators then reviewed and
corrected the annotations.

Some sentences have been annotated multiple times to validate our
guidelines and schema. Included are 656 sentences which have been
independently annotated by two different annotators.

Part-of-speech frequencies:

  |  POS  | Freq  |
  | ----- | ----  |
  | NOUN  | 14405 |
  | DET   | 10134 |
  | ADP   |  6655 |
  | PUNCT |  4310 |
  | ADJ   |  4278 |
  | VERB  |  2888 |
  | CCONJ |  2821 |
  | PRON  |  2036 |
  | PROPN |  1473 |
  | SCONJ |  1179 |
  | NUM   |   747 |
  | PART  |   638 |
  | X     |   621 |
  | ADV   |   475 |
  | AUX   |   172 |
  | _     |    92 |
  | SYM   |    72 |
  | INTJ  |     6 |


# Inter-annotator analysis

The 656 doubly-annotated sentences were analyzed using Cohen's kappa, producing
the following statistics:

- avg total tokens: 17462
- comparable tokens: 15121

Overall agreement:

  |             | Agreement |
  | ----------- | --------- |
  | token       | 0.99      |
  | lemma       | 0.894318  |
  | upos        | 0.958029  |
  | misc        | 0.987517  |

Per-feature agreement:

  |             | Agreement |
  | ----------- | --------- |
  | Typo        | 0.44365   |

## Metadata fields

- fields for technical use:

  - `sent_id`    - a unique identifier for the annotation within this release
  - `text`       - the text of the original sentence
  - `url`        - the link for the source entry/article
  - `source`     - the source of the sentence
  - `doc_id`     - a unique identifier for the source document
  - `parnumber`  - the paragraph sequence number within the source document
  - `sentnumber` - the sentence sequence number within the source paragraph

## Acknowledgments

We would like to thank all the people who contributed to this corpus:

Amir Ejmail
Amjad Aliat
Assia Adam
Mutaz Ayesh
Nick Howell
Noam Ordan
Sawsan Thabit
Yifat Ben Moshe

