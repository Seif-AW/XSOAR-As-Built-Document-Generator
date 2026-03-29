# XSOAR As-Built Generator

**Professional As-Built Document Generator for Cortex XSOAR Playbooks**

Automatically converts any Cortex XSOAR playbook (`.yml`) into a **clean, enriched, professional As-Built document** in Word.

### Why this tool brings real value

PS consultants and XSOAR Engineers waste hours manually creating UCD / As-Built documents.  
This tool **eliminates that manual work** by generating complete, beautifully formatted documents in seconds — including full flow logic, conditional tasks with real conditions, transformers, arguments, and sub-playbooks.

**Saves hours of repetitive work on every single playbook.**

### Key Features

- Automatically generates professional As-Built documents from any playbook YML file
- Full support for sub-playbooks (recursive — shows detailed flow tables for every included sub-playbook)
- Rich representation of conditional tasks with actual conditions displayed
- Clear display of transformers, complex arguments, and script details
- Easy customization of customer name and consultant name via command-line arguments
- Clean, consistent layout with Montserrat font and perfectly balanced tables

### Requirements

- Python 3.8 or higher
- `python-docx`
- `PyYAML`

Install the required packages with:

```bash
pip install python-docx PyYAML
