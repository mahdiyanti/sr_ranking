# sr_ranking
Trial to make ranking for Systematic Review

# Project Description: Screening & Ranking Scientific Articles
This repository contains Python scripts for automated relevance scoring and ranking of scientific articles based on keyword matching in abstracts. The workflow is designed to support literature screening in forestry, plant science, and epigenetics research.

# Key Features
## Keyword-based relevance scoring
Simple scoring: counts occurrences of target keywords in abstracts.

Advanced scoring: applies category-based weights (e.g., epigenetics, regulation, mechanism, plant type) and bonuses for multi-category matches.

## Data handling
Input: articles_479.csv containing article metadata (title, abstract, author, year, journal).

Output:
Ranked CSV files (sorted_screening_479.csv, sorted_screening_all.csv, sorted_screening_detailed_results.csv).
RIS files (sorted_screening_479.ris, sorted_screening_all.ris) for reference management software.

## Detailed results
Each record includes relevance score, matched keywords, matched categories, and applied bonuses.
Top-ranked articles are displayed in the console with keyword/category breakdowns.

# Workflow
1. Load article dataset (articles_479.csv).
2. Apply relevance scoring functions:
   calculate_relevance() --> basic keyword count.
   calculate_relevance_advanced() --> weighted scoring with category bonuses.
3. Sort articles by score.
4. Export results to CSV and RIS formats.
5. Print summary statistics and top-ranked articles.

# Example Console Output
- Total records loaded
- Number of relevant records (score > 0)
- Max and mean scores
- Top 15 most relevant articles with keyword/category matches

