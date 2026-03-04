# Google Sheets Apps Script Automation

Professional **Google Apps Script (JavaScript)** code for **Google Sheets automation, dashboards, and custom formulas**.

This repository contains examples and utilities for building powerful **data dashboards, automation workflows, and custom spreadsheet functions** using Google Apps Script.

---

## Features

✔ Dashboard automation
✔ Custom spreadsheet formulas
✔ Data processing scripts
✔ Automated reports
✔ Email notifications
✔ Trigger-based workflows
✔ Google Sheets performance optimization

---

## Technologies Used

* JavaScript
* Google Apps Script
* Google Sheets Automation
* Spreadsheet APIs

---

## Example Use Cases

### 1. Dashboard Automation

Automatically update key metrics and summary data in a dashboard.

### 2. Custom Spreadsheet Functions

Create reusable formulas directly inside Google Sheets.

Example:

```javascript
function MULTIPLYBY10(value) {
  return value * 10;
}
```

Usage in Google Sheets:

```
=MULTIPLYBY10(A1)
```

---

### 3. Automated Data Processing

Example script:

```javascript
function updateDashboard() {
  var ss = SpreadsheetApp.getActiveSpreadsheet();
  var dataSheet = ss.getSheetByName("Data");
  var dashSheet = ss.getSheetByName("Dashboard");

  var values = dataSheet.getRange("B2:B100").getValues();

  var total = 0;

  for (var i = 0; i < values.length; i++) {
    total += values[i][0];
  }

  dashSheet.getRange("B2").setValue(total);
}
```

---

## Automation Triggers

Apps Script supports automatic triggers:

* On edit
* Time-based schedules
* Form submissions
* Spreadsheet updates

Example trigger:

```javascript
function createTrigger() {
  ScriptApp.newTrigger("updateDashboard")
  .timeBased()
  .everyDays(1)
  .create();
}
```

---

## Project Goals

* Simplify Google Sheets automation
* Build scalable dashboards
* Improve productivity with scripting
* Provide reusable Apps Script solutions

---

## Author

Amlesh

---

## License

This project is open-source and available for learning and development.
