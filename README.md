# Sephora Beauty Analytics Dashboard 💄

An end-to-end business intelligence project analyzing **8,216 products** and **1,094,411 customer reviews** from Sephora using Python and Power BI.

---

## 📊 Dashboard Preview

### Page 1 — Product Overview
![Product Overview](screenshots/Product_Overview.png)

### Page 2 — Customer Sentiment
![Customer Sentiment](screenshots/Customer_Sentiment.png)

### Page 3 — Market Gaps
![Market Gaps](screenshots/Market_Gaps.png)

### Page 4 — Skincare Deep Dive
![Skincare Deep Dive](screenshots/Skincare_Deep_Dive.png)

---

## 🗂️ Project Structure

```
sephora-beauty-analytics/
│
├── Sephora_Project.pbix        # Power BI dashboard file
├── sephora_cleaning.ipynb      # Python data cleaning notebook
├── screenshots/                # Dashboard page screenshots
└── README.md
```

---

## 🛠️ Tools Used

| Tool | Purpose |
|---|---|
| Python (Pandas) | Data cleaning and preprocessing |
| Google Colab | Development environment |
| Power BI Desktop | Dashboard and visualizations |
| DAX | Custom measures |

---

## 📁 Dataset

- **Source:** [Sephora Products and Reviews — Kaggle](https://www.kaggle.com/datasets/nadyinky/sephora-products-and-skincare-reviews)
- **Size:** 8,494 products + 1,094,411 reviews across 5 files
- **Columns used:** 15 product columns + 8 review columns after cleaning

---

## 🧹 Data Cleaning (Python)

**Product table:**
- Dropped 12 irrelevant columns (ingredients, variation details, child pricing)
- Removed 278 rows with null ratings (1% of data)
- Filled 8 null secondary_category values with "Unknown"
- Final shape: 8,216 rows × 15 columns

**Reviews table:**
- Combined 5 CSV files into one DataFrame (1,094,411 rows)
- Dropped high-null columns (helpfulness — 51% null)
- Filled null skin_type with "Unknown"
- Converted submission_time to datetime
- Final shape: 1,094,411 rows × 8 columns

---

## 📈 Dashboard Pages

### Page 1 — Product Overview
- KPI Cards: Total Products (8.2K), Avg Rating (4.19), Total Brands (302), High Rated Products (2K), Avg Price of High Rated Products ($55.53)
- Products by Category bar chart
- Top 10 Brands by Product Count
- Price Distribution histogram
- Category slicer

### Page 2 — Customer Sentiment
- KPI Cards: Avg Customer Rating (4.30), Recommendation Rate (84%)
- Rating Distribution column chart
- Reviews by Skin Type pie chart
- Rating by Skin Type column chart
- Skin type slicer

### Page 3 — Market Gaps
- Out of Stock by Category
- Online Only vs In-Store by Category
- Limited Edition Products by Category
- Category slicer

### Page 4 — Skincare Deep Dive
- Top 10 Skincare Brands by Rating
- Skincare Products by Subcategory
- Price vs Rating scatter plot
- Top 10 Most Loved Skincare Products
- Subcategory slicer

---

## 💡 Key Business Insights

1. **Skincare and Makeup dominate** — together 55%+ of Sephora's catalog
2. **84% recommendation rate** — extremely high customer satisfaction
3. **700K 5-star reviews out of 1M** — J-curve rating distribution typical in beauty retail
4. **Combination skin = 50% of reviewers** — largest target segment for skincare brands
5. **Makeup has the highest out-of-stock rate** — biggest restocking opportunity
6. **Price doesn't predict quality** — high rated products average only $55.53
7. **Lip Sleeping Mask = most loved skincare product** — ingredient-led products win
8. **Sephora Collection leads by volume** — private label dominance strategy

---

## 🔗 Connection to DermIQ

This project was built as a data validation layer for **DermIQ** — an AI-powered skincare ingredient analyzer. Key findings:
- Moisturizers and Treatments are most stocked → highest ingredient complexity → strongest use case for DermIQ
- Combination skin dominates reviews → DermIQ's personalization layer is most relevant here
- Ingredient-led products (Niacinamide, Hyaluronic Acid) top the most-loved list → users care about ingredients

---

## 👩‍💻 Author

**Nandini Ranjan Sinha**
- [LinkedIn](https://www.linkedin.com/in/nandiniranjansinha/)
- [GitHub](https://github.com/nandiniranjansinha)
- nandirsinha@gmail.com
