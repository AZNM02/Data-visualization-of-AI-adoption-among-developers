# AI Adoption Among Developers: A Data Visualisation Study

An exploratory data analysis project examining the factors that influence developers' adoption of Artificial Intelligence in their workflows, using the 2024 Stack Overflow Annual Developer Survey.

---

## Research Question

> **"What are the factors influencing developers' adoption of Artificial Intelligence (AI) in their workflows?"**

---

## Dataset

All data is sourced publicly from the [TidyTuesday project](https://github.com/rfordatascience/tidytuesday/tree/master/data/2024/2024-09-03), which hosts the 2024 Stack Overflow Annual Developer Survey. Three files are loaded directly from URLs — no local data files are required to run this project.

| File | Description |
|------|-------------|
| `stackoverflow_survey_single_response.csv` | Main survey responses (17,734 rows) |
| `qname_levels_single_response_crosswalk.csv` | Label mappings for categorical variables |
| `stackoverflow_survey_questions.csv` | Survey question metadata |

---

## Analysis Structure

The project investigates three dimensions of AI adoption:

**1. Geographic Factors**
A treemap visualises AI adoption rates across continents, with tile size representing total respondent count and colour gradient representing adoption proportion. The Americas show the highest adoption rates, while regional disparities are noted alongside sample size caveats.

**2. Demographic Factors**
Four line charts examine how AI adoption varies across age groups, years of professional coding experience, education level, and annual compensation. A consistent pattern emerges: younger, less experienced, and lower-compensated developers show higher AI adoption rates, suggesting AI tools serve as productivity supplements rather than replacements for expertise.

**3. Psychological Factors**
Stacked bar charts compare sentiment distribution (Favorable / Neutral / Unfavorable) and threat perception (Threat / Non-Threat / Unsure) between developers who have and have not adopted AI. Favorable sentiment strongly correlates with adoption, while perceived threat to careers shows surprisingly little influence on adoption behaviour.

---

## Key Findings

- 83.6% of surveyed developers actively use AI tools in their workflows
- Despite high adoption, only 72% express a favorable sentiment toward AI
- AI adoption declines steadily with age, experience, education, and compensation — consistent across all four demographic dimensions
- Perceived threat of AI to careers does not meaningfully differentiate adopters from non-adopters; most developers in both groups view AI as non-threatening

---

## Technical Stack

| Tool | Purpose |
|------|---------|
| R / R Markdown | Core language and reproducible report format |
| tidyverse | Data manipulation and cleaning (dplyr, tidyr, readr) |
| ggplot2 | All visualisations |
| ggthemes | Clean plot themes |
| treemapify | Treemap visualisation for geographic analysis |
| patchwork / cowplot | Multi-panel plot composition |
| countrycode | Country-to-continent mapping |
| knitr | Table rendering and report knitting |

---

## How to Run

1. Clone the repository
2. Open `DSA2101_Project.Rmd` in RStudio
3. Install dependencies if needed:
   ```r
   install.packages(c("tidyverse", "ggthemes", "patchwork", "cowplot",
                      "countrycode", "treemapify", "knitr"))
   ```
4. Click **Knit** to render the full HTML report — data loads automatically from public URLs, no local files required

---

## Project Structure

```
├── DSA2101_Project.Rmd       # Source R Markdown file
├── DSA2101_Project.html      # Rendered HTML report (knitted output)
└── README.md
```

---

## Contributors

| Name | Contributions |
|------|--------------|
| Ryan Ng Jek Hian | Introduction, data transformation, summary statistics, line charts (age, coding experience) |
| Tee Jing Xin | Summary statistics, line charts (education level, compensation) |
| Aung Zar Ni Min | Data joining, stacked bar plots (sentiment & threat perception), discussion |
| Elias Liew Zhi Song | Treemap (geographic analysis) |
