# Cybersecurity_internship-task-2
Task 2


# Cybersecurity Internship - Task 2: Analyze a Phishing Email Sample

## Objective
The goal of this task was to identify phishing characteristics in a suspicious email sample by examining its technical header and body content using the prescribed tools and hints.

## Deliverables
1.  **Report listing phishing indicators found** (Contained in `Phishing_Analysis_Report.md` or `Phishing_Analysis_Report.txt`)
2.  **GitHub repository link** (This repository itself)

---

## 🔍 Analysis Process

### 1. Data Source
* **File:** `Phishing_Email_Source.txt`
* The raw source code of the suspicious solar panel promotional email was obtained for analysis.

### 2. Header Analysis (Technical Indicators)
To verify the authenticity of the sender (Hint 3), the full email header was copied and pasted into a free online header analyzer (e.g., Google Admin Toolbox or MXToolbox).

* **Key Findings:** The analysis immediately revealed critical authentication failures, including `spf=none`, `dkim=none`, and `compauth=fail reason=001`, confirming the sender address was forged (spoofed). The sender and reply-to domains were also found to be mismatched.

### 3. Body Content Analysis (Social Engineering)
The visible body of the email was analyzed for common phishing tactics (Hints 4, 5, 6, 7):

* **Urgency:** Language was used to create a false sense of scarcity/urgency ("Wacht daarom niet langer...") to pressure the recipient into clicking immediately (Hint 5).
* **Mismatched Links:** The link text appeared legitimate, but the actual URL destination pointed to a suspicious redirect/tracking domain (`go.nltrck.com...`), confirming misdirection (Hint 6).
* **Quality:** Grammatical errors were noted, which is typical of low-effort phishing attempts (Hint 7).

---

## ✅ Conclusion

All findings, cross-referenced with the original email source, are detailed in the attached report file. The high number of technical authentication failures combined with clear social engineering tactics confirms this message is a **phishing/spam email**.

### File Structure in this Repository

| File Name | Description |
| :--- | :--- |
| `README.md` | This file, summarizing the objective and process. |
| `Phishing_Email_Source.txt` | The complete, raw source code of the email used for analysis (the evidence). |
| `Phishing_Analysis_Report.md` | The final deliverable: a detailed list of all phishing indicators found (the table). |
