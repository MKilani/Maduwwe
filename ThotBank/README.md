# ThotBank

Status: work-in-progress

Current release: 1.4, 09.04.2020

## How to cite

Kilani Marwan, 2020, Madùwwe Project - ThotBank dataset, https://github.com/MKilani/Maduwwe

## Authors

* **Marwan Kilani** - Swiss National Science Foundation (Mobility Grant) - Freie Universität Berlin (2019-2020)

## Others

This database is part of the output of the PostDoc project "Wandering Words: Sociolinguistics of Loanwords in Egypt and the Ancient Near East", sponsored by Swiss National Science Foundation (Mobility Grant - P400PG_186657 )

## Online version

Live version of the database: [ThotBank](http://maduwwe.herokuapp.com/ThotBank/)

## Description

ThotBank is a dataset of Coptic words for which an Egyptian etymology has been suggested. The datased provides the Coptic form in unicode, and automatically generated trascription, translation based on the [Coptic Online Dictionary](http://coptic-dictionary.org/about.cgi) project (COD), the suggested Egyptian etymology with references, a translation of the Egyptian form based on the [Thesaurus Linguae Aegyptiae](http://aaew.bbaw.de/tla/index.html) project (TLA), and additional related Coptic and Egyptian words.

Dialectal variants of the Coptic forms will be added soon.

The project is currently in developement, and new entries and new references are added regularly.

Each entry is interlinked, through ID numbers, to both the [Comprehensive Coptic Lexicon](http://coptic-dictionary.org/about.cgi) and the [Thesaurus Linguae Aegyptiae](http://aaew.bbaw.de/tla/index.html) databases.

### Structure of the database

The dataset is currently distributed as a .json with the following structure:

```json

      "EGY_ROOT__ID": int,
      "EGY_ROOT__TLA_ROOT": dict{},
      "EGY_ROOT-form": "string",
      "EGY_ROOT-meaning_en": "string",
      "TLA-forms": dict{},
      "CCL__forms": dict{},
      "MATCHES": dict{}

```

Each entry is identified by an ID ("EGY_ROOT-ID") and has the following main fields.

The "TLA-forms" contains references to the Egyptian and Demotic words recorded in the TLA that are related with basic root.

The "BBWA-forms" contains references to the Coptic words recorded in the BBWA database that are related with basic root according to the etymologies provided by various scholars.

The "MATCHES" contains etymologies sugegsted by various scholars connecting the basic root to Coptic words. Each entry in the "MATCHES" field correspond to one single grammatical form suggested by one scholar.

Finally note that the database is still in progress, so many fields already exist, but are still empty - they will be filled up in the future (e.g. the "EGY_ROOT-meaning_en" are all empty, as the prototypical meanign of the root will have to be reconstructed on the basis of the Egyptian attestations in the TLA and the Coptic attestations in the BBWA database).

Here a sample entry:


```json
{
    //...
    "118": {
      "EGY_ROOT-ID": 118,
      "EGY_ROOT-form": "gḏ",
      "EGY_ROOT-meaning_en": "",
      "TLA-forms": {
         "877949": {
            "TLA-ID": "877949",
            "TLA-form": "gḏ",
            "TLA-meaning_en": "",
            "TLA-meaning_de": "[Hand]"
         },
         "d6713": {
            "TLA-ID": "d6713",
            "TLA-form": "gjḏ(.t)",
            "TLA-meaning_en": "",
            "TLA-meaning_de": "Hand"
         },
         "168780": {
            "TLA-ID": "168780",
            "TLA-form": "gḏ",
            "TLA-meaning_en": "",
            "TLA-meaning_de": "Arme"
         }
      },
      "CCL-forms": {
         "C7995": {
            "CCL-ID": "C7995",
            "CCL-form": "ϭⲓϫ",
            "CCL-meaning_en": "hand; forefoot (of animals); handful (as measure); handwriting; handiwork, handicraft, activity",
            "CCL_MATCH-ID": [
               "250"
            ]
         },
         "C7999": {
            "CCL-ID": "C7999",
            "CCL-form": "ϭⲓϫ",
            "CCL-meaning_en": "by hand",
            "CCL_MATCH-ID": [
               "250"
            ]
         }
      },
      "MATCHES": {
         "250": {
            "MATCH-ID": "250",
            "MATCH-form": "",
            "MATCH-meaning_en": "",
            "MATCH-gram_number": "",
            "MATCH-gram_gender": "",
            "MATCH-pattern": "",
            "VYCICHL-1983": {
               "Degree_Certainty": "very_likely",
               "Relation_cpt-eg_forms": "same",
               "Root": "gḏ; gḏw; qḏ.t",
               "Reconstruction": "",
               "Gram_number": "",
               "Gram_gender": "",
               "Gram_form": "",
               "Meaning_fr": "main; pied de devant d'une bête",
               "Pages": "92",
               "Coptic": {
                  "S": "ϭⲓϫ",
                  "B": "",
                  "A": "",
                  "A2": "",
                  "P": "ⲕⲓϫ",
                  "F": "ϭⲓϭ, ϫⲓϫϩ",
                  "F0": "",
                  "S0": "",
                  "O": "",
                  "B0": "",
                  "A0": "",
                  "M": "ϭⲓϭ",
                  "L": "",
                  "G": "",
                  "B-Gr": "",
                  "Sf": "",
                  "H": "",
                  "A20": "",
                  "Hf": ""
               }
            }
         },
         "251": {
            "MATCH-ID": "251",
            "MATCH-form": "",
            "MATCH-meaning_en": "",
            "MATCH-gram_number": "pl",
            "MATCH-gram_gender": "",
            "MATCH-pattern": "",
            "VYCICHL-1983": {
               "Degree_Certainty": "very_likely",
               "Relation_cpt-eg_forms": "same",
               "Root": "gḏ; gḏw; qḏ.t",
               "Reconstruction": "*qiḏw-ū; *qiwḏ-ū",
               "Gram_number": "pl",
               "Gram_gender": "",
               "Gram_form": "",
               "Meaning_fr": "main; pied de devant d'une bête",
               "Pages": "92",
               "Coptic": {
                  "S": "",
                  "B": "",
                  "A": "",
                  "A2": "",
                  "P": "",
                  "F": "ϫⲉⲩϫ, ϫⲉⲟⲩϫ, ϫⲉⲟⲩϫϩ, ϫⲉⲟⲩϩϫ, ϫⲉϫⲟⲩϫϩ",
                  "F0": "",
                  "S0": "",
                  "O": "",
                  "B0": "",
                  "A0": "",
                  "M": "",
                  "L": "",
                  "G": "",
                  "B-Gr": "",
                  "Sf": "",
                  "H": "",
                  "A20": "",
                  "Hf": ""
               }
            }
         }
      }
   },
   //...
}
```



