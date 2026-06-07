# SOC Automations

Automated workflows I build to speed up SOC triage and reduce manual investigation time.

---

## 1. IOC Enrichment & Triage (Tines)

**What it does:** Automatically enriches a suspicious IP address and generates a bilingual (EN/FR) triage summary.

**Workflow:**
1. 🔹 Webhook receives a suspicious IP
2. 🔹 VirusTotal enriches it with detection data
3. 🔹 A condition evaluates if it crosses the malicious threshold (>5 detections)
4. 🔹 The verdict gets formatted automatically with a direct VT link
5. 🔹 An AI Agent writes a triage summary in English and French

**Tools:** Tines, VirusTotal API, LLM Agent

**Setup:**
- Import `IOC_Enrichment_Triage.json` into Tines
- Add your own VirusTotal API key in the "Check VirusTotal" action
- Send a POST request to the webhook with `{"ip": "8.8.8.8"}` to test

**Screenshot:**

<img width="1119" height="854" alt="Screenshot 2026-06-07 at 4 21 08 PM" src="https://github.com/user-attachments/assets/682c3d41-9ce7-4a7b-9132-cc0b8a1847aa" />


---

*Built by [Amina Belhout](https://linkedin.com/in/it-amina-belhout) — Junior SOC Analyst at Bradley & Rollins, working toward AI SOC / Security Automation Engineer.*
