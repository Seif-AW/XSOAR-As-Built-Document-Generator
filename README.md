XSOAR UCD Generator

**Professional As-Built Document Generator for Cortex XSOAR Playbooks**

Automatically converts any Cortex XSOAR playbook (`.yml`) into a **clean, enriched, professional As-Built document** in Microsoft Word — ready for customer delivery.

### Why this tool brings real value
PS consultants and XSOAR administrators waste hours manually creating UCD / As-Built documents.  
This tool **eliminates that manual work** by generating complete, beautifully formatted documents in seconds — including full flow logic, conditional tasks with real conditions, transformers, arguments, and sub-playbooks.

**Saves hours of repetitive work** on every single playbook.

### Key Features

- Automatically generates professional As-Built documents from any playbook YML file
- Full support for sub-playbooks (recursive — shows detailed flow tables for every included sub-playbook)
- Rich representation of conditional tasks with actual conditions displayed
- Clear display of transformers, complex arguments, and script details
- Easy customization of customer name and consultant name via command-line arguments
- Clean, consistent layout with Montserrat font and perfectly balanced tables

### Quick Start

```powershell
# Recommended (auto-detects sub-playbooks)
python ucd_generator.py ".\Phishing\Phishing___BM_Final.yml" --auto-subs --out "Phishing As-Built.docx"

# With custom names
python ucd_generator.py "main.yml" --auto-subs --customer "Banque Misr SOC" --ps "Seif Abdelwahid"
Installation

Clone or download this repository
Install the required Python packages:

PowerShellpip install python-docx PyYAML
Full Command Options








































ArgumentDescriptionDefault ValueymlMain playbook YML file (required)---auto-subsAuto-discover sub-playbooks in the same folder as mainFalse--subsPath to folder containing sub-playbooks---outOutput Word document name<playbook>_UCD.docx--customerCustomer name (shown in document header)"Banque Misr SOC"--psConsultant / PS name"Seif Abdelwahid – Palo Alto Networks"
Who is this for?

XSOAR Professional Services Consultants
SOC Automation Engineers
XSOAR Administrators who need to deliver clean, professional documentation to customers

Stop spending hours on documentation. Generate professional As-Built documents in seconds.
