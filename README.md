# Web Vulnerability Templates (WVS)

Official **detection templates** for the
[web-vuln-scanner (WVS)](https://github.com/alishams11/web-vuln-scanner).

This repository contains **auditable, production-safe, template-driven
security detections** designed for real-world
**Pentest, AppSec, and SOC workflows**.

---

## 🧠 Template-Driven Detection Philosophy

Instead of embedding detection logic directly in code, WVS uses
**template-driven scanning**, where each template defines:

- What requests are sent
- What response patterns are evaluated
- How confident the detection is

This approach allows:
- Easier tuning and auditing
- Reduced false positives
- Independent evolution of detection rules

---

## 📦 Available Templates

| Category | Template | Description |
|--------|---------|-------------|
| XSS | xss-basic | Reflected XSS via query parameter |
| SQLi | sqli-error | Error-based SQL injection |
| LFI | lfi-basic | Local File Inclusion |
| SSRF | ssrf-basic | Server-Side Request Forgery |
| Misconfig | auth-misconfig | Exposed HTTP Basic Authentication |

---

## 🚀 Usage

Clone the templates repository:

```bash
git clone https://github.com/alishams11/web-vuln-templates.git
```
Run a scan using a specific template:
python3 -m pywvs scan https://example.com \
  -t templates/xss/xss-basic.yaml \
  -o report.json


Each finding includes:

Severity

Confidence score

Evidence for reporting

---

## 🧠 Confidence Scores
Each template defines a confidence value (low / medium / high)
indicating the estimated likelihood of a true positive.

Confidence scores are designed to:

Reduce alert fatigue

Help prioritization

Support SOC and AppSec triage workflows

Use .wvs-ignore to suppress accepted or known findings.

---

## 🧩 Template Structure (Overview)
Each template follows a standard schema:

Metadata (id, severity, confidence)

One or more HTTP requests

Matchers defining detection logic

📄 Full specification:
docs/template-spec.md

---

## 🤝 Contributing
Pull requests are welcome.

When contributing templates, please ensure they are:

Minimal and deterministic

Safe and non-destructive

Clearly described

Aligned with the official template specification

---

## ⚠️ Disclaimer
Templates are provided for educational and authorized testing only.
Do not scan systems without explicit permission.

---

## 📜 License
MIT License
