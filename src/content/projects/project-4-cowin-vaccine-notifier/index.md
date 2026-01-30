---
title: "CoWIN Vaccine Notifier"
summary: "A viral web app that notified 460+ users about vaccine availability via email during the COVID-19 crisis."
date: "May 20, 2021"
draft: false
tags:
- Django
- AWS EC2
- Python
- System Design
---

![CoWIN Vaccine Notifier Dashboard](https://placehold.co/600x400?text=CoWIN+Notifier+Dashboard)

## The Problem
During the peak of the COVID-19 pandemic in India, vaccine slots were booking out in seconds. Users had to manually refresh the CoWIN portal hundreds of times a day, often missing their chance.

## The Solution
I built an automated **Availability Tracker** that polled the government's public API and alerted users instantly via email when a slot opened in their specific district.

- **Architecture:** A **Django** backend running scheduled cron jobs on an **AWS EC2** instance to poll API endpoints efficiently without hitting rate limits.
- **Delivery:** Integrated SMTP services to blast real-time notifications to subscribers.
- **Impact:** The project went viral on LinkedIn, solving a critical need for hundreds of families.

### Key Metrics
- **10,000+** Emails sent in the first week.
- **460+** Registered users across India.
- **100%** Uptime during peak traffic.

### Links
- [GitHub Repository](https://github.com/AnubhavMadhav/COVID-Vaccine-Notifier)