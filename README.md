# MCWR: Morals and Cultural values from Writers and Readers

## Overview

Most datasets that annotate text for moral or cultural values record only what an
annotator inferred. They do not collect information on who wrote the text, who annotated it, or
whether the inference was accurate.

MCWR takes a different approach, using a two-step collection procedure:

**Step 1 — Writers.** 200 participants wrote short texts in response to prompts
designed to elicit value-laden content: personal experiences, interview-style
questions, arguments on controversial claims, and replies to online comments.
Each writer produced 10 texts and completed two standard value questionnaires, so
each text is paired with the writer's own value profile.

**Step 2 — Readers.** A separate set of ~500 participants read those texts and
inferred the writer's values, without any information about who wrote them. Each
reader rated 20 texts from different writers, and each text was rated by
approximately 5 readers. Readers completed the same value questionnaires about
themselves.

Every annotation therefore comes with three value profiles: the writer's actual
values, the reader's own values, and the reader's inference about the writer.
This supports questions, such as whether annotators project their own values onto strangers and under what conditions
their inferences diverge from the writer's self-report.

## Coverage

| Language | Annotations | Writers | Readers | Texts |
|---|---|---|---|---|
| English (US) | 2,097 | 50 | 138 | 493 |
| Spanish (Mexico) | 1,990 | 50 | 120 | 495 |
| Chinese | 2,094 | 50 | 120 | 495 |
| Arabic | 1,842 | 50 | 120 | 498 |
| **Total** | **8,023** | **200** | **498** | **1,981** |

## Value dimensions

Eleven dimensions from two frameworks.

**Moral Foundations (MFQ2):** Care, Equality, Proportionality, Authority,
Loyalty, Purity. Scored 1–5, where higher scores indicate that the foundation is
more important to the individual.

**Cultural Dimensions (CVSCALE):** Individualism–Collectivism, Power Distance,
Gender Egalitarianism, Uncertainty Avoidance, Long- vs. Short-Term Orientation.
Scored 1–5 as positions along a continuum between two orientations.

Demographics are available for both writers and readers: age, gender, ethnicity,
education, occupation, political leaning, and country of residence, along with
language-specific items (years lived in China for Chinese speakers; Arabic
variety and usage context for Arabic speakers).

## Example record

```json
{
  "text_id": "us_0421",
  "writer_id": "w_us_017",
  "reader_id": "r_us_083",
  "language": "US",
  "prompt_type": "experience",
  "prompt": "Share about a time you overcame a challenging situation. What was the situation and how did you overcome it? What did you learn from that experience?",
  "text": "This occurred when I struggled with an opiate addiction. I was addicted to heroin for years and struggled to live a normal life Nobody trusted me and I was financially, mentally, and spiritually unstable I lost a lot of friends and normalcy in my life I overcame it by going to rehab and exchanging that bad habit for better ones like my career and fitness",

  "writer_self_reported": {
    "care": 3.50, "equality": 2.83, "proportionality": 4.17,
    "authority": 3.00, "loyalty": 3.33, "purity": 2.17,
    "collectivism": 2.50, "power_distance": 1.60,
    "gender_egalitarianism": 4.00, "uncertainty_avoidance": 3.80,
    "long_term_orientation": 4.33
  },

  "reader_self_reported": {
    "care": 4.83, "equality": 3.17, "proportionality": 4.50,
    "authority": 2.67, "loyalty": 3.00, "purity": 4.50,
    "collectivism": 3.00, "power_distance": 1.40,
    "gender_egalitarianism": 4.50, "uncertainty_avoidance": 4.20,
    "long_term_orientation": 4.67
  },

  "reader_inferred": {
    "care": 4.00, "equality": 3.00, "proportionality": 4.00,
    "authority": 3.00, "loyalty": 3.50, "purity": 4.50,
    "collectivism": 3.50, "power_distance": 2.00,
    "gender_egalitarianism": 4.00, "uncertainty_avoidance": 3.67,
    "long_term_orientation": 4.50
  },

  "reader_demographics": {
    "age_group": "30-39", "gender": "non-male", "ethnicity": "White",
    "education": "College degree", "occupation": "Employed",
    "political": "Left"
  }
}
```

## Notes on the data

The reader questionnaire is a shortened version of the full instruments, since
administering 50 items per text was not feasible in a crowdsourcing setting. We
ran pilot studies and measured Cronbach's α for every dimension; reliability
figures are reported in the paper.

Purity and Proportionality show weaker internal consistency than the other
dimensions, particularly in Arabic. Low reliability for Purity is a known issue
in the literature rather than something specific to this collection.

Chinese and Arabic participants were recruited by language rather than by country
of residence, so these samples include people living abroad and are not directly
comparable to the US and Mexican samples.


## Access

The data is available for research purposes. Because it contains self-reported
values and demographic information from identifiable individuals, we share it on
request rather than as an open download.

To request access, contact **Neele Falk** at **[neele.falk@ims.uni-stuttgart.de]** with a short
description of the intended use. Please include your affiliation and a brief
outline of the planned analysis or system.

We ask that the data not be used to build tools that infer individuals' moral
beliefs from their writing without their knowledge. Profiling of this kind is
explicitly outside the intended use.

## Citation

```bibtex
@inproceedings{falk2026mcwr,
  title     = {Shaped by Values: Language Through the Lens of Culture and Morality},
  author    = {Falk, Neele and Jurgens, David and Lapesa, Gabriella},
  booktitle = {Proceedings of the 2026 Conference on Empirical Methods
               in Natural Language Processing},
  address   = {Budapest, Hungary},
  year      = {2026}
}
```