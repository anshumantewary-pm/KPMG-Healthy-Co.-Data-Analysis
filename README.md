# KPMG Healthy Co. – Patient Flow Data Analysis

An Excel-based case study of patient flow at a healthcare clinic ("Healthy Co."). The workbook records how long each patient spends at every stage of a visit, from check-in to payment, along with the staff involved. The analysis looks at where patients wait, how waiting time compares with time spent with a doctor, and where bottlenecks and data-quality problems show up.

## Dataset

File: [`KPMG Healthy Co Raw Data.xlsx`](KPMG%20Healthy%20Co%20Raw%20Data.xlsx), sheet `Raw data`

- 5,007 rows, one per patient visit (`Unique ID`)
- 12 fields:

| Field | Description |
|---|---|
| `Unique ID` | Patient visit identifier |
| `Arrival (Hour of day, GMT)` | Hour the patient arrived |
| `Check-in (mins)` | Time taken at check-in |
| `Wait for vitals (mins)` | Wait before vitals were taken |
| `Vitals (mins)` | Time taken for vitals |
| `Wait for doctor (mins)` | Wait before seeing the doctor |
| `Doctor visit (mins)` | Length of the consultation |
| `Payment (mins)` | Time taken at payment |
| `Diagnosis group` | Group 1, Group 2 or Group 3 |
| `Admin (check-in)` | Admin staff member who checked the patient in |
| `Nurse (vitals)` | Nurse who took vitals |
| `Doctor` | Attending doctor (5 doctors in the data) |

**Data-quality note:** the last row (ID `999924`) holds the text `Dr. Yung` in every field, including the numeric time columns. It is a placeholder or entry error and should be left out of any calculation.

## Approach

1. **Data review and cleaning.** Checked the columns for consistency and flagged invalid entries, such as text in numeric time fields.
2. **Process breakdown.** Split each visit into its stages (check-in, wait for vitals, vitals, wait for doctor, doctor visit, payment) to see where the time goes.
3. **Exploration with Excel tools.** Used sorting, filtering and formulas to compare stages, diagnosis groups and staff.
4. **Visualisation.** The workbook includes two charts:
   - a scatter plot of **Wait for vitals (mins)** across all visits
   - a line chart, **"Comparison Wait For Doctor Vs Doctor Visit"**, plotting each patient's wait for the doctor against the length of their consultation

## What the analysis covers

- How waiting time (for vitals and for the doctor) compares with actual service time
- Whether long waits for the doctor go with short consultations
- How patient load is spread across diagnosis groups, doctors, nurses and admin staff
- Data-quality issues to fix before any operational recommendation is made

## Tools & Tech

- Microsoft Excel (formulas, sorting and filtering, charts)

## Repository Structure

```
.
├── KPMG Healthy Co Raw Data.xlsx   # Patient-flow dataset with analysis charts
└── README.md
```

## How to Open

1. Clone or download the repository:
   ```bash
   git clone https://github.com/anshumantewary-pm/KPMG-Healthy-Co.-Data-Analysis.git
   ```
2. Open `KPMG Healthy Co Raw Data.xlsx` in Microsoft Excel. Google Sheets and LibreOffice Calc also work, though the charts may look slightly different.
3. The charts sit to the right of the data on the `Raw data` sheet.

---

**Author:** Anshuman Tewary · [GitHub](https://github.com/anshumantewary-pm) · [LinkedIn](https://www.linkedin.com/in/tewary-anshuman/)
