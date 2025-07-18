# Tariff Calculator
A Python-based tool that parses commercial invoices (PDF format) and calculates estimated:

  -  Tariff based on HS Code and Country of Origin

  -  Merchandise Processing Fee (Service Fee) (0.3464%)

  -  Total Entry Cost (Tariff + Service Fee)


Output
Excel file with:

*Tariff % per item

*Calculated tariff amount

*Total summary section highlighted in yellow


## Example output format:

============================================================
     🚢  TARIFF CALCULATION SUMMARY  📦     
============================================================
🔶 Total Tariff :   $2,288.64
🔷 Service Fee  :   $448.46
🟩 Entry Fee    :   $2,737.10
============================================================

📄 Tariff Breakdown Table (top items):

| Item                     | Amount | Origin | HS Code | Tariff % | Tariff Amount |
|--------------------------|--------|--------|---------|----------|----------------|
| Ant-RP_SMAM-WiFi-196MM1  | 210    | TAIWAN | 852910  | 10.0%    | $21.00         |
| SSD-1TB-TLC5WT-TD        | 1176   | TAIWAN | 847330  | 0.0%     | $0.00          |
| PA-600W-ENC              | 1188   | CHINA  | 850440  | 55.0%    | $653.40        |
