# r/HostileArchitecture — Reddit Community Analysis

An exploratory study of the Reddit community [r/HostileArchitecture](https://www.reddit.com/r/HostileArchitecture/), combining natural language processing, sentiment and emotion analysis, temporal trends and user-interaction networks to understand conversations around hostile urban design.

## Research questions

- What topics, places and organizations appear in the discussions?
- What sentiment and emotions characterize posts and comments?
- Which users are structurally central, and what interaction communities emerge?
- How do activity and expressed sentiment vary across the observed posts?

## Workflow

1. **Collection:** retrieve recent subreddit submissions and comments using Reddit's API through PRAW (the original analysis uses `new(limit=1000)`).
2. **Text processing:** cleaning, tokenization, stopword removal and lemmatization; named-entity recognition using spaCy.
3. **Content analysis:** sentiment with VADER, emotion analysis with NRCLex and keyword/co-occurrence analysis.
4. **Social network analysis:** directed user-reply graph, degree/betweenness centrality and community detection with NetworkX.
5. **Exploratory reporting:** activity trends, graphs and comparisons between content and interaction structure.


## Contents

- [`r_HostileArchitecture.ipynb`](r_HostileArchitecture.ipynb): original notebook **with all code and Markdown cells preserved**. Saved execution outputs have been removed for public sharing to avoid redistributing Reddit usernames and comment excerpts; this does not modify the source code. Consequently, charts need to be regenerated when running the notebook.
- [`requirements.txt`](requirements.txt): approximate dependencies inferred from the original imports, not a frozen or tested environment.

## Running the notebook

The notebook was originally developed in **Google Colab** and uses a specific Google Drive location for a `redditCredentials.json` file. To execute it you need:

1. A Google Colab environment with the packages in `requirements.txt` installed and the required language resources/models available.
2. Your **own** authorized Reddit API credentials, stored privately (never committed to GitHub).
3. Access to/configuration of the expected Google Drive path; the original notebook references `/content/drive/MyDrive/WSA/Exam_25/redditCredentials.json`.
4. To execute notebook cells in order. Fresh API data may differ from the data used for the original analyses.

## Authorship and contributions

This project was jointly developed by:

- **Chiara Bosi** — [@chiarabosi-aiml](https://github.com/chiarabosi-aiml)
- **Francesca Chite** — [@francescachite](https://github.com/francescachite)

Both authors collaborated throughout the project, contributing to its development, analysis, and documentation.

## Attribution and reuse

All Reddit data and posts remain attributable to their respective creators and are subject to Reddit's applicable terms. The dataset is not redistributed here. No software license is assigned to this coursework repository at present. This portfolio presentation preserves the original project and documents its constraints.
