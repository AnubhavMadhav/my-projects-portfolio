---
title: "Avengers of GitHub"
summary: "A gamified profile analyzer that assigns you an Avenger identity based on your GitHub coding stats."
date: "Nov 15, 2020"
draft: false
tags:
- Python
- GitHub API
- Gamification
- Django
---

![Avengers of GitHub Interface](https://placehold.co/600x400?text=Avengers+of+GitHub)

## The Idea
Developer portfolios can be boring. I wanted to create a fun, engaging way for developers to visualize their open-source contributions using pop culture.

## The Solution
A **Django-based Analysis Engine** that fetches a user's public GitHub data (commits, PRs, stars) and maps them to superhero traits.

- **The Algorithm:**
    - High Commit Frequency + Speed → **The Flash / Quicksilver**.
    - High Accuracy + Bug Fixes → **Captain America**.
    - Massive Codebase Management → **Iron Man**.
- **Tech Stack:** Consumed the **GitHub REST API** to aggregate stats in real-time and render a "Hero Card" for the user.

### Key Features
- **Profile Gamification:** Turned boring contribution graphs into shareable social content.
- **API Integration:** Handled rate limiting and complex JSON parsing from GitHub's data stream.

### Links
- [GitHub Repository](https://github.com/AnubhavMadhav/Avengers-Of-GitHub)