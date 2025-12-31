# web-vuln-templates

Official vulnerability templates for **web-vuln-scanner (WVS)**.

This repository contains community-ready, production-safe templates
used by the WVS engine.

---

## 📦 Available Templates

| Category | Template | Description |
|--------|---------|-------------|
| XSS | xss-basic | Reflected XSS via query parameter |
| SQLi | sqli-error-based | Error-based SQL injection |
| LFI | lfi-basic | Local File Inclusion |
| SSRF | ssrf-basic | Server-Side Request Forgery |
| Misconfig | basic-auth | Exposed Basic Auth |

---

## 🚀 Usage

Clone the templates:

```bash
git clone https://github.com/alishams11/web-vuln-templates.git

Run a scan using a template:
python3 -m pywvs scan https://example.com \
  -t templates/xss/xss-basic.yaml \
  -o report.json
'''
🧠 Confidence Scores

Each template includes a confidence field (0.0–1.0) indicating
the likelihood of a true positive.

Use .wvs-ignore to suppress known false positives.

##⚠️ Disclaimer

Templates are provided for educational and authorized testing only.
Do not scan systems without permission.

##🤝 Contributing

Pull requests welcome!
Please ensure templates are:

minimal

deterministic

safe

well-described

##📜 License
