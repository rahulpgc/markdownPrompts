Generate a complete Google Apps Script (GAS) project, designed to be developed in VS Code and deployed as a container-bound script to a Google Sheet. This project will process data from input tabs in the Sheet, perform calculations, and output the results to a separate output tab.

**General Project Requirements (Always Apply):**

- **Container-Bound:** The script must be bound to a Google Sheet.
- **Input/Output Tabs:** The Google Sheet will have distinct tabs for data input and data output.
- **Output Tab Format:** The output tab will present data in a standard, well-formatted table. I will specify the exact layout and columns in the project-specific section below. There will usually be only one output tab.
- **Input Tab Format:** Data in the input tabs will be organized either in _horizontal rows_ or _vertical columns_. Each row/column (excluding the header row/column) will represent a single data record. I will specify whether rows or columns are used in the project-specific section.
- **Header Exclusion:** Data calculations must exclude the first row (if data is in rows) or the first column (if data is in columns) as these will contain headers.
- **Coding Standards:**
  - The code must be thoroughly annotated and commented, adhering to modern JavaScript and Google Apps Script best practices.
  - All function declarations MUST include JSDoc-style comments with:
    - A one-line description of the function's purpose.
    - `@param` tags for each argument, specifying the data type and a description.
    - `@return` tag(s) specifying the data type(s) of the return value(s).
- **Project Structure:**
  - All JavaScript code must reside within a `src/` folder.
  - The primary JavaScript file must be named `src/main.js`.
  - Consider using a `src/helpers/` subfolder and additional `.js` files within it to improve code organization and maintainability. Determine if this is necessary based on the complexity of the project-specific calculations. If used, clearly document the purpose of each helper file.
- **README.md:** Generate a comprehensive `README.md` file targeted at developers. This file MUST include:
  - A clear explanation of the script's overall functionality.
  - Instructions on how to create the bound Google Sheet and the GAS project.
  - A list of project dependencies.
  - A description of the project's folder structure.
  - Descriptions of each file within the project.
  - Step-by-step instructions for the initial VS Code, GitHub, and Clasp setup (assume the developer has `npm` and `clasp` installed globally).
  - Step-by-step workflow instructions explaining how to keep VS Code, GitHub, and the GAS project synchronized during development.
  - A summary of essential Git and Clasp commands with concise descriptions.
- **CHANGELOG:** Generate a `CHANGELOG` file.
- **Boilerplate Files:** Include all necessary boilerplate files for a modern GAS project, including but not limited to:
  - `.clasp.json`
  - `.claspignore`
  - `.gitignore`
  - `appsscript.json`
  - `package.json`
  - `package-lock.json`
    Ensure that all these files are correctly configured.

**Project-Specific Requirements (Modify This Section For Each Project):**

- **Input Tab Name(s):** [Provide the name(s) of the input tab(s) here. Example: `"Sheet1"` or `"Input Data", "More Input"`]
- **Input Data Orientation:** [Specify whether input data records are arranged in `rows` or `columns`.]
- **Output Tab Name:** [Provide the name of the output tab. Example: `"Results"`]
- **Output Tab Layout:** [Describe the desired layout of the output table. Be specific about the columns, their headers, and the data they should contain. Example: `"The output tab should have three columns: 'Customer Name' (text), 'Total Purchases' (number), and 'Average Purchase Value' (number)."`]
- **Data Calculations:** [Provide a _detailed_ description of the calculations to be performed. Be extremely precise. Use plain language, mathematical notation, or pseudocode. This is the most critical part to get right. Example:
  `"For each customer (represented by a row in the 'Input Data' tab), calculate the following:
  1. Total Purchases: Sum all the values in columns B through F.
  2. Average Purchase Value: Divide the 'Total Purchases' by the number of non-empty cells in columns B through F."`]
- **Google Sheet Name**: [Provide a suitable name for the Google Sheet so that you can build the project's appscript.json file]

**Output:**

I expect the complete project structure, including all necessary files and folders, with well-commented code that fulfills both the general and project-specific requirements. The code should be ready to be cloned, `clasp login`, `clasp pull` and deployed to a Google Sheet.
