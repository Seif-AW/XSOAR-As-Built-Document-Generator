# 📄 XSOAR As-Built Generator

**Professional As-Built Document Generator for Cortex XSOAR Playbooks**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![python-docx](https://img.shields.io/badge/python--docx-latest-blue)](https://python-docx.readthedocs.io/)
[![PyYAML](https://img.shields.io/badge/PyYAML-latest-blue)](https://pyyaml.org/)

Automatically converts any Cortex XSOAR playbook (`.yml`) into a **clean, enriched, professional As-Built document** in Word — in seconds, not hours.

---

## 🚀 Why This Tool Exists

PS consultants and XSOAR engineers waste hours manually writing UCD / As-Built documents after every playbook build. This tool **eliminates that entirely** by parsing the playbook YAML directly and generating a fully formatted `.docx` with:

- Complete flow logic and task sequencing
- Real conditional logic with parsed expressions
- Transformer chains and complex argument mappings
- Full sub-playbook breakdowns in their own sections

**Saves hours of repetitive documentation work — on every single engagement.**

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 🗂 Playbook Parsing | Reads any standard XSOAR `.yml` playbook |
| 🔁 Sub-Playbook Support | Auto-discovers and documents all included sub-playbooks |
| 🔀 Conditional Logic | Displays real parsed conditions (`isNotEmpty`, `isEqualString`, etc.) |
| ⚙️ Transformer Chains | Shows `replace`, `Cut`, `concat`, and other transformer steps |
| 📋 Argument Mapping | Renders both simple and complex script arguments |
| 🎨 Professional Styling | Montserrat font, color-coded task types, balanced table layout |
| 🏷 Document Control | Auto-fills creation date, consultant name, and customer name |

---

## 📋 Requirements

- Python **3.8 or higher**
- `python-docx`
- `PyYAML`

---

## 📦 Installation

**1. Clone the repository**

```bash
git clone https://github.com/your-username/xsoar-as-built-generator.git
cd xsoar-as-built-generator
```

**2. Install dependencies**

```bash
pip install -r requirements.txt
```

---

## 🖥 Usage

```bash
python ucd_generator.py <playbook.yml> [OPTIONS]
```

### Arguments

| Argument | Required | Description |
|---|---|---|
| `yml` | ✅ Yes | Path to the main XSOAR playbook `.yml` file |
| `--subs <folder>` | ❌ No | Path to a folder containing sub-playbook `.yml` files |
| `--auto-subs` | ❌ No | Auto-discover sub-playbooks in the same folder as the main playbook |
| `--out <file.docx>` | ❌ No | Custom output file path (defaults to `<playbook_name>_As-Built.docx`) |
| `--customer <name>` | ❌ No | Customer name shown in the document header (default: `Customer Name`) |
| `--ps <name>` | ❌ No | Consultant name shown in the Document Control section |

---

## 💡 Examples

**Basic usage — just the main playbook:**
```bash
python ucd_generator.py "My Playbook.yml"
```

**With a custom customer name and consultant:**
```bash
python ucd_generator.py "My Playbook.yml" \
  --customer "E CORP" \
  --ps "Seif Abdelwhaid"
```

**Auto-discover sub-playbooks from the same folder:**
```bash
python ucd_generator.py "My Playbook.yml" --auto-subs \
  --customer "E CORP" \
  --ps "Seif Abdelwhaid"
```

**Point to a dedicated sub-playbooks folder:**
```bash
python ucd_generator.py "My Playbook.yml" \
  --subs "./sub-playbooks/" \
  --customer "E CORP" \
  --ps "Seif Abdelwhaid"
```

**Specify a custom output path:**
```bash
python ucd_generator.py "My Playbook.yml" \
  --out "./output/Acme_AsBuilt_v1.docx" \
  --customer "E CORP" \
  --ps "Seif Abdelwhaid"
```

---

## 📁 Output Structure

The generated `.docx` includes:

1. **Cover / Title** — Document title with customer name
2. **Main Playbook Flow** — Full task table for the main playbook
3. **Sub-Playbooks Details** — Individual flow tables for each discovered sub-playbook
4. **Document Control** — Auto-filled metadata (date, author, version)

Each flow table contains four columns:

| Condition / Task Name | Automation Action | Manual Action / Escalation | Next Step |
|---|---|---|---|
| Task display name | Script, command, or sub-playbook | Manual instructions if applicable | Branching paths |

Task types are **color-coded** for instant readability:
- 🔵 **Blue** — Automation commands
- 🟠 **Orange** — Sub-playbook calls
- 🟢 **Green** — Conditional tasks
- ⬜ **Plain** — Manual / standard tasks

---

## 🗂 Project Structure

```
xsoar-as-built-generator/
├── ucd_generator.py     # Main script
├── requirements.txt     # Python dependencies
└── README.md            # You're reading it
```

---

## 🤝 Contributing

Contributions are welcome! Feel free to open an issue or submit a pull request for:
- New task type support
- Additional styling options
- Bug fixes or edge cases in YAML parsing

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

Built by a PS consultant, for PS consultants.  
If this saves you time on an engagement, give it a ⭐ on GitHub!
