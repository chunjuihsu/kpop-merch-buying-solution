# 🎤​ Kpop Merch Buying Solution

A Google Sheets-based solution to help Kpop merch buyers scale their businesses and improve customer satisfaction by optimizing product allocation and purchase decisions using probability and assignment logic.

---

## 📌 Table of Contents

- [📖 Background](#-background)
- [🚨 Business Problem](#-business-problem)
- [💡 The Solution](#-the-solution)
- [🚀 Getting Started](#-getting-started)
  - [Step 1: Create a Google Spreadsheet](#step-1-create-a-google-spreadsheet)
  - [Step 2: Open App Script](#step-2-open-app-script)
  - [Step 3 (Optional): Authorize the Script](#step-3-optional-authorize-the-script)
  - [Step 4: Copy the Script Code](#step-4-copy-the-script-code)
  - [Step 5: Initialize the Workspace](#step-5-initialize-the-workspace)
  - [Step 6: Add Possible Products](#step-6-add-possible-products)
  - [Step 7: Add Orders](#step-7-add-orders)
  - [Step 8: Add Purchased Products](#step-8-add-purchased-products)
  - [Step 9: Assign Products to Orders](#step-9-assign-products-to-orders)
  - [Step 10: Estimate Next Purchase Probability](#step-10-estimate-next-purchase-probability)
  - [Step 11: Add More Purchases (Optional)](#step-11-add-more-purchases-optional)
  - [Step 12: Re-run Assignments and Estimations](#step-12-re-run-assignments-and-estimations)
  - [Step 13: Reset Workspace](#step-13-reset-workspace)
- [📈 What's Next](#-whats-next)

## 📖 Background

Kpop's global rise has brought with it a surge in demand for exclusive, limited-edition merchandise. However, many of these items are only available in South Korea, giving rise to a new type of professions: the **Kpop merch buyer**.

These individuals help international fans get merch, acting as middlemen who purchase and ship products overseas. One major challenge they face is the **mystery box** nature of most merch — buyers don't know what they’re getting until after the purchase.

## 🚨 Business Problem

1. **Mystery Box Merch**: Items are sold randomly (e.g., photo cards of different group members).
2. **Uncertain Fulfillment**: Buyers allow customers to list multiple preferred items, but matching these efficiently is difficult.
3. **Inefficient Allocation**: Time-consuming manual assignment of products to orders.
4. **Cost Dilemma**: Whether or not to buy another mystery box is a gamble.

## 💡 The Solution

This tool offers two key features to solve the problems above:

- ✅ **One-click product assignment**: Match available products to customer preferences optimally.
- 📊 **Purchase probability estimation**: Estimate the probability that buying one more mystery box will improve total customer satisfaction.

---

## 🚀 Getting Started

### Step 1: Create a Google Spreadsheet

Create a new Google Sheet with your account.


### Step 2: Open App Script

From your Sheet: Click `Extensions` → `Apps Script`


### Step 3 (Optional): Authorize the Script

If you are prompted with "Authorization Required" when continuing any of the following steps, follow this guide to enable access:

[Fix "This app is blocked" error](https://web.archive.org/web/20230207010146/https://aimanfikri.com/2022/05/09/this-app-is-blocked-error-on-google-apps-script-solution/)

### Step 4: Copy the Script Code

1. Open `Code.gs` (or create a new file).
2. Paste the script code in `Code.gs` in this repository.

### Step 5: Initialize the Workspace

1. Refresh your sheet.
2. Go to the new menu: **`Kpop Merch Buying Solution`** → **`Initialize Workspace`**
3. Enter the number of picks (1–10) each customer can select.

This will create 6 sheets:

- `main`
- `orders`
- `products`
- `possible_products`
- `satisfaction_scoring_rules`
- `assignment_result`

### Step 6: Add Possible Products

In `possible_products`, list every potential merch outcome.

Example: apple, banana, orange, grapes, strawberry, water melon, pineapple

### Step 7: Add Orders

In the `orders` sheet, fill in your customer orders like so:

| id | first_pick | second_pick  | third_pick  |
|----|------------|--------------|-------------|
| 1  | apple      |              |             |
| 2  | apple      | water melon  | strawberry  |
| 3  | banana     | pineapple    |             |
| 4  | orange     | banana       | grapes      |
| 5  | grapes     | water melon  |             |

### Step 8: Add Purchased Products

In `products`, enter what items you actually received.

Example: apple, banana, water melon, orange, orange

### Step 9: Assign Products to Orders

1. Click the menu: **`Kpop Merch Buying Solution`** → **`Assign Products to Orders`**
2. Check the `assigned_product` column in the `orders` sheet for the results.

### Step 10: Check Satisfaction Score

1. Go to the `main` sheet.
2. You’ll see the **current satisfaction score** calculated based on how well the assignments match each customer’s priority picks.

This score is based on rules defined in the `satisfaction_scoring_rules` sheet.

Use this score to evaluate how effective your current purchase was.

### Step 11: Estimate Next Purchase Probability

1. Click: **`Kpop Merch Buying Solution`** → **`Estimate Probability Next Purchase Improves Score`**
2. Check the `main` sheet to see the probability (%) that the next mystery box is going to improve customer satisfaction.

### Step 12: Add More Purchases (Optional)

If you buy another mystery box, add the new item to `products`. 

### Step 13: Re-run Assignments and Estimations

Repeat [Step 9](#step-9-assign-products-to-orders) and [Step 10](#step-10-estimate-next-purchase-probability) to update the satisfaction score and probabilities.

If you are happy with the current satisfaction score and the probability of further improvement is low, you may decide to finish the process and start shipping to your customers.

### Step 14: Reset Workspace

- To start fresh, go to **`Kpop Merch Buying Solution`** → **`Clear Workspace`**
- To change the number of picks allowed per order, re-run **Initialize Workspace**.

---

## 📈 What's Next

There are two exciting directions I want to explore:

1. **Web UI Frontend**

Replace spreadsheet UI with a user-friendly web app.

2. **Optimal Purchase Recommendation**
  
Recommend the number of mystery boxes to buy based on cost-benefit analysis using probability theory and current orders.

---

Have suggestions or want to contribute? PRs and issues welcome!

