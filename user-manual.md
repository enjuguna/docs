# Inverter Settings Checker – User Manual

Welcome to the Inverter Settings Checker desktop application. This guide provides a comprehensive walkthrough of all features, screens, and workflows to help you get the most out of the app.

---

## Table of Contents

1. [Introduction](#introduction)
2. [General Usage](#general-usage)
3. [Inverters Tab](#inverters-tab)
4. [Models Tab](#models-tab)
5. [Verification Tab](#verification-tab)
6. [Tests Tab](#tests-tab)
7. [Logs Tab](#logs-tab)
8. [Menu Bar Features](#menu-bar-features)
9. [Screenshot Guidance](#screenshot-guidance)
10. [Troubleshooting & Tips](#troubleshooting--tips)

---

## Introduction

The Inverter Settings Checker is a modern desktop application for managing inverter devices, models, verification results, and logs. It is designed for professional inverter management and Modbus communication, with a focus on usability and reliability.

**Key Features:**
- Tabbed interface for easy navigation
- CSV-based data storage for inverters, models, and results
- Real-time log viewer and filtering
- Export and verification tools for results
- Modern, responsive UI

---

## General Usage

### Launching the Application

- Double-click the executable file to start the app.
- The main window will open, displaying a tabbed interface at the top.

### Navigating the Interface

- Tabs: Inverters, Models, Verification, Tests, Logs.
- Click a tab to switch to its section.
- The menu bar at the top provides Help and About options.

### Data Storage

- All data is stored in CSV files for easy backup and integration.
- Inverter data: `inverters/inverters.csv`
- Model data: `models/`
- Results: `results/`
- Logs: `app.log`

---

## Inverters Tab

This tab allows you to manage all inverter devices in your system.

### Overview

- **Table View:** Displays all inverters with columns for ID, Name, IP Address, Port, Model, and Addressing Type.
- **Form Panel:** Add or edit inverter details.
- **Action Buttons:** Add, Modify, Delete.

### Step-by-Step Guide

1. **Viewing Inverters**
   - All inverters are listed in a table.
   - Columns:  
     - **ID:** Unique identifier (auto-generated).
     - **Inverter Name:** Descriptive name (auto-generated, editable in CSV).
     - **IP Address:** Network address (e.g., `192.168.100.1`).
     - **Port:** Communication port (e.g., `502`).
     - **Model:** Select from available models (e.g., `SG4400`).
     - **One Based Addressing:** Choose `true` or `false`.

2. **Adding an Inverter**
   - Fill in the IP Address, Port, Model, and Addressing Type.
   - Click **Add**.
   - The new inverter appears in the table and is saved to `inverters/inverters.csv`.

3. **Editing an Inverter**
   - Select a row in the table.
   - The form is populated with the inverter's details.
   - Modify the fields as needed.
   - Click **Modify** to save changes.

4. **Deleting an Inverter**
   - Select a row in the table.
   - Click **Delete** to remove the inverter.

5. **Sorting and Filtering**
   - Click column headers to sort.
   - Use the search/filter features (if available) to find specific inverters.

**Screenshot Placeholder:**  
*Insert screenshot of the Inverters tab showing the table and form panel.*

**Notes:**
- All changes are saved automatically to the CSV file.
- If you encounter errors (e.g., invalid IP address), check your input and try again.

---

## Models Tab

Manage inverter models and their register settings.

### Overview

- **Model List:** Displays all available models (CSV files).
- **Settings Table:** Shows register settings for the selected model.
- **Management Panel:** Add, modify, or delete models and settings.

### Step-by-Step Guide

1. **Viewing Models**
   - The left panel lists all models.
   - Select a model to view its settings in the table.

2. **Adding a Model**
   - Enter a new model name (must end with `.csv`).
   - Click **Add Model**.
   - The new model appears in the list and is created in the `models/` directory.

3. **Deleting a Model**
   - Select a model from the list.
   - Click **Delete Model** to remove it.

4. **Viewing and Editing Settings**
   - The settings table displays register settings for the selected model.
   - Columns may include: `slave_id`, `register_type`, `register_address`, `data_type`, `scale`, `byte_order`, `units`, etc.

5. **Adding a Setting**
   - Click **Add Setting**.
   - Fill in the required fields (data type, byte order, etc.).
   - Click **OK** to save.

6. **Modifying a Setting**
   - Select a row in the settings table.
   - Click **Modify Setting**.
   - Edit the fields and click **OK**.

7. **Deleting a Setting**
   - Select a row in the settings table.
   - Click **Delete Setting**.

**Screenshot Placeholder:**  
*Insert screenshot of the Models tab showing the model list and settings table.*

**Notes:**
- All changes are saved to the model's CSV file.
- Use consistent naming for models and settings for easier management.

---

## Verification Tab

View, filter, and export verification results.

### Overview

- **Results File Selector:** Choose a CSV file to view results.
- **Results Table:** Displays verification data.
- **Device Filter:** Focus on specific devices.
- **Export/Verify Panel:** Export results or check for missing values.

### Step-by-Step Guide

1. **Viewing Results**
   - Select a results file from the dropdown.
   - The table displays all verification entries.

2. **Filtering by Device**
   - Use the device dropdown to show results for a specific inverter/device.

3. **Exporting Results**
   - Click **Export Results** to save the currently visible rows to `results/exported_results.csv`.

4. **Verifying Results**
   - Click **Verify Results** to check for missing or empty values.
   - A dialog will report any issues found.

5. **Understanding Table Columns**
   - Common columns: `Date Time`, `Inverter`, `Register Address`, `Data Type`, `Description`, `Scaling`, `Actual Value`, `Units`, `Correct Settings`.

**Screenshot Placeholder:**  
*Insert screenshot of the Verification tab showing the results table and export/verify panel.*

**Notes:**
- Only visible rows are exported.
- Verification helps ensure data completeness before reporting.

---

## Tests Tab

Configure and test Modbus registers for inverters.

### Overview

- **Test Results Table:** Shows all register tests.
- **Register Configuration Panel:** Add new tests.
- **Action Buttons:** Add, Modify, Delete, Test.

### Step-by-Step Guide

1. **Adding a Register Test**
   - Fill in the model, IP address, port, register type, register number, data type, and units.
   - For string data types, specify the number of bytes.
   - Click **Add** to create a new test entry.

2. **Modifying a Register Test**
   - Select a row in the table.
   - Click **Modify** to edit the details.

3. **Deleting a Register Test**
   - Select a row in the table.
   - Click **Delete** to remove the entry.

4. **Testing a Register**
   - Select a row and click **Test**.
   - The app will attempt to fetch the actual value from the device.
   - If unreachable, "N/A" is shown.

5. **Understanding Table Columns**
   - Columns: `Date Time`, `Inverter`, `Register Address`, `Data Type`, `Description`, `Scaling`, `Actual Value`, `Units`, `Correct Settings`.

**Screenshot Placeholder:**  
*Insert screenshot of the Tests tab showing the test results table and configuration panel.*

**Notes:**
- Ensure device connectivity for successful register tests.
- Use correct data types and register numbers for accurate results.

---

## Logs Tab

Monitor and manage application logs.

### Overview

- **Log Viewer:** Displays logs from `app.log`.
- **Filter Dropdown:** Select log severity (All, Info, Warning, Error).
- **Action Buttons:** Refresh Logs, Clear Logs.

### Step-by-Step Guide

1. **Viewing Logs**
   - Logs are displayed in real time.
   - Color coding helps distinguish severity levels.

2. **Filtering Logs**
   - Use the dropdown to filter by Info, Warning, or Error.

3. **Refreshing Logs**
   - Click **Refresh Logs** to reload the log file.

4. **Clearing Logs**
   - Click **Clear Logs** to remove all entries.
   - A confirmation message will appear.

**Screenshot Placeholder:**  
*Insert screenshot of the Logs tab showing the log viewer and controls.*

**Notes:**
- Logs help diagnose issues and monitor system activity.
- Clearing logs does not affect application data.

---

## Menu Bar Features

### Help Menu

- Access documentation and Modbus resources.
- Click **Help > Documentation** to open online resources.

### About Dialog

- View information about the application, version, and purpose.
- Click **Help > About Inverter Settings Checker** for details.

**Screenshot Placeholder:**  
*Insert screenshot of the menu bar and About dialog.*

---

## Screenshot Guidance

- Add screenshots at each indicated location for visual reference.
- Screenshots should clearly show the UI, controls, and typical workflows.
- Use annotations to highlight important buttons or fields.

---

## Troubleshooting & Tips

### Common Issues

- **App does not start:**  
  Ensure all dependencies (Qt, Go) are installed. Check for missing files.

- **Cannot add inverter/model:**  
  Verify all required fields are filled and valid.

- **Register test shows "N/A":**  
  Check device connectivity and register details.

- **Logs not updating:**  
  Ensure the app has permission to write to `app.log`.

### Tips

- Regularly export and back up your CSV files.
- Use descriptive names for inverters and models.
- Consult the Help menu for additional resources.

---

## Support

For further assistance, consult the Help menu or contact your system administrator.