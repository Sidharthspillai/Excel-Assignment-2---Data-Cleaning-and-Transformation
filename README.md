# Assignment-2-Data-Cleaning-and-Transformation

## Assignment-2-Data-Cleaning-and-Transformation

* **Handling Missing Values:** Identified missing values in the **Price** and **Category** columns. Missing prices were filled using **category-wise average imputation with `AVERAGEIF`**. Missing categories were assigned based on the product type.
* **Price Imputation:** Filled missing prices for **Sony Headphones = $522.30 (Electronics), Coleman Camping Tent = $130.00 (Outdoor), and Ray-Ban Sunglasses = $75.71 (Fashion)** and highlighted the imputed values in yellow.
* **Category Imputation:** Assigned missing categories based on product type: **Backpack and Sneakers → Fashion; Coffee Maker and Fitness Tracker → Electronics**, and highlighted the corrected values in gold.
* **Correcting Inconsistent Data:** Corrected category spelling errors such as **"Electroni" → "Electronics"** and highlighted the correction in teal.
* **Product Name Formatting:** Standardized inconsistent product names into **Title Case** using `PROPER` and `TRIM` functions, such as **laptop → Laptop, smartphone → Smartphone, headphones → Headphones**.
* **Removing Duplicates:** Identified duplicate records by comparing the complete row and removed **3 exact duplicate rows**, leaving **31 data records** excluding the header.
* **Splitting Product ID:** Split the `Product ID` into **Manufacturing Date** and **Country Code**. Since the year was not provided in the Product ID, **2024 was assumed** as the manufacturing year.
* **Manufacturing Date:** Used `DATE`, `MATCH`, `MID`, and `LEFT` functions to create the Manufacturing Date from the Product ID.
* **Country Code:** Extracted the two-letter country code from the Product ID using the `RIGHT` function.
* **Merging Data:** Created a new **Product Brand** column by merging `Brand Name` and `Product Name` using the `CONCAT` function.
* **Number Formatting:** Formatted the **Price ($)** column as currency and the **Manufacturing Date** column in `DD-MM-YYYY` format.
* **Conditional Formatting:** Applied **Data Bars** to the Price column to visually compare relative price values.
* **Category Highlighting:** Created a custom conditional formatting rule to highlight every row where the **Category = "Electronics"**.
