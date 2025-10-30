## 📄 Project Summary — YouTube Dislikes Analysis
This is a personal project I started in the **Summer of 2025** and completed during the **Fall of 2025** to strengthen my skills in **data cleaning, visualization, and statistical analysis using R**. The project explores patterns in YouTube engagement—specifically, how likes, dislikes, and views relate to one another. I used the Kaggle “USvideos.csv” dataset, performed feature engineering, and built interactive visuals and summary statistics to uncover trends in user interaction and sentiment. The full HTML report provides a detailed walkthrough of my workflow, analysis, and insights. Also want to give thanks to my **STAT 630 class at California State University, East Bay** to help guide me in analytical practices as well as **Datacamp** for teaching me the foundations of R programming. 

### 🔗 [View Final Project in HTML](https://nmfisher716.github.io/R_youtube_project/Youtube_projectNF.html)

| Variable | Description |
|-----------|-------------|
| `bt_data$interaction` | Ratio of likes over views. If the interaction is closer to zero, it suggests the video received relatively few likes compared to its views. |
| `bt_data$likes_diff` | Difference between likes and dislikes. This indicates whether likes or dislikes outweigh each other. |
| `bt_data$dislike_ratio` | Proportion of dislikes per observation, calculated as dislikes divided by the total of likes and dislikes. |

### What to Look For
- **Part 1 — Data + Packages:** Source (Kaggle USvideos.csv) and initial structure check (40,949 rows, 16 columns).  
- **Part 2 — Cleaning Steps:** Duplicate removal, filtering out disabled ratings/comments, and creating key features:
  - `interaction` = likes / views  
  - `likes_diff` = likes − dislikes  
  - `dislike_ratio` = dislikes / (likes + dislikes)  
  Final analysis set: **6,354 rows** and **10 variables** (after cleaning and feature engineering).
- **Part 3 — Analyses:**
  1) **Low-Interaction Videos:** Table of examples where likes are very small relative to views—shows why “few likes” ≠ “disliked content.”  
  2) **Most Disliked Video (by likes_diff):** *“PSA from Chairman of the FCC Ajit Pai”* surfaces as the largest gap favoring dislikes.
- **Part 4 — Deeper Dive (By Year):** Groups videos into **2016 & before**, **2017**, **2018** and compares average dislike percentage:
  - 2016 & before: **10.95%**  
  - 2017: **7.09%**  
  - 2018: **6.31%**
- **Confidence Interval (Bootstrap, 20,000 reps):** For videos in **2017–2018**, the mean `dislike_ratio` is **0.0658**, with a **95% CI ~ [0.063, 0.068]**.

### Key Takeaways
- **“Low likes” does not automatically mean “disliked”**—dislikes data clarifies sentiment.  
- **Dislike proportion appears lower in 2017–2018 vs. earlier years.**  
- For 2017–2018, **typical dislike share per video is ~6–7%**.

### 🔗 [View Final Project in HTML](https://nmfisher716.github.io/R_youtube_project/Youtube_projectNF.html)
