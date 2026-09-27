## Unveiling the Android App Market (Google Play Store Analysis)

#### Overview
This project digs into the Google Play Store to answer a question most developers face before writing a line of code: where should a new app actually launch?

Using two real, messy datasets scraped from the Store, 10,841 app listings and 64,295 user reviews, I cleaned the data, looked at how crowded each category is, checked whether ratings, size, and price actually move the needle on installs, and ran independent sentiment analysis on the review text itself rather than relying on the dataset's pre-labelled sentiment.

#### Objective

To perform a comprehensive data analysis of the Google Play Store ecosystem by cleaning messy real-world data, exploring app category distribution, analysing ratings and pricing trends, and conducting sentiment analysis on user reviews in order to derive actionable, data-driven insights for a developer planning to launch a new app.

#### Steps Performed

1. **Data Loading** — Loaded the Play Store apps dataset (10,841 apps) and the user reviews dataset (~64,295 reviews) separately.
2. **Data Cleaning** — Fixed a corrupted record, converted `Installs`, `Price`, `Size`, and `Reviews` from messy text formats (e.g. `"10,000+"`, `"$4.99"`, `"19M"`) into proper numeric types, removed 1,181 duplicate app entries, dropped empty/duplicate reviews, and handled remaining nulls.
3. **Category Analysis** — Visualised app distribution across categories with a bar chart and identified the most/least saturated categories.
4. **Ratings Analysis** — Plotted the overall rating distribution and computed average rating by category.
5. **Size vs. Installs Analysis** — Built a scatter plot of app size against install count and calculated the correlation between them.
6. **Pricing Analysis** — Compared free vs. paid app distribution, plotted price distribution for paid apps, and estimated revenue by category.
7. **Sentiment Analysis** — Classified user reviews as Positive, Negative, or Neutral using VADER (rule-based sentiment analysis suited to short, informal text).
8. **Sentiment by Category** — Merged review sentiment with app categories to identify which categories have the happiest/unhappiest users.
9. **Interactive Visualisation** — Built an interactive Plotly bubble chart plotting category rating vs. sentiment vs. app count.
10. **Conclusion** — Summarised 3 data-driven insights for a developer planning a new app launch.

#### Tools Used

- **Python**
- **pandas**, **numpy** — data cleaning and analysis
- **matplotlib**, **seaborn** — static visualisations
- **plotly** — interactive visualisation
- **VADER** (`vaderSentiment`) — sentiment analysis
- **Jupyter Notebook** — development environment

#### Outcome
After cleaning the data, the analysis covered 9,659 unique apps across 33 categories and 29,692 usable user reviews.

The Family category was highly crowded, with almost one in five apps belonging to it. Game and Tools were also highly competitive.

Smaller categories such as Beauty, Events, Comics, and Parenting had fewer apps, which may give new developers more opportunities to stand out.

Most apps had ratings between 4.2 and 4.3 stars, showing that high ratings were common across the Play Store.

App size did not have a strong relationship with downloads. In simple terms, making an app smaller does not automatically mean that more people will download it.

Around 92% of apps were free, suggesting that users generally expect free access. A freemium or in-app-purchase model may be more suitable than charging users before download.

Family, Lifestyle, and Game apps showed the highest estimated revenue potential based on price and reported installs. This was only a comparison estimate, not actual revenue.

About 70% of analyzed reviews were positive, while approximately 20% were negative and the rest were neutral.

Social, Video Players, and News & Magazines had more negative feedback, suggesting that users in these categories may have higher expectations or more frequent complaints.

Comics and Auto & Vehicles had more positive user sentiment, indicating stronger user satisfaction in the available reviews.

#### Business Interpretation
A developer entering the Play Store should not choose a category only because it has many users. A better decision would consider three things:

- How crowded the category is.

- Whether users appear satisfied.

- Whether the category has realistic earning potential.

For example, launching a new app in Family, Game, or Tools may provide access to a large market, but these categories also have strong competition. A smaller category may be easier to enter, especially if it has positive user sentiment and an identifiable unmet need.

The analysis also suggests that app size should not be the main product decision. Developers may gain more value by focusing on useful features, user experience, app stability, marketing, and regular updates.

Because most apps are free, developers should carefully consider a freemium or in-app-purchase strategy instead of relying only on upfront pricing. Categories with more negative reviews may offer opportunities for improvement, but they would also require strong customer support and frequent bug fixes.

#### Limitations
The dataset is an older snapshot of the Google Play Store, so current market conditions may be different.

Install numbers were reported as ranges, such as 10,000+, rather than exact values.

Estimated revenue was calculated using price and installs, so it does not represent actual earnings.

Sentiment analysis was based on a rule-based tool and may not correctly understand sarcasm or informal language.

The results show patterns in the dataset but do not prove that one factor causes another.

Review sentiment was available for only some apps, so it may not represent the entire Play Store.

#### Author

**Zubia Ansari** — Data & BI Analyst 

[LinkedIn](https://www.linkedin.com/in/zubia-ansari01/) · [GitHub](https://github.com/ansarizubia)
