---
title: "Verbal"
summary: "An Emotion Analysis engine for audio and video content, built for BothOfUs AB (Sweden)."
date: "Jun 20, 2021"
draft: false
tags:
- AI
- Emotion Analysis
- DigitalOcean
- Nginx
---

![Verbal Dashboard](https://placehold.co/600x400?text=Verbal+Analysis+Tool)

## The Problem
Understanding the "Sentiment" of video content usually requires manual watching. My client needed an automated way to gauge the emotional tone of YouTube videos and raw audio files.

## The Solution
I developed **Verbal**, a processing pipeline that extracts audio tracks and runs them through sentiment analysis models.

- **Architecture:** Built with **Django** and deployed on **DigitalOcean Droplets** using **Nginx** as a reverse proxy.
- **Core Feature:** Users upload a file or paste a YouTube link, and the system generates a report breaking down emotions (Happy, Sad, Neutral, Angry).

### Key Metrics
- **International Delivery:** Successfully delivered to a Swedish client (BothOfUs AB) as part of a remote internship.
- **Full Stack:** Handled everything from the UI (HTML/CSS) to the server configuration (Nginx/Gunicorn).

### Links
- [Company Website](https://bothofus.se/)