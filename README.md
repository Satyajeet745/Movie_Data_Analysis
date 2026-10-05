# 🎬 Movie Dataset Analysis — Exploratory Data Analysis

An EDA project analyzing a dataset of **9,800+ movies**, exploring genre trends, popularity, audience voting patterns, and release trends over time — using Python, Pandas, Matplotlib, and Seaborn.

## 📌 Overview

This project explores a large movie dataset to answer questions like:

- Which genres are most common, and which get the most audience engagement?
- What are the most and least popular movies in the dataset?
- How has the number of movie releases changed over the years?
- How can movies be grouped into popularity tiers based on their average rating?

## 📊 Dataset

The dataset (`mymoviedb.csv`) originally contained **9,837 rows and 9 columns**, including release date, title, overview, popularity, vote count, vote average, language, genre, and poster URL.

After cleaning, the working dataset has **6 columns**:

| Column | Description |
|---|---|
| `Release_Date` | Year the movie was released |
| `Title` | Movie title |
| `Popularity` | Popularity score |
| `Vote_Count` | Number of audience votes |
| `Vote_Average` | Average rating, later binned into categories |
| `Genre` | Genre(s) of the movie |

**Cleaning steps applied:**
- Dropped irrelevant columns: `Overview`, `Poster_Url`, `Original_Language`
- Removed rows with missing values (9,837 → 9,826 rows)
- Converted `Release_Date` to just the release year
- Converted `Vote_Count` to integer and `Vote_Average` to float
- No duplicate rows found

## 🛠️ Tools & Libraries

- **Python 3**
- **Pandas** & **NumPy** – data loading, cleaning, aggregation
- **Matplotlib** & **Seaborn** – visualization


## 🔍 Analysis Performed

1. Initial data inspection (shape, dtypes, nulls, duplicates)
2. Data cleaning — dropping columns, handling nulls, fixing data types
3. Categorizing `Vote_Average` into 4 popularity tiers (not_popular, below_avg, average, popular)
4. Exploding the `Genre` column to analyze multi-genre movies individually
5. Genre distribution analysis
6. Genre-wise audience vote totals
7. Most and least popular individual movies
8. Movie release trends by year

## 💡 Key Insights

**1. Genre Distribution**
**Drama** is by far the most common genre (~3,750 movies), followed by **Comedy** (~3,020) and **Action** (~2,700). **Western**, **TV Movie**, and **Documentary** are the rarest, each under 250 movies.

**2. Audience Engagement by Genre**
**Drama** also leads in total audience votes (**5.14M**), followed by **Action** (4.87M) and **Adventure** (4.31M). Interestingly, **Documentary** films receive the fewest total votes (**38K**) — even fewer than the rarer **Western** genre (186K) — suggesting documentaries exist in decent numbers but get far less audience engagement per film.

**3. Most & Least Popular Movies**
**"Spider-Man: No Way Home"** has the highest popularity score in the dataset (**5,083.95**), spanning Action, Adventure, and Science Fiction. **"The United States vs. Billie Holiday"** has the lowest (**13.35**), under the Music genre.

**4. Movie Releases Over Time**
Releases grew slowly until the 1980s, then rose sharply from the 2000s onward, **peaking around 2020 with over 1,600 movies released** that year. A sharp drop-off in 2022–2023 likely reflects incomplete data collection for the most recent years, not an actual decline in movie output.

**5. Popularity Categorization**
Movies were grouped into 4 popularity tiers — **not_popular, below_avg, average, popular** — based on quartile cuts of `Vote_Average`, making it easier to compare movies across a consistent scale rather than raw ratings.

## 🚀 How to Run

```bash
git clone https://github.com/Satyajeet745/<your-repo-name>.git
cd <your-repo-name>
pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook Movie_data_Analysis.ipynb
```

## 📈 Sample Visuals

The notebook includes bar charts, a histogram, and a line graph for:
- Genre distribution
- Genre-wise vote totals
- Movie releases by year (histogram & line graph)


## 🙋‍♂️ Author

Made with 🎬 and Python by **Satyajeet**
GitHub: [Satyajeet745](https://github.com/Satyajeet745)


