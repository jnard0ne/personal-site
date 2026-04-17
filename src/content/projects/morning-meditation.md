---
title: Morning Meditation
description: An email subscription service that delivers an AI-generated quote and meditation each morning. Inspired by Ryan Holiday's The Daily Stoic.
url: https://www.morning-meditation.com/
tags:
  - Flask
  - Python
  - Claude AI
  - Supabase
  - GitHub Actions
status: active
---

A daily email service delivering one AI-generated meditation each morning. Subscribers receive a quote drawn from a rotating set of sources — Marcus Aurelius, Seneca, Epictetus, Buddhist and Taoist philosophy, and others — along with a reflection prompt. A journal feature allows users to write down their thoughts.

Built with Flask, hosted on Render, and powered by the Anthropic API for content generation. Subscriber data lives in Supabase; daily sends run via GitHub Actions on a 9 AM ET cron. SMS delivery is in the pipeline pending Twilio A2P approval.