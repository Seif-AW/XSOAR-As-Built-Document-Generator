# XSOAR UCD Generator

**Professional As-Built Document Generator for Cortex XSOAR Playbooks**

Automatically converts XSOAR playbook `.yml` files into beautiful, white-labeled Microsoft Word UCD documents.

![Example Screenshot](screenshot.png)

- Recursive sub-playbook support
- Auto current date
- `--auto-subs` sub-playbook discovery

### Quick Start

```powershell
python ucd_generator.py ".\Phishing\Phishing___BM_Final.yml" --auto-subs --out "Phishing_UCD.docx"
