# E-Commerce Food Delivery Data Analytics Project

## Project Overview

This project focuses on analyzing an e-commerce food delivery platform similar to companies like Delivery Hero or Uber Eats. The goal is to explore user behavior, restaurant performance, order patterns, delivery efficiency, payment methods, and customer satisfaction through comprehensive data analysis.

We use a realistic, relational database schema covering all aspects of the platform: users, restaurants, menus, orders, deliveries, payments, and ratings. This enables end-to-end insights into the entire food delivery lifecycle.

---
## Database Schema

### Schema Diagram

![Database Schema](./docs/Schema.png)

## Database Tables

The schema consists of the following main tables, designed to capture all relevant data points in the system:

| Table Name           | Description                                            |
|----------------------|--------------------------------------------------------|
| `users`              | Registered customers and their profile details          |
| `restaurants`        | Details of restaurants offering food                     |
| `menu_items`         | Menu items offered by restaurants                         |
| `orders`             | Customer orders with timestamps, status, and payment info |
| `order_items`        | Items included in each order                              |
| `delivery_persons`   | Delivery agents responsible for fulfilling orders        |
| `deliveries`         | Delivery events linked to orders with timing and status  |
| `payments`           | Payment records for orders including method and status   |
| `ratings`            | Customer feedback and ratings for orders and restaurants  |
| `payment_methods`    | Lookup table for normalized payment method types          |
| `promotions`         | Marketing campaigns offering discounts                    |
| `order_promotions`   | Discounts applied to orders via promotions                |
| `menu_item_history`  | Historical price and availability tracking for menu items |
| `delivery_status_history` | Status timeline for deliveries                        |
| `user_logins`        | User login activity tracking for behavioral analysis      |

---

## Table Relationships and Data Flow

- Each **user** can place multiple **orders**.
- Each **order** is linked to one **restaurant** and contains multiple **order_items**.
- Each **order_item** references a **menu_item** from the restaurant's menu.
- Orders are linked to one or more **payments**, normalized via the `payment_methods` table.
- Each **order** corresponds to one **delivery** fulfilled by a **delivery_person**.
- Deliveries have a **status history** tracking progress over time.
- Customers provide **ratings** and feedback per order and restaurant.
- **Promotions** can be applied to orders to offer discounts.
- **Menu items** have a historical log to track price changes.
- User login data supports behavioral and device usage analysis.

---

## Key Analytical Questions and Findings

This project aims to answer several critical business questions by analyzing the data:

### User & Order Analytics
- How do user signup trends vary by city and device?
- What percentage of users are loyal customers?
- What are the peak order times and popular cuisines?

### Restaurant & Menu Performance
- Which restaurants have the highest average ratings?
- How does menu item availability affect order frequency?
- How have menu item prices changed over time?

### Delivery & Logistics
- What is the average delivery time and distance?
- Which delivery persons have the highest completion rates?
- How often do deliveries experience delays or status changes?

### Payment & Promotions
- What are the most common payment methods?
- How effective are promotions in increasing order value or frequency?

### Customer Satisfaction & Feedback
- What is the distribution of customer ratings?
- Are there correlations between delivery time and ratings?
- What common feedback themes emerge in text comments?

---

## Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- SQL (PostgreSQL / MySQL)
- DBML for database schema design
- Jupyter Notebooks for interactive data exploration

---

## How to Use This Repository

1. Explore the **DBML schema file** to understand the database structure.
2. Load the **sample datasets** (CSV files) corresponding to each table.
3. Run the **Python notebooks** to perform exploratory data analysis and visualization.
4. Modify queries and visualizations to fit new hypotheses or business needs.

---

## Contribution and Future Work

- Integrate real-time order and delivery data for live dashboards.
- Add customer segmentation based on order history and behavior.
- Implement predictive models for delivery time estimation and churn.
- Expand schema to include multi-restaurant orders and subscription services.

---

![Project Structure](./docs/Project-Structure.png)

---

## License

This project is open source under the MIT License.

---

## Contact

For questions or collaborations, please contact:

**Nandu**  
Email: nandu26m.com  
GitHub: [github.com/nandu26m](https://github.com/nandu26m)

---

| Table                         | Number of Records | Notes   |
| ----------------------------- | --------------------------- |
| **users**                     | 10,000                      |
| **restaurants**               | 500                         |
| **menu\_items**               | 5,000                       |
| **orders**                    | 50,000                      |
| **order\_items**              | 120,000                     |
| **delivery\_persons**         | 200                         |
| **deliveries**                | 48,000                      |
| **payments**                  | 50,000                      |
| **ratings**                   | 25,000                      |
| **payment\_methods**          | 5                           |
| **promotions**                | 50                          |
| **order\_promotions**         | 8,000                       |
| **menu\_item\_history**       | 10,000                      |
| **delivery\_status\_history** | 150,000                     |
| **user\_logins**              | 80,000                      |
