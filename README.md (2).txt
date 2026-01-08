# 🧾 Invoice Automation System

### 📊 Overview
The **Invoice Automation System** is a Python-based tool designed to simplify payment processing for freelance writing and bidding accounts.  
It automatically cleans, combines, and analyzes multiple Excel sheets from different account sources (e.g., *Titania*, *Flora*, *Alyssa*, *Beryl*, and *Magdalene*) to generate structured payment summaries and bidder invoices.

---

### 🧠 Project Motivation
Manual invoice preparation for each bidder and writer was time-consuming and error-prone.  
This system automates the process — turning messy order records into clear, downloadable Excel invoices with totals per bidder, writer, and account.

---

### ⚙️ Key Features
- Automatically reads and combines multiple Excel sheets
- Cleans and standardizes dates, pay, and fine columns
- Detects duplicate orders using an automated flag
- Generates separate **invoice sheets per bidder**
- Creates a **summary sheet** with total writer pay, bidder pay, and owner share
- Exports results as an Excel file for easy review or sharing

---

### 🧰 Technologies Used
| Tool | Purpose |
|------|----------|
| **Python (Pandas, NumPy)** | Data cleaning, transformation, and summarization |
| **ExcelWriter (xlsxwriter)** | Automated Excel report and invoice generation |
| **Jupyter Notebook** | Code execution and project documentation |
| **Matplotlib** | Data visualization and analytics |

---

### 📁 Project Structure

```
invoice-automation-system/
│
├── invoice_automation.ipynb    # Main Jupyter Notebook
├── README.md                    # Project documentation
├── requirements.txt             # Python dependencies
├── data/                        # Input Excel files (not tracked)
├── output/                      # Generated invoices (not tracked)
└── .gitignore                   # Git ignore file
```

---

### 🚀 How to Run the Project

#### Prerequisites

Make sure you have Python 3.x installed. Then install the required packages:

```bash
pip install pandas numpy matplotlib xlsxwriter openpyxl jupyter
```

Or use the requirements file:

```bash
pip install -r requirements.txt
```

#### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/bonifacekimanga/invoice-automation-system.git
   cd invoice-automation-system
   ```

2. **Prepare your data**
   - Place your Excel files in the project directory
   - Ensure each Excel file contains sheets named: Titania, Flora, Alyssa, Beryl, Magdalene
   - Each sheet should have columns: Order Number, Date Bid, Bidder, Number of Pages, Pay, Fine, Status

3. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook invoice_automation.ipynb
   ```

4. **Run all cells**
   - Execute cells sequentially or use "Run All"
   - The system will process all data and generate the output file

5. **Check output**
   - Look for the generated Excel file in the output folder
   - Each sheet represents a bidder's invoice with complete payment details

---

### 📊 Example Output

The system generates an Excel workbook with detailed payment records. Here's a sample of the output structure:

| Order Number | Date Bid | Bidder | Source_Sheet | Number of Pages | Bidder Pay (KES) | Fine ($) | Paid Status | DUPLICATE_FLAG | Fine (KES) | Net Payable (KES) |
|--------------|----------|--------|--------------|-----------------|------------------|----------|-------------|----------------|------------|-------------------|
| 7592280 | 2025-12-06 | xxxx | xxxx | 3 | 195 | | 0 | FALSE | 0 | 195 |
| 7593076 | 2025-12-07 | xxxx | xxxx | 3 | 195 | | 0 | FALSE | 0 | 195 |

Each bidder's invoice includes:
- **Order tracking**: Complete order number and date
- **Source identification**: Which account the order came from
- **Page count**: Total pages completed
- **Payment calculation**: Base pay, fines, and net payable amount
- **Duplicate detection**: Automatic flagging to prevent double payments
- **Currency handling**: Fine conversion from USD to KES

---

### 💡 Key Technical Highlights

- **Data Integration**: Combines multiple Excel sheets into a unified dataset
- **Data Cleaning**: Handles missing values, standardizes formats, and validates data types
- **Duplicate Detection**: Implements automated flagging to ensure payment accuracy
- **Currency Conversion**: Manages fines in both USD and KES
- **Scalability**: Easily handles growing numbers of accounts and bidders

---

### 🔮 Future Enhancements

- [ ] Add PDF invoice generation
- [ ] Implement email automation for invoice delivery
- [ ] Create interactive dashboard for real-time analytics
- [ ] Add support for multiple currencies with live exchange rates
- [ ] Integrate payment tracking and confirmation system
- [ ] Build web interface for easier access

---

### 📝 Data Privacy

This repository does not include actual client data files to protect privacy. Sample data structures are provided for demonstration purposes only.

---

### 👨‍💻 Author

**Boniface Kimanga**  
Data Analyst

- 🐙 GitHub: [@bonifacekimanga](https://github.com/bonifacekimanga)
- 📧 Email: kimangaboniface79@gmail.com
- 💼 LinkedIn: [Connect with me](https://www.linkedin.com/in/bonifacekimanga)

---
### 📄 License
MIT License

Copyright (c) 2025 Boniface Kimanga

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation for educational and portfolio purposes.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND.
---

### 🙏 Acknowledgments

Built as part of my journey in data analysis and automation, demonstrating skills in:
- Data processing and cleaning
- Business logic implementation
- Workflow automation
- Financial reporting systems

---

*If you find this project helpful or interesting, please consider giving it a star ⭐*

---

