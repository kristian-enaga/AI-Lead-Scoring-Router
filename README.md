# 📌 AI Lead Scoring & Priority Router

An automated AI triage engine built with **n8n** and **Google Gemini AI** to automatically qualify inbound sales leads and route high-value opportunities to sales teams in real time.

![AI scoring](Portfolio2.png)
---

## 🎯 Business Problem
Sales teams waste up to 70% of their day reviewing low-budget inquiries, while high-value enterprise prospects wait hours for a response. This delay leads to lost deals and lower pipeline conversion rates.

## 🚀 Solution Overview
This automated n8n workflow acts as an instant lead triage system:
1. **Webhook Trigger:** Receives raw lead payloads dynamically.
2. **AI Lead Scoring:** Evaluates budget, company size, and urgency using Google Gemini.
3. **Dynamic Routing:**
   * **VIP Branch (True):** Posts immediate alerts with AI reasoning to Slack for sales intervention.
   * **Standard Branch (False):** Automatically sends a self-service resource packet via Gmail.
4. **CRM Sync:** Logs all scored leads centrally into Google Sheets.

---

## 📹 Loom Video Walkthrough
Watch the 3-minute project demo:  
👉 AI Lead Scoring & Priority Router Demo](https://www.loom.com/share/38164c8a840f4076b3ac0ec62a26e3ce)

---

## 🛠️ Tech Stack & Integrations
* **Automation Engine:** n8n
* **AI Model:** Google Gemini Chat Model
* **Notifications:** Slack API
* **Email Communication:** Gmail API
* **Database/CRM:** Google Sheets API

---

## 📋 Scoring Criteria
* **High Priority (VIP):**
  * Budget $\ge$ $10,000
  * Enterprise size (500+ or 1,000+ employees)
  * High urgency or immediate replacement needs
* **Low Priority (Standard):**
  * Budget < $2,000 with company size < 50 employees
  * General pricing inquiries or trial requests

---

## ⚙️ How to Import
1. Download the `workflow.json` file from this repository.
2. Open your n8n instance.
3. Go to **Workflows** $\rightarrow$ **Import from File**.
4. Configure your credentials for Google Gemini, Slack, Gmail, and Google Sheets.
