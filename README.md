# BigBasket-Product-Catalog-Analysis-using-Looker-Studio
# BigBasket Product Catalog Analysis Dashboard


## Interactive Dashboard

You can view the live, interactive Looker Studio dashboard here:
**View Live Dashboard :** (https://lookerstudio.google.com/reporting/6bdb68f8-6444-4f1a-a32e-38e98a0280c2)

### Dashboard Pages:
- **Page 1: Overview** (High-level KPIs and category distribution)
- **Page 2: Product Pricing & Quantity** (Detailed pricing, discounts, hierarchy)
- **Page 3: Price Insights** (In-depth price and discount analysis)

## Project Overview

This repository features an interactive data analytics dashboard developed using **Google Looker Studio**. The project undertakes a comprehensive analysis of the **BigBasket Product Catalog**, aiming to transform raw data into actionable intelligence. The dashboard provides in-depth insights into product distribution, pricing strategies, discount effectiveness, and customer perception (through ratings) across various categories, sub-categories, brands, and product types.

## Visualizations & Insights 

The dashboard is intuitively structured into three distinct pages, each delivering targeted insights for strategic decision-making.

### **Page 1: Overview**

This page serves as a high-level summary, providing immediate Key Performance Indicators (KPIs) and a broad understanding of the overall product catalog's scale and composition.

#### 1. KPI Scorecards 
* **Visualisation:** Prominent single-number displays highlighting key aggregate metrics.
* **Insights:**
    * The BigBasket product catalog comprises a substantial **24K unique products**, indicating a vast and diverse selection available to customers, reinforcing BigBasket's strong market presence.
    * An **Average Product Rating of 3.99** out of 5 across all products suggests generally positive customer satisfaction, indicating that products are well-received and meet customer expectations.
    * An **Average Discount Percentage of 11.82%** across the catalog demonstrates that BigBasket consistently employs promotional pricing. This strategy likely contributes to driving sales volume, maintaining competitive pricing, or managing inventory effectively.

#### 2. Product Count by Main Category
* **Visualisation:** A vertical bar chart illustrating the distribution of product count across the major main categories.
* **Insights:**
    * BigBasket's most extensive product offerings and deepest inventory concentrations are evident in **'Beauty & Hygiene' with 6,839 products**, followed by **'Gourmet & World Food' with 4,109 products**, and **'Kitchen, Garden & Pets' with 3,186 products**. These categories represent significant inventory depth and are likely core strategic focuses.
    * Conversely, categories such as **'Fruits & Vegetables' (358 products)** and **'Baby Care' (549 products)** show notably lower product counts, potentially indicating opportunities for expansion or a more curated selection in these areas.

#### 3. Product Distribution by Category
* **Visualisation:** A donut chart illustrating the proportional distribution of products within `category` groupings, emphasizing their percentage share of the total catalog.
* **Insights:**
    * The largest proportional share of the catalog is dedicated to **'Beauty & Hygiene' at 28.8%**, indicating a substantial focus and variety in this segment.
    * **'Gourmet & World Food' (17.3%)** and **'Kitchen, Garden & Pets' (13.4%)** also represent significant portions, highlighting BigBasket's diversified offerings beyond traditional groceries.

#### 4. Filter Controls
* **Visualisation:** Interactive elements including dropdown lists (`category`, `brand`) and a slider (`rating`).
* **Insights:**
    * These controls empower users to conduct dynamic data exploration. A user can select a specific `category` (e.g., 'Beauty & Hygiene'), a `brand` (e.g., 'Himalaya'), and filter by `rating` (e.g., between 4 and 5 stars) to update all visualizations across the entire report instantly. This capability streamlines specific query resolution.
---

### **Page 2: Product Pricing & Quantity**

This page offers a more granular look into individual product attributes, pricing dynamics, and hierarchical product organization, delivering deeper operational insights.

#### 1. Product Pricing & Quantity
* **Visualisation:** A detailed table presenting specific information for individual products, including calculated discount metrics.
* **Insights:**
    * This table allows for a precise, item-by-item examination of pricing and discounts. For example, `Zour Bomb` and `Zoroy` are currently listed at their full market price with **0 discount**, indicating no active promotions for these specific items at the time of data capture.
    * This direct comparison of `market_price` vs. `sale_price` alongside calculated discounts is crucial for understanding the exact value proposition for each product and identifying instances of zero or deep discounting.

#### 2. Price vs. Discount Analysis by Category
* **Visualisation:** A scatter plot with `market_price` on the X-axis and `Calculated Discount Percentage` on the Y-axis. Each point represents a product, colored by `category`.
* **Insights:**
    * The scatter plot reveals that BigBasket's discounting strategy spans its entire market price spectrum. While lower-priced items form a dense cluster with diverse discounts, there are instances where products, even in the **₹500-₹1000 price range**, receive substantial discounts (**up to 60-70%**). This suggests targeted promotional pushes not solely confined to clearing low-value inventory.
    * Outlier points immediately highlight unique price-discount combinations. For example, products with very high market prices (e.g., **₹5,000+**) but minimal discounts (**<10%**) likely represent premium or non-promotional items. Conversely, a product priced around **₹1000 with a 60% discount** would be an interesting case for further investigation into its specific promotional rationale.

#### 3. Product Distribution by Category Hierarchy
* **Visualisation:** A treemap utilizing nested rectangles to represent the hierarchical structure of product categories, with the size of each rectangle indicating the `Record Count` (product volume).
* **Insights:**
    * The treemap intuitively visualizes the precise concentration of product volume within the catalog's hierarchical structure. It confirms `Beauty & Hygiene` and `Gourmet & World Food` as leading top-level categories by product count.
    * Within `Kitchen, Garden & Pets`, sub-categories like `Storage & Accessories` and `Cookware` contribute significantly to product volume, highlighting depth in household items. Similarly, `Chocolates & Candies` and `Biscuits & Cookies` are substantial sub-segments within `Snacks & Branded Foods`, indicating a wide variety in these popular categories.

#### 4. Average Rating by Category & Brand
* **Visualisation:** A pivot table summarizing `Average Rating` at the intersection of `category` (rows) and `brand` (columns).
* **Insights:**
    * This table allows for precise performance comparison across categories. `Foodgrains, Oil & Masala` shows the highest average rating at **4.07**, followed by `Gourmet & World Food` and `Baby Care` both at **4.04**. This indicates strong customer satisfaction in essential and specialized food categories.
    * Conversely, `Kitchen, Garden & Pets` has the lowest average rating at **3.84**, suggesting potential areas for product quality review or customer experience improvement in this category.
    * The overall average rating for all products is **3.99**, consistent with the KPI on the overview page.

---

### **Page 3: Price Insights**

This page is specifically dedicated to in-depth analysis of product pricing and discounting strategies across various granular dimensions, providing actionable financial insights.

#### 1. List of Discounted Products
* **Visualisation:** A table displaying a concise list of products, sorted by their `discount_percentage` in descending order.
* **Insights:**
    * This table provides an immediately actionable list for marketing and sales teams, highlighting products with the most aggressive discounts. The **'Fruit & Vegetables Hand Juicer'** stands out with an exceptionally high **82.51% discount**, suggesting a strong promotional push, potentially for rapid inventory clearance or as a loss leader.
    * Multiple `Kitchen, Garden & Pets` items, such as `Small Silicone Spatula` (**81.2% discount**) and `Decorative Party Light` (**80.98% discount**), also feature prominently, indicating widespread promotions in this category.

#### 2. Average Market Price by Product Type
* **Visualisation:** A vertical bar chart comparing the average `market_price` for different granular `product types`.
* **Insights:**
    * The chart clearly illustrates significant price differentiation across product types. `Gas Stove` products, averaging around **₹8,300**, represent a distinct high-value segment, while `Cloth Dryer` items (approx. **₹3,100**) also occupy a higher price tier. This insight is crucial for understanding the typical price points and value proposition within specific product classifications.
    * Conversely, `Others` category products have a significantly lower average market price of around **₹339.7**, showcasing a diverse catalog that caters to various customer budgets and product needs.

#### 3. Average Discount Percentage by Sub-Category
* **Visualisation:** A horizontal bar chart illustrating the average `discount_percentage` for various `sub_categories`.
* **Insights:**
    * This visualization precisely highlights `Bakeware` with the highest average discount at **38%**, closely followed by `Steel Utensils` at **33.3%** and `Storage` at **29.1%**. This pattern strongly suggests that these sub-categories are either highly competitive areas, subject to frequent promotional activities, or strategic targets for inventory clearance.
    * Conversely, `Others` sub-categories exhibit a notably lower average discount of **10.5%**, indicating less aggressive promotional strategies in these segments. This insight is valuable for fine-tuning promotional strategies and managing profit margins per sub-category.

#### 4. Top 10 Brands by Average Market Price
* **Visualisation:** A vertical bar chart showcasing the top 10 brands based on their `Average market_price`.
* **Insights:**
    * The chart clearly identifies `Farmina` (approx. **₹10.1K** average market price) and `Carolina He...` (approx. **₹7.4K**) as the brands commanding the highest average market prices in the catalog. This positions them as premium brands, likely offering high-value or specialized products.
    * This insight is crucial for understanding the brand portfolio's strategic positioning. Brands like `Estee Laude` (approx. **₹5K**) and `Berggaer` (approx. **₹4.5K**) represent significant contributions to the higher-value segments, showcasing a diverse brand portfolio that caters to various price points.
---
