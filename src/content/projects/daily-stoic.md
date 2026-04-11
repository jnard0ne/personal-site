---
title: Daily Stoic Meditation
description: An email subscription service that delivers an AI-generated Stoic quote and meditation each morning. Inspired by Ryan Holiday's The Daily Stoic.
url: https://daily-stoic-meditation.onrender.com
tags: [Flask, Python, Claude AI, Supabase, GitHub Actions]
status: active
---

A daily email service delivering one AI-generated Stoic meditation each morning. Subscribers receive a quote drawn from a rotating set of sources — Marcus Aurelius, Seneca, Epictetus, Buddhist and Taoist philosophy, and others — along with a reflection prompt.

Built with Flask, hosted on Render, and powered by the Anthropic API (Claude Haiku) for content generation. Subscriber data lives in Supabase; daily sends run via GitHub Actions on a 9 AM ET cron. SMS delivery is in the pipeline pending Twilio A2P approval.
