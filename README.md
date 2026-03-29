# XSOAR UCD Generator

**Professional As-Built Document Generator for Cortex XSOAR Playbooks**

Automatically transforms any XSOAR playbook (`.yml`) into a **clean, enriched, professional As-Built document** — ready for customer delivery.

### Why this tool exists
PS consultants and XSOAR administrators spend hours manually creating UCD / As-Built documents.  
This tool **eliminates that manual work** by generating complete, beautifully formatted Microsoft Word documents in seconds — including full flow logic, conditional tasks with real conditions, transformers, arguments, sub-playbooks, and more.

**Saves hours of repetitive work** for every playbook.

### Key Features

- **Automatic As-Built Document Generation**  
  One command → complete professional Word document from any playbook YML.

- **Full Sub-Playbook Support**  
  Automatically detects and includes detailed flow tables for every sub-playbook (recursive).

- **Rich Conditional Task Representation**  
  Shows `(Conditional Task)` + the actual conditions (e.g. `If incident.sourceBrand == Manual AND incident.sourceBrand == EWS v2`).

- **Detailed Transformers & Arguments**  
  Clearly displays complex script arguments, transformers (`Cut`, `replace`, `concat`, etc.), and their exact values.

- **Easy Customization**  
  Pass consultant name and customer name directly via command-line arguments.

- **Professional Output**  
  Montserrat font, perfectly balanced tables, clean green headers, auto-distributed columns, current date, and Document Control section.

### Quick Start

```powershell
# Basic usage (recommended)
python ucd_generator.py ".\Phishing\Phishing___BM_Final.yml" --auto-subs --out "Phishing As-Built.docx"
