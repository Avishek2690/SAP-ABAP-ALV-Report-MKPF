<!--# SAP-ABAP-ALV-Report-MKPF
SAP ABAP ALV Report project using the MKPF table to display Material Document information through an interactive ALV Grid with field catalog customization, event handling, and report formatting.-->
# SAP ABAP ALV Report using MKPF Table

## Project Information

| Attribute        | Details                        |
| ---------------- | ------------------------------ |
| Project Name     | SAP ABAP ALV Report using MKPF |
| Project Type     | SAP ABAP Mini Project          |
| Module           | SAP ABAP                       |
| Report Type      | Classical ALV Grid Report      |
| Table Used       | MKPF                           |
| Development Tool | SAP ABAP Workbench             |
| ALV Type         | REUSE_ALV_GRID_DISPLAY         |

---

## Project Overview

This project demonstrates the development of a Classical ALV (ABAP List Viewer) Report using the MKPF (Material Document Header) table.

The report retrieves and displays Material Document information in an interactive ALV Grid format, allowing users to efficiently view and analyze material document data. Field catalog customization, report formatting, hotspot functionality, and ALV event handling have been implemented to enhance the presentation and usability of the report.

---

## Business Scenario

Material Documents are generated during various inventory management processes such as goods receipt, goods issue, and transfer postings.

Business users often require quick access to Material Document information for monitoring, auditing, and reporting purposes.

This ALV Report provides a structured and user-friendly interface to display Material Document details retrieved from the MKPF table.

---

## Objective

The objective of this project was to:

* Retrieve Material Document data from the MKPF table.
* Display the data using ALV Grid.
* Implement a selection screen for user input.
* Customize ALV output using Field Catalog.
* Apply formatting and hotspot functionality.
* Implement TOP-OF-PAGE event handling.
* Improve report readability and user experience.

---

## Technical Implementation

### Step 1: Selection Screen

A selection screen was created using SELECT-OPTIONS to allow users to enter one or more Material Document Numbers.

```abap
SELECT-OPTIONS: so_mblnr FOR mkpf-mblnr.
```

---

### Step 2: Data Retrieval

Material Document information is retrieved from the MKPF table based on the user-selected document numbers.

#### Fields Retrieved

| Field | Description              |
| ----- | ------------------------ |
| MBLNR | Material Document Number |
| BLART | Document Type            |
| USNAM | User Name                |
| VGART | Transaction/Event Type   |

---

### Step 3: Field Catalog Configuration

Field Catalog entries were configured to:

* Define column headings
* Highlight important fields
* Apply ALV formatting
* Enable hotspot functionality

The Material Document Number field was configured as a hotspot for improved user interaction.

---

### Step 4: ALV Event Handling

The TOP-OF-PAGE event was implemented to display a custom report header.

```abap
wa_alv_events-name = 'TOP_OF_PAGE'.
wa_alv_events-form = 'HEADING'.
```

---

### Step 5: ALV Grid Display

The report output is displayed using the standard SAP function module:

```abap
REUSE_ALV_GRID_DISPLAY
```

This provides:

* Sorting
* Filtering
* Layout customization
* Column resizing
* Interactive data viewing

---

## Table Used

| Table | Description                   |
| ----- | ----------------------------- |
| MKPF  | Material Document Header Data |

---

## Technologies Used

* SAP ABAP
* ALV Grid Display
* REUSE_ALV_GRID_DISPLAY
* SAP Data Dictionary (DDIC)
* Internal Tables
* Work Areas
* Selection Screen Programming
* ALV Events
* Field Catalog

---

## Skills Demonstrated

* SAP ABAP Report Development
* ALV Report Development
* Internal Table Processing
* Data Retrieval using Open SQL
* Field Catalog Configuration
* ALV Event Handling
* Selection Screen Design
* SAP Data Presentation Techniques

---

## Business Benefits

* Provides quick access to Material Document information.
* Improves report readability through ALV formatting.
* Enables efficient data filtering and sorting.
* Reduces manual effort in document analysis.
* Enhances user productivity through interactive reporting.

---

## Project Architecture

```text
                 User Input

                       │
                       ▼

            Selection Screen
             (SO_MBLNR)

                       │
                       ▼

                 MKPF Table
          (Material Document Header)

                       │
                       ▼

               Data Retrieval
                (Open SQL)

                       │
                       ▼

              Internal Table
                (IT_MKPF)

                       │
                       ▼

          Field Catalog Creation

                       │
                       ▼

             ALV Event Handling
               (TOP_OF_PAGE)

                       │
                       ▼

         REUSE_ALV_GRID_DISPLAY

                       │
                       ▼

               ALV Grid Output
```

---

## Screenshots

### ABAP Program

```markdown
[ABAP Program](screenshots/code.png)
```

---

### Selection Screen

```markdown
[Selection Screen](screenshots/selection-screen.png)
```

---

### ALV Report Output

```markdown
[ALV Output](screenshots/output.png)
```

---

## Key Learnings

Through this project, I gained practical experience in:

* Classical ALV Report Development
* REUSE_ALV_GRID_DISPLAY Function Module
* Open SQL Data Retrieval
* Internal Tables and Work Areas
* Field Catalog Customization
* Selection Screen Programming
* ALV Event Handling
* SAP Reporting Techniques

---

## Future Enhancements

* Add Drill-Down Functionality
* Implement Custom Toolbar Buttons
* Enable Excel Export
* Add User Command Events
* Integrate Additional Material Management Tables
* Develop Interactive ALV Features

---

## Outcome

Successfully developed a Classical ALV Report using the MKPF table to display Material Document information in an organized and interactive format.

The project demonstrates practical implementation of SAP ABAP reporting concepts, ALV Grid functionality, event handling, and report customization techniques.

---

## Author

**Avishek Chourasiya**

SAP ABAP Developer Intern | Computer Science Student

LinkedIn:
linkedin.com/in/avishek-chourasiya

