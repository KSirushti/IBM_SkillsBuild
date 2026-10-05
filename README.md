# Cloudflare Open-Source Ecosystem Intelligence

## Project Overview

This project analyzes the **Cloudflare GitHub ecosystem** to understand repository popularity, developer engagement, technology composition, maintenance activity, and repository health.

The project follows the business-intelligence workflow:

**Data → Information → Insights → Decision → Action**

The analysis uses Python-based data analytics to transform GitHub repository data into meaningful insights and practical recommendations.

---

## Problem Statement

The Cloudflare developer ecosystem contains both official Cloudflare repositories and community-owned repositories covering technologies such as Workers, Pages, DNS, Tunnel, Wrangler, and Cloudflared.

The objective of this project is to answer:

> **What does the current Cloudflare developer ecosystem look like, which technologies and repositories show strong community engagement, and which repositories show strong or weak signs of ongoing ecosystem health?**

---

## Objectives

- Understand the composition of the Cloudflare-related open-source ecosystem.
- Identify popular and highly engaged repositories.
- Compare official Cloudflare repositories with community-owned repositories.
- Analyze programming-language distribution.
- Examine repository activity and maintenance recency.
- Study relationships between popularity, engagement, repository age, and activity.
- Identify potential ecosystem risks and opportunities.
- Develop a transparent Repository Health Score.
- Convert analytical findings into actionable recommendations.

---

## Dataset

**Dataset:** Cloudflare GitHub Ecosystem 2026

**Source:** Kaggle

**Dataset Link:**  
https://www.kaggle.com/riyagarg0314/cloudflare-github-ecosystem-2026

### Dataset Statistics

| Metric | Value |
|---|---:|
| Repositories analyzed | 1,882 |
| Source variables | 26 |
| Total stars | 770,170 |
| Total forks | 318,380 |
| Official Cloudflare repositories | 300 |
| Archived repositories | 153 |

### Important Dataset Limitation

This dataset represents a **current snapshot of repositories**, rather than a historical time series.

Therefore, this project analyzes current:

- Popularity
- Community engagement
- Repository activity
- Technology composition
- Repository health

It does **not** claim historical growth or decline unless the available data supports such a conclusion.

---

## Key Features Used

The analysis uses repository-level attributes including:

- Stars
- Forks
- Watchers
- Open issues
- Stars per day
- Programming language
- License
- Topics
- Repository creation date
- Repository update date
- Last push date
- Repository age
- Days since last push
- Owner type
- Official Cloudflare indicator
- Archived status
- Queried topic

---

## Methodology

### 1. Data Loading

The dataset is loaded using Pandas from:
The notebook performs initial inspection of:

- Dataset dimensions
- Column names
- Data types
- Descriptive statistics
- Missing values
- Duplicate records

### 2. Data Cleaning

The following preprocessing steps are performed:

- Standardize column names
- Remove unnecessary whitespace from text fields
- Convert date columns into datetime format
- Check missing values
- Detect duplicate records
- Remove exact duplicate rows where necessary

### 3. Feature Engineering

Additional analytical variables are created, including:

#### Fork-to-Star Ratio

Measures community participation relative to repository popularity.

#### Issues per 1,000 Stars

Provides a normalized view of open issues relative to repository popularity.

#### Activity Status

Repositories are classified according to the number of days since their latest push:

| Activity Status   | Days Since Last Push |
|-------------------|----------------------|
| Very Active       | ≤ 7 days             |
| Active            | 8–30 days            |
| Recently Active   | 31–90 days           |
| Moderately Active | 91–180 days          |
| Low Activity      | 181–365 days         |
| Stale             | > 365 days           |

#### Repository Age

Repositories are grouped according to their age to support comparisons between newer and established projects.

---

## Analysis

The project analyzes the ecosystem across several dimensions.

### Executive KPIs

Key metrics include:

- Total repositories
- Total stars
- Total forks
- Total watchers
- Official Cloudflare repositories
- Archived repositories

### Programming Language Analysis

The project examines the distribution of programming languages used across repositories and investigates whether different languages are associated with different levels of popularity or activity.

### Repository Popularity

Repository popularity is evaluated using:

- Stars
- Forks
- Watchers
- Stars per day

### Repository Activity

Maintenance activity is analyzed using:

- Days since last push
- Activity status
- Archived status
- Repository age

### Official vs Community Analysis

Official Cloudflare repositories are compared with community-owned repositories using measures such as:

- Repository count
- Stars
- Forks
- Maintenance recency

---

## Repository Health Score

A descriptive **Repository Health Score** is developed to help identify repositories with stronger or weaker ecosystem signals.

The score combines normalized indicators related to:

- Activity
- Popularity
- Community engagement
- Maintenance
- Recency

The score is used as an analytical prioritization tool.

It is **not a machine-learning prediction model** and should not be interpreted as an absolute measure of software quality.

---

## Technologies Used

### Programming

- Python

### Data Analysis

- Pandas
- NumPy

### Data Visualization

- Matplotlib
- Seaborn

### Development Environment

- Jupyter Notebook

---

## Project Structure

Cloudflare-Ecosystem-Intelligence/
│
├── Sirushti_CloudflareEcosystemIntelligence.ipynb
├── cloudflare_ecosystem_2026.csv
├── requirements.txt
├── Sirushti_ProjectReport.docx
└── README.md



```text
cloudflare_ecosystem_2026.csv
