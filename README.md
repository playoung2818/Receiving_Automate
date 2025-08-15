# Receiving Process Automation

My daily receiving process comes with three steps: **Calculating tariff**, **recording receipts**, and **creating the incoming form**. This script automates most parts of this workflow

---

## Workflow Overview

1. **Parse the invoice**  
   Extract product numbers, quantities, and prices from the invoice section. Tariff, service fees, and total charges are calculated automatically.

2. **Parse the packing list**  
   Identify box numbers and product numbers. Each item is expanded based on quantity, unless its part number starts with specific prefixes (e.g., `Cbl`, `DIN`, `AccsyBx`, `Gpubr`, `Ant`, `FK`), in which case the row is kept as-is.

3. **Generate output files**
   - `Receiving Log.xlsx`: structured file used during physical receiving
   - `Incoming Form.docx`: formal Word document based on the receiving log, suitable for internal filing or sign-off
   - `Tariff Summary.xlsx` (optional): includes cost breakdown if tariff data is present in the invoice
  
4. **Upload Receving_Log to DB**

---

## Input

- `invoice.pdf` —include both invoice and packing list sections

---

## Output

- `Receiving Log.xlsx` — includes `Box #`, `POD#`, `Part#`, `SN#`, and `Qty`
- `Incoming Form.docx` — formatted Word document used as the official receiving record
- `Tariff Summary.xlsx` — optional breakdown of duties and fees
  
<img width="555" height="326" alt="image" src="https://github.com/user-attachments/assets/223f8205-f2f2-404d-9120-790624e74353" />

---

## Notes

- The script assumes files are processed in order of last modified time
- Serial numbers (`SN#`) are left blank for manual entry or future automation
- You can customize expansion rules (e.g., which prefixes to skip)

---
