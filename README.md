# HW2 Team 4 — Dataset Collection and Understanding

Computational Social Science 2026, National University of Kyiv-Mohyla Academy (NaUKMA).

**Authors:** Vereitinova Daria, Ivanova Sofia

## Overview

This repository contains the data collection and preprocessing work for Homework 2. The project focuses on Ukraine's information space during the full-scale war, combining data from Telegram and Reddit to analyze volunteer fundraising campaigns, donation requests, and user engagement patterns.

## Notebooks

| Notebook | Description |
|---|---|
| `H2_team4_Telegram.ipynb` | Collection and cleaning of posts from 17 Ukrainian Telegram channels (news, state/global, volunteer/charity, military, entertainment/culture) starting from February 24, 2022. Builds a unified `full_df` of ~536K messages (~804 MB), with a focus on fundraisers, donation requests, and engagement/algorithmic promotion patterns. |
| `H2_team4_Reddit.ipynb` | Parsing of a large Reddit archive (Academic Torrents, via BitTorrent) to extract posts from r/ukraine. Raw ingestion: ~349K rows / 764.78 MB across 127 columns; after feature pruning and noise filtering: ~333K records / 36 columns / 355.50 MB. Focuses on upvotes, comments, and awards as engagement signals around fundraising campaigns. |

## Data Sources

- **Telegram:** custom export/parsing pipeline for 17 channels, cleaned and standardized into a single DataFrame.
- **Reddit:** raw dumps from Academic Torrents, filtered to r/ukraine via a custom parser.
- **Google Drive** (processed datasets): [link](https://drive.google.com/drive/folders/1Xx9N9LRu3pQyb_wOfZtd6sseaUt5X0ys)

## Key Notes

- The Telegram corpus has significant volume imbalance between high-frequency news channels and lower-frequency brigade/charity accounts — cross-channel comparisons require careful weighting.
- The Reddit dataset is dominated (over 90%) by links, photos, and videos rather than text-only posts.

## Course

Prepared as part of the *Computational Social Science 2026* course for third-year Applied Mathematics students at NaUKMA.
