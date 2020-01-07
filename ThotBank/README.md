# ThotBank

Status: work-in-progress

Current release: 1.5, 07.01.2020

Estimated Completion Date: February 2020

Link: [ThotBank](ThotBank)

## How to cite

Kilani Marwan, 2020, Madùwwe Project - ThotBank dataset, https://github.com/MKilani/Maduwwe

## Authors

* **Marwan Kilani** - Swiss National Science Foundation (Mobility Grant) - Freie Universität Berlin (2019-2020)

## Others

This database is part of the output of the PostDoc project "Wandering Words: Sociolinguistics of Loanwords in Egypt and the Ancient Near East", sponsored by Swiss National Science Foundation (Mobility Grant - P400PG_186657 )

## Description

ThotBank is a dataset of Coptic words for which an Egyptian etymology has been suggested. The datased provides the Coptic form in unicode, and automatically generated trascription, translation based on the [Comprehensive Coptic Lexicon](http://coptic-dictionary.org/about.cgi) project (CCL), the suggested Egyptian etymology with references, a translation of the Egyptian form based on the [Thesaurus Linguae Aegyptiae](http://aaew.bbaw.de/tla/index.html) project (TLA), and additional related Coptic and Egyptian words.

Dialectal variants of the Coptic forms will be added soon.

The project is currently in developement, and new entries and new references are added regularly.

Each entry is interlinked, through ID numbers, to both the [Comprehensive Coptic Lexicon](http://coptic-dictionary.org/about.cgi) and the [Thesaurus Linguae Aegyptiae](http://aaew.bbaw.de/tla/index.html) databases.

### Structure of the database

The dataset is currently distributed as a .json with the following structure:

```json
{
	"ThotBank_ID": {
        "matches": [
            [
                {
                    "01_Vycichl_page": "page_nr, page_nr",
                    "02_Osing_page": "page_nr, page_nr",
                    "03_Černý_page": "page_nr, page_nr",
                    "04_Kilani": "agree/disagree (ref. if any)",
                    "10_match": [
                        {"CCL_ID_Coptic": [["Coptic_Unicode"], ["Automatic_Transliteration"], "CCL_transaltion"]},
                        {"TLA_ID_Egyptian": [["TLA_transliteration"], ["Kilani_transliteration"], "TLA_translation"]},
                        {"TLA_ID_Demotic": [["TLA_transliteration"], ["Kilani_transliteration"], "English_translation_of_TLA_translation_german | TLA_translation_german"]}
                    ]
                }
            ]
        ],
        "other_Coptic": {
            "CCL_ID_Coptic": [["Coptic_Unicode"], ["Automatic_Transliteration"], "CCL_transaltion"]
        },
        "other_Demotic": {
            "TLA_ID_Demotic": [["TLA_transliteration"], ["Kilani_transliteration"], "English_translation_of_TLA_translation_german | TLA_translation_german"]
        },
        "other_Egyptian": {
            "TLA_ID_Egyptian": [["TLA_transliteration"], ["Kilani_transliteration"], "TLA_translation"]
        }
    },
    ...
}
```

The dataset is provided in two variants: in the first some of the sublists have been converted into strings for the sake of readability, while in the in the second all lists and sublists are encoded as such.

Version 1 (ThotBank_1_5):

```json
{
	...
	"2455": {
        "matches": [
            [
                {
                    "01_Vycichl_page": "342",
                    "02_Osing_page": "46, 188",
                    "03_Černý_page": "332",
                    "04_Kilani": "agree (-)",
                    "10_match": [
                        "{'C7765': [['ϭⲛⲟⲛ'], ['kʲ.n.o.n'], 'be soft, smooth, weak']}",
                        "{'d6811': [['gnn'], ['gnn'], 'to be tender, to be mild; to be wet | zart sein, milde sein; feucht sein']}",
                        "{'167540': [['gnn'], ['gnn'], 'to be weak; to be soft'], '600572': [['gnn'], ['gnn'], 'to be weak; to be soft']}"
                    ]
                }
            ]
        ],
        "other_Coptic": {
            "C7766": "[['ϭⲛⲟⲛ'], ['kʲ.n.o.n'], 'softness']",
            "C7769": "[['ϭⲛⲟⲛ'], ['kʲ.n.o.n'], 'bend, bow']"
        },
        "other_Demotic": {
        },
        "other_Egyptian": {
            "167550": "[['gnn'], ['gnn'], 'weak one']",
            "167560": "[['gnn'], ['gnn'], 'soft part of a plant product (med.)']",
            "167570": "[['gnn'], ['gnn'], 'an aromatic plant']",
            "167580": "[['gnn'], ['gnn'], 'an edible plant (legume?)']",
            "167600": "[['gnn.t'], ['gnn.t'], 'weakness (?)']",
            "167610": "[['gnn.w'], ['gnn.w'], 'fat']",
            "856747": "[['gnn.w'], ['gnn.w'], 'weakness']"
        }
    },
    ...
}
```

Version 2 (ThotBank_1_5_one_line):

```json
{
	...
	"2455": {
        "matches": [
            [
                {
                    "01_Vycichl_page": "342",
                    "02_Osing_page": "46, 188",
                    "03_Černý_page": "332",
                    "04_Kilani": "agree (-)",
                    "10_match": [
                        {
                            "C7765": [
                                [
                                    "ϭⲛⲟⲛ"
                                ],
                                [
                                    "kʲ.n.o.n"
                                ],
                                "be soft, smooth, weak"
                            ]
                        },
                        {
                            "d6811": [
                                [
                                    "gnn"
                                ],
                                [
                                    "gnn"
                                ], 
                                "to be tender, to be mild; to be wet | zart sein, milde sein; feucht sein"
                            ]
                        },
                        {
                            "167540": [
                                [
                                    "gnn"
                                ],
                                [
                                    "gnn"
                                ],
                                "to be weak; to be soft"
                            ],
                            "600572": [
                                [
                                    "gnn"
                                ],
                                [
                                    "gnn"
                                ],
                                "to be weak; to be soft"
                            ]
                        }
                    ]
                }
            ]
        ],
        "other_Coptic": {
            "C7766": [
                [
                    "ϭⲛⲟⲛ"
                ],
                [
                    "kʲ.n.o.n"
                ],
                "softness"
            ],
            "C7769": [
                [
                    "ϭⲛⲟⲛ"
                ],
                [
                    "kʲ.n.o.n"
                ],
                "bend, bow"
            ]
        },
        "other_Demotic": {
        },
        "other_Egyptian": {
            "167550": [
                [
                    "gnn"
                ],
                [
                    "gnn"
                ],
                "weak one"
            ],
            "167560": [
                [
                    "gnn"
                ],
                [
                    "gnn"
                ],
                "soft part of a plant product (med.)"
            ],
            "167570": [
                [
                    "gnn"
                ],
                [
                    "gnn"
                ],
                "an aromatic plant"
            ],
            "167580": [
                [
                    "gnn"
                ],
                [
                    "gnn"
                ],
                "an edible plant (legume?)"
            ],
            "167600": [
                [
                    "gnn.t"
                ],
                [
                    "gnn.t"
                ],
                "weakness (?)"
            ],
            "167610": [
                [
                    "gnn.w"
                ],
                [
                    "gnn.w"
                ],
                "fat"
            ],
            "856747": [
                [
                    "gnn.w"
                ],
                [
                    "gnn.w"
                ],
                "weakness"
            ]
        }
    },
    ...
}
```