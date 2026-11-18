# n8n-veo-video-automation
Autonomous n8n cloud video pipeline generating 35s faceless educational shorts (Zack D. Films style) using Google Veo 3, Gemini, and Shotstack API.

# 🎬 Autonomous Faceless Video Generator (n8n + Veo 3 + Shotstack)

[![n8n](https://img.shields.io/badge/n8n-Cloud-FF6C37?style=flat-square&logo=n8n)](https://n8n.io/)
[![Google Veo](https://img.shields.io/badge/Google-Veo_3.x-4285F4?style=flat-square&logo=google)](https://cloud.google.com/vertex-ai)
[![Shotstack](https://img.shields.io/badge/Shotstack-API-000000?style=flat-square)](https://shotstack.io/)

A 100% cloud-native, fully autonomous video production pipeline that generates 35-second, high-retention educational short-form videos (in the style of Zack D. Films). This workflow reduces video production time from 2.5 hours to zero active human labor.

## 🚀 The Problem It Solves
Scaling a faceless YouTube Shorts, TikTok, or Instagram Reels channel requires massive volume. Manually writing scripts, generating 7-second visual chunks, extracting frames to prevent jump cuts, syncing AI voiceovers, and mixing audio is repetitive and expensive. 

This project is a **set-it-and-forget-it cloud engine**. You drop a video topic into a Google Sheet, and the system autonomously handles scripting, 3D cinematic generation, audio mixing, and final assembly, delivering a ready-to-publish MP4 to your Google Drive.

## ⚙️ Cloud Architecture & Tech Stack

This pipeline requires **zero local servers** and bypasses the need for local FFmpeg by relying entirely on cloud APIs.

* **Workflow Orchestration (n8n Cloud):** Manages the logic loop, API routing, and error handling.
* **Scripting (Google Gemini 2.5 Pro):** Auto-generates the 5-shot narrative and creates precise, highly descriptive macro-camera prompts.
* **Cinematic Video (Google Veo 3.x API):** Generates photorealistic, 8-second 3D cutaway animations with native spatial sound effects (whooshes, mechanical clicks).
* **Frame Extraction & Editing (Shotstack API):** Programmatically captures the exact final frame of Shot A to use as the starting image prompt for Shot B, ensuring seamless visual continuity. It also handles the final 35-second assembly and audio ducking.
* **Voiceover (ElevenLabs):** Provides natural, broadcast-quality AI narration.
* **State Management (Google Sheets):** Acts as the database to track clip generation status. If an API times out, a watchdog trigger resumes the workflow from the exact failed clip rather than starting over.

## 🧠 Key Engineering Highlights
* **Infinite Clip Chaining:** Bypasses standard AI video length limits by injecting programmatic frame-extraction directly into the prompt loop.
* **Zero-Waste Crash Recovery:** Built-in row locking and checkpointing means system crashes never result in lost progress or burned API credits.
* **Pre-Balanced Audio Mastering:** The final assembly node automatically sets foreground narration to 100% volume while ducking the native background sound effects to 28%, matching professional editing standards.

## 🤝 Let's Collaborate

I built this to prove that content creation can be transformed from a manual bottleneck into an automated, predictable revenue engine. I am actively looking to collaborate with forward-thinking brands, marketing agencies, and founders who want to leverage automated content systems to scale their reach.

* **Want to implement a custom automated content pipeline for your business?**
* **Looking to scale your media output without hiring a massive editing team?**

**Let’s connect.** Reach out to me directly via LinkedIn (link in GitHub bio) or send a direct message to discuss how we can build something powerful together. 

---
**Tags & Keywords:** `n8n workflow` `AI Video Automation` `YouTube Shorts Automation` `TikTok Bot` `Google Veo API` `Shotstack` `Faceless Channel Automation` `Generative AI` `Content Creation Pipeline` `Serverless Video Editing`
