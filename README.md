# XSOAR UCD Generator

**Professional As-Built Document Generator for Cortex XSOAR Playbooks**

Automatically converts XSOAR playbook `.yml` files into beautiful, white-labeled Microsoft Word UCD documents.

![Example Screenshot](screenshot.png)

### ✨ Features
- Full **Montserrat** font across the entire document
- Beautiful green professional table headers
- Perfectly balanced columns
- Recursive sub-playbook support
- Auto current date + customizable customer name
- `--auto-subs` smart discovery

### Quick Start

```powershell
python ucd_generator.py ".\Phishing\Phishing___BM_Final.yml" --auto-subs --out "Phishing_UCD.docx"
