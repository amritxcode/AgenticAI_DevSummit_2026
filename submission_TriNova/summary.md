# Submission Summary

## Team

**Team Name:** AlphaAI  
**Members:**  
Amrit Rayt | Developer  
Teammate 2 | AI Logic  
Teammate 3 | UI & Testing  

**Contact Email:** your@email.com  

---

## Problem Statement

**Selected Problem:** PS-01  
**Problem Title:** Client Onboarding  

Scrollhouse currently performs client onboarding manually, taking 45 minutes per client and often missing critical steps like Airtable entry or incorrect setup. This leads to operational inefficiencies, delayed invoicing, and poor client experience.  

Our system automates the entire onboarding workflow, reducing time to near zero and eliminating human error.

---

## System Overview

Our system is an Agentic AI onboarding assistant that takes client details as input and completes the onboarding process automatically.  

It plans onboarding steps using an LLM, executes them through multiple agents, and generates outputs such as sending emails, creating folders, and storing data.  

The system ensures consistency, reduces errors, and provides a final onboarding summary without manual intervention.

---

## Tools and Technologies

| Tool or Technology | Version or Provider | What It Does in Your System |
|---|---|---|
| Python | 3.x | Core backend logic |
| Streamlit | Latest | UI for interaction |
| Groq API | LLaMA3 | LLM planning and decision making |
| dotenv | python-dotenv | Secure API key management |
| SMTP | Gmail | Sends onboarding emails |
| CSV | Built-in | Stores client records |

---

## LLM Usage

**Model(s) used:** LLaMA3-70B  
**Provider(s):** Groq  
**Access method:** API key  

| Step | LLM Input | LLM Output | Effect on System |
|---|---|---|---|
| Planning | Client details (brand, category) | List of onboarding steps | Determines workflow dynamically |
| Decision fallback | Same input | Default plan | Ensures system reliability |

---

## Algorithms and Logic

The system uses an LLM-based planning mechanism to dynamically generate onboarding workflows.  

A retry mechanism is implemented for email sending to ensure reliability.  

The orchestrator maps each planned step to a corresponding agent function and executes sequentially.  

Fallback logic ensures the system continues functioning even if LLM fails.

---

## Deterministic vs Agentic Breakdown

| Layer | Percentage | Description |
|---|---|---|
| Deterministic automation | 70% | Email sending, folder creation, data storage |
| LLM-driven and agentic | 30% | Planning onboarding steps dynamically |

The agentic layer determines the workflow dynamically. Without the LLM, the system would follow a fixed sequence and lose adaptability.

---

## Edge Cases Handled

| Edge Case | How Your System Handles It |
|---|---|
| Duplicate client | Blocks onboarding and shows error |
| Missing email | Stops execution and alerts user |
| Email failure | Retry mechanism attempts resend |

---

## Repository

**GitHub Repository Link:** https://github.com/YOUR_USERNAME/AgenticAI_DevSummit_2026  
**Branch submitted:** main  
**Commit timestamp of final submission:** (paste from GitHub commit)  

---

## Deployment

**Is your system deployed?** No  

---

## Known Limitations

- Notion, Airtable, and Google Drive are simulated (mock links)  
- Limited edge case handling due to time constraints  
- No real API integration for external tools  

---

## Anything Else

We improved the system by integrating an LLM planner, converting a static automation script into a dynamic agentic system capable of decision-making and workflow generation.

The addition of retry logic and multi-agent orchestration makes the system closer to real-world enterprise automation tools.