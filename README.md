# What Drives User Satisfaction with Productivity Applications?
### A Comparative Analysis of Apple App Store Reviews

## Overview
This project uses NLP and regression modeling to analyze 3,000 customer reviews across six leading productivity applications on the US Apple App Store (Notion, Microsoft OneNote, Evernote, Todoist, Microsoft To Do, and Structured) to determine which aspects of the user experience most strongly impact customer satisfaction.

### Research Questions
1. Which aspects of the user experience most strongly influence star ratings across leading productivity apps?
2. Do satisfaction drivers differ between Information Management tools (*Notion, Microsoft OneNote, Evernote*) and Task Management tools (*Todoist, Microsoft To Do, Structured*)?

## Key Findings

* **Asymmetry of Satisfaction**: Negative UX friction penalizes star ratings 1.6× to 4.9× more severely than positive features reward them. In the pooled OLS model, ratings are pulled down most strongly by Reliability (-1.14 stars), AI & Updates (-0.74 stars), Value & Pricing (-0.68 stars), and Functionality (-0.46 stars), while Organization (+0.29 stars) and Usability (+0.23 stars) are the primary positive drivers.
* **Category Divergence (Info vs. Task Management)**:
  * Information Management apps (*Notion, OneNote, Evernote*) are penalized most heavily by Value & Pricing (-0.93 stars vs. -0.46 in Task Management) and AI & Updates (-0.79 stars vs. -0.60), while interface Usability is not statistically significant (p = 0.124).
  * Task Management apps (*Todoist, Microsoft To Do, Structured*) are penalized the most by Reliability (-1.32 stars vs. -0.97 in Information Management) and are the only segment where everyday Usability significantly boosts ratings (+0.26 stars, p = 0.008).
* **App-Specific Pain Points**: Per-app TF-IDF predictors and sub-issue breakdowns show distinct friction mechanisms for each app: Evernote (2.74 stars) is dragged down by price hikes (29.6%, 1.89 stars) and free-tier paywalls/ads (25.4%, 1.54 stars); Notion (3.07 stars) by AI rollouts (24.6%, 2.36 stars) and iPad/platform bugs (21.6%, 2.04 stars); Microsoft To Do (3.02 stars) by iOS crashes (26.6%, 2.02 stars); and Microsoft OneNote (3.04 stars) by crashes (21.6%, 2.21 stars) and login friction (1.74 stars).

## Repository Structure
```text
productivity-app-consumer-research/
│
├── README.md                         # Project overview
├── productivity_app_analysis.ipynb   # Full Python notebook (data collection, NLP, OLS, visualizations, analysis)
├── requirements.txt                  # Python packages needed to run the notebook
│
└── data/
    └── app_reviews_cleaned.csv       # Cleaned snapshot of 3,000 Apple App Store reviews
```
