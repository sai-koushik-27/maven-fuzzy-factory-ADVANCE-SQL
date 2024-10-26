# E-Commerce Data Analysis for Maven Fuzzy Factory

## Project Overview
Maven Fuzzy Factory is an e-commerce startup specializing in stuffed animals. This project analyzes user behavior, traffic sources, and product performance using SQL. The goal is to provide actionable insights for business strategy and optimization.

## Tool Used
- **SQL Workbench**: Used to execute SQL queries and perform data analysis.

## Dataset Overview
The project utilizes a custom-built database with data on:
- Website Activity
- Products
- Orders


## Features of Each Table

### 1. **order_item_refunds**: Tracks refund information for items in orders.

| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| order_item_refund_id | Unique identifier for each refund record         |
| created_at          | Date when the refund was processed                |
| order_item_id       | Identifier linking to the specific item refunded  |
| order_id            | Identifier linking to the order with the refunded item |
| refund_amount_usd   | Amount refunded in USD                            |

---

### 2. **order_items**: Contains details of items purchased in each order.

| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| order_item_id       | Unique identifier for each item in an order       |
| created_at          | Date when the item was added to the order         |
| order_id            | Identifier linking to the parent order            |
| product_id          | Identifier linking to the product purchased       |
| is_primary_item     | Indicates if the item is the primary product (1 for primary, 0 for cross-sell) |
| price_usd           | Selling price of the item in USD                  |
| cogs_usd            | Cost of goods sold (COGS) for the item in USD     |

---

### 3. **orders**: Stores information about customer orders.

| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| order_id            | Unique identifier for each order                 |
| created_at          | Date and time when the order was placed           |
| website_session_id  | Identifier linking to the website session during the order |
| user_id             | Identifier for the user who placed the order      |
| primary_product_id  | ID of the main product purchased in the order     |
| items_purchased     | Total number of items purchased in the order      |
| price_usd           | Total amount paid for the order in USD            |
| cogs_usd            | Total cost of goods sold (COGS) for the order in USD |

---

### 4. **products**: Contains details about the products available.

| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| product_id          | Unique identifier for each product                |
| created_at          | Date when the product was added to the catalog    |
| product_name        | Name of the product                               |

---

### 5. **website_sessions**: Tracks website traffic and user sessions.

| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| website_session_id  | Unique identifier for each website session        |
| created_at          | Date and time when the session started            |
| utm_source          | Source of the traffic (e.g., 'gsearch', 'bsearch')|
| utm_campaign        | Specific campaign name or type (e.g., 'nonbrand', 'brand') |
| device_type         | Type of device used during the session (e.g., 'mobile', 'desktop') |
| http_referer        | Referring URL that led the user to the website    |

---

### 6. **website_pageviews**: Records page views within each session.

| Column Name         | Description                                      |
|---------------------|--------------------------------------------------|
| website_pageview_id | Unique identifier for each page view              |
| website_session_id  | Identifier linking to the session during the page view |
| pageview_url        | URL of the page that was viewed                   |
| created_at          | Date and time when the page was viewed            |
## Entity Relationship Diagram
Below is a diagram showing the relationships between the tables in the SQL Workbench environment:

![image](https://github.com/user-attachments/assets/7fcc3e16-32ba-4899-9a9e-61038dea1272)


## Requirements and Insights
1. **Monthly Trends for Gsearch Sessions and Orders**: Showcases Gsearch growth.
2. **Gsearch Brand vs. Non-brand Campaigns**: Non-brand sessions outpaced brand.
3. **Device Analysis**: Mobile sessions high, desktop conversion better.
4. **Channel Trends**: Gsearch is the dominant traffic source.
5. **Website Performance**: Gradual improvement in conversion rates.
6. **Landing Page Test Impact**: `Lander-1` boosted conversions.
7. **Conversion Funnel Analysis**: `Lander-1` users had better flow.
8. **Volume Growth**: Steady increase in sessions and orders.
9. **Cross-Selling Analysis**: Strong cross-sell between products post-launch.

## Usage
To replicate this analysis, clone the repository and follow the SQL scripts provided:

git clone [Click Here](https://github.com/HarshaVardhan1505/maven-fuzzy-factory.git)


## Conclusion
The analysis helps understand traffic patterns, user behavior, and product performance, guiding strategic decisions for future growth.
