# Competitive Pokémon Analytics

![Competitive Pokémon Analytics Dashboard](visuals/pokemon_dashbord.png)

## Project Overview

Competitive Pokémon is a useful analytics problem because raw statistical strength does not automatically translate into competitive success. A Pokémon can have an impressive Base Stat Total (BST) and still see limited play, while another with lower overall stats can become a major part of the competitive metagame because of its typing, speed, abilities, role, or team utility.

I built this project to explore that relationship using Pokémon species data and 2024 VGC usage statistics. The analysis combines SQL, Power BI, and data visualization to compare statistical strength, typing, and actual competitive usage.

The central question behind the project is simple:

**What separates raw statistical strength from real competitive value?**

## Dashboard

![Competitive Pokémon Analytics Dashboard](visuals/pokemon_dashbord.png)

The Power BI dashboard brings the main analysis into one interactive view. Filters for primary type, generation, legendary status, and BST allow the dataset to be explored from different competitive perspectives rather than treating every Pokémon as part of a single population.

The report combines type distribution, average BST, competitive usage, and the relationship between BST and VGC representation so that statistical strength can be compared directly with actual metagame usage.

## Statistical Profile of the Dataset

### Pokémon Count by Primary Type

![Pokemon Count by Primary Type](visuals/type_count_chart.png)

Water and Normal are among the most common primary typings in the dataset, while Flying and Fairy appear considerably less often as a Pokémon's primary type. This provides useful context for later competitive comparisons because a type with more available Pokémon also has more opportunities to accumulate representation.

### Average Base Stat Total by Primary Type

![Average Base Stat Total by Primary Type](visuals/average_bst_by_type.png)

Dragon, Psychic, and Steel show some of the highest average Base Stat Totals, while types such as Bug and Normal rank lower overall. Comparing this result with type frequency shows that prevalence and raw statistical strength are not the same thing: some of the most common typings are not the strongest by average BST.

## Does Higher BST Lead to Higher Competitive Usage?

![BST vs Competitive VGC Usage 2024](visuals/bst_vs_vgc_usage_2024.png)

The 2024 VGC data shows a positive relationship between Base Stat Total and competitive usage, but the relationship is far from absolute. Higher stats can provide a stronger competitive foundation, but BST alone does not explain which Pokémon become heavily used.

Pokémon such as Flutter Mane illustrate the difference between total stats and how those stats are distributed and used. Typing, speed, offensive pressure, abilities, matchup value, and the ability to fill multiple roles can allow a Pokémon to outperform alternatives with greater raw statistical totals.

The dataset also contains **Eternamax Eternatus (BST 1125)**, an extreme statistical outlier. It was retained in the data for completeness but treated cautiously when interpreting the broader relationship between BST and competitive usage.

The main conclusion from this comparison is that **raw power matters, but competitive value depends on how effectively that power fits the metagame.**

## Which Types See the Most Competitive Play?

![Competitive VGC Usage by Primary Type](visuals/sum_of_usage_by_type_2024.png)

The 2024 usage data shows substantial differences in representation across primary typings. Grass, Fighting, Psychic, Ghost, and Fire account for some of the strongest cumulative usage in the dataset, while Bug, Poison, and Ice maintain considerably lower representation.

This does not mean that one typing is automatically superior to another. Competitive usage reflects the individual Pokémon available within each type as well as their abilities, secondary typings, matchups, team roles, and synergy with the rest of the format. However, the differences make it clear that typing is an important part of competitive viability and team construction.

## Key Findings

- **Higher BST is associated with stronger competitive usage, but it is not a reliable predictor by itself.**
- **Typing frequency does not necessarily correspond with statistical strength.** Water and Normal are common primary typings, while several less common types have higher average BST.
- **Competitive usage is concentrated among specific Pokémon and typings rather than being distributed according to raw stats alone.**
- **Stat distribution, typing, speed, abilities, role compression, and team utility help explain why some Pokémon outperform statistically stronger alternatives.**
- **Competitive value is multidimensional.** The strongest team-building choices are determined by how a Pokémon functions within the metagame, not simply by the total number of base-stat points it has.

## Analytical Approach

I approached the project in three stages. First, I established the overall structure of the dataset by analyzing Pokémon counts and average BST across primary typings. Next, I compared Base Stat Total with 2024 VGC usage to evaluate whether statistical strength translated into actual competitive representation. Finally, I analyzed cumulative usage by primary type to examine how typing appeared within the competitive metagame.

Power BI was used to combine these findings into an interactive dashboard, while SQL and data preparation workflows supported aggregation, cleaning, and analysis of the underlying data.

## Tools & Skills

**Power BI · SQL · Data Cleaning · Data Transformation · Exploratory Data Analysis · Data Visualization · Interactive Dashboard Design · Competitive Trend Analysis · Git · GitHub**

## Dataset

The project combines Pokémon species information with competitive VGC usage data. Fields used in the analysis include:

- Base stats and Base Stat Total
- Primary typing
- Generation
- Legendary status
- 2024 competitive VGC usage

The data was cleaned and transformed before analysis to make the statistical and competitive fields suitable for comparison and visualization.

## Limitations

Competitive usage cannot be explained by BST or primary typing alone. VGC performance is affected by factors that are not fully represented in this analysis, including abilities, movesets, secondary typing, items, team composition, format rules, matchup environments, tournament results, and changes to the metagame over time.

For that reason, the findings should be interpreted as an analysis of relationships within the available data rather than a model that predicts competitive success.

## Potential Extensions

Future versions of the analysis could incorporate tournament placement and win-rate data, compare multiple competitive formats or seasons, evaluate secondary typings and abilities, and use Python-based statistical modeling to measure the relative importance of different factors in competitive usage.

## Author

### Jesse Luffman

Data analytics professional and Bachelor of Information Technology student interested in using analytics to explore both practical business problems and complex systems where the most obvious metric does not tell the entire story.
