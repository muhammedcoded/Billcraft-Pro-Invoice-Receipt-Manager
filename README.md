# Billcraft Pro | Invoice & Receipt Manager

A modern, responsive, and browser-based **Invoice and Receipt Management Application** built with **HTML, CSS, and JavaScript**.

Billcraft Pro helps individuals, freelancers, and small businesses create professional invoices, issue payment receipts, manage customers, track payments, and monitor outstanding balances from one dashboard.

The application works entirely in your browser without requiring a backend, database, account registration, or API key.

## Features

### Business Dashboard

- View total invoiced amounts
- Track payments received
- Monitor outstanding balances
- Identify overdue invoices
- Access recent business activity

### Invoice Management

- Create, edit, and manage invoices
- Generate custom invoice numbers
- Add multiple products or services
- Automatically calculate subtotals, discounts, taxes, and additional fees
- Set invoice issue dates and payment deadlines
- Track paid, partially paid, unpaid, and overdue invoices
- Preview invoices before printing
- Export professional invoices as PDF documents

### Receipt Management

- Create professional payment receipts
- Generate standalone receipts
- Link receipts to existing invoices
- Record full and partial payments
- Add payment methods and transaction references
- Automatically update invoice balances when payments are recorded
- Preview, print, and export receipts as PDFs

### Customer Management

- Add and manage customer records
- Save customer names, email addresses, and phone numbers
- Store billing addresses
- Reuse customer information when generating invoices

### Business Settings

- Customize company name and contact information
- Add business addresses and bank details
- Configure payment instructions
- Set a preferred currency
- Export and restore application data using JSON backups

### Additional Features

- Responsive design for desktop, tablet, and mobile
- Automatic data persistence using Local Storage
- Live invoice and receipt previews
- Print-friendly A4 document layouts
- No installation or registration required
- No backend or external database required

## Supported Currencies

Billcraft Pro supports the following currencies:

| Currency | Code |
|---|---|
| US Dollar | USD |
| Nigerian Naira | NGN |
| British Pound | GBP |
| Euro | EUR |
| Canadian Dollar | CAD |
| Indian Rupee | INR |
| Australian Dollar | AUD |

**Note:** Currency selection changes how amounts are displayed. It does not perform currency conversion.

## Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Responsive styling and interface design |
| JavaScript | Application functionality and calculations |
| Local Storage | Saving business records locally |
| JSON | Data backup and restoration |
| Browser Print API | Printing and PDF export |
| Node.js | Optional automated testing |

## Installation and Setup in VS Code

### Step 1: Download the Project

1. Click the green **Code** button on this GitHub repository.
2. Select **Download ZIP**.
3. Extract the downloaded ZIP file.
4. Open Visual Studio Code.
5. Select **File > Open Folder**.
6. Choose the extracted `billcraft-pro` folder.

### Step 2: Run the Application

No installation is required.

1. Open the project folder.
2. Locate `index.html`.
3. Double-click the file to open it in your browser.
4. The Invoice & Receipt Manager is ready to use.

You do not need Python, Node.js, or a backend server.

### Alternative: Run Using Live Server

1. Open Visual Studio Code.
2. Navigate to the Extensions panel.
3. Search for **Live Server** by Ritwick Dey.
4. Install the extension.
5. Open `index.html`.
6. Right-click and select **Open with Live Server**.

The application will typically open at:

`http://127.0.0.1:5500`

## How to Use

### 1. Configure Your Business

1. Open the application.
2. Navigate to **Settings**.
3. Enter your business name, address, and contact details.
4. Choose your preferred currency.
5. Enter your payment instructions and bank details.
6. Click **Save settings**.

### 2. Add Customers

1. Open the **Clients** tab.
2. Add a new customer.
3. Enter the customer's name, email address, phone number, and billing address.
4. Save the customer information for future invoices.

### 3. Create an Invoice

1. Open the **Invoices** tab.
2. Click **New invoice**.
3. Select an existing customer or enter billing details.
4. Enter the invoice number, issue date, and due date.
5. Add the products or services being billed.
6. Specify quantities, prices, discounts, and applicable taxes.
7. Review the calculated total.
8. Save the invoice.

### 4. Export an Invoice as PDF

1. Open a saved invoice.
2. Click **View**.
3. Select **Print / Save PDF**.
4. Choose **Save as PDF** in your browser's print dialog.
5. Save the document to your computer.

For cleaner output, disable browser headers and footers in the print settings.

### 5. Create a Payment Receipt

1. Open the **Receipts** tab.
2. Create a new receipt.
3. Enter the payment amount, date, method, and transaction reference.
4. Optionally link the receipt to an existing invoice.
5. Save the receipt.
6. Preview or export the receipt as a PDF.

When a receipt is linked to an invoice, the recorded payment automatically reduces the invoice's outstanding balance.

### 6. Monitor Business Transactions

Open the **Overview** dashboard to view:

- Total invoice amounts
- Total payments received
- Outstanding balances
- Overdue invoices
- Recent business activity

### 7. Export and Restore Data

Billcraft Pro stores records locally in your browser.

To back up your information:

1. Navigate to **Settings**.
2. Click **Export backup**.
3. Save the generated JSON file.

To restore your information, use the application's backup import option and select your previously exported JSON file.

## Project Structure

```text
billcraft-pro/
├── index.html
├── assets/
│   ├── app.js
│   ├── core.js
│   └── styles.css
├── tests/
│   └── core.test.cjs
├── .gitignore
├── LICENSE
└── README.md
```

### File Descriptions

- **index.html:** Contains the main application interface and navigation.
- **assets/app.js:** Handles user interactions, invoice and receipt management, local storage, and document printing.
- **assets/core.js:** Contains calculations, validation, and business logic.
- **assets/styles.css:** Controls styling, responsiveness, and print layouts.
- **tests/core.test.cjs:** Automated tests for core application functionality.
- **.gitignore:** Excludes unnecessary development files.
- **LICENSE:** Contains the MIT License.

## Running Automated Tests

Node.js version 18 or newer is required only for automated testing.

Open the VS Code terminal and execute:

```bash
node --test tests/core.test.cjs
```

The automated tests cover:

- Invoice subtotal calculations
- Tax and discount calculations
- Outstanding balance calculations
- Invoice payment statuses
- Receipt and invoice payment matching
- Input validation
- HTML escaping

Node.js is not required to use the application.

## Deploying on GitHub Pages

Billcraft Pro can be hosted for free using GitHub Pages.

### Deployment Steps

1. Create a public GitHub repository named `billcraft-pro`.
2. Upload all extracted project files and folders.
3. Ensure `index.html` is in the root directory.
4. Open the repository's **Settings**.
5. Select **Pages**.
6. Under **Build and deployment**, choose **Deploy from a branch**.
7. Select the `main` branch.
8. Select the `/(root)` directory.
9. Click **Save**.

After deployment completes, GitHub Pages will provide a public website URL.

No backend hosting or external database is required.

## Privacy and Data Storage

- All application data is stored in the browser using Local Storage.
- Records are not automatically uploaded to external servers.
- Data does not synchronize between browsers or devices.
- Clearing browser storage may permanently remove saved records.
- Regular JSON backups are recommended.
- Local Storage is not encrypted.
- Avoid storing sensitive financial information on shared computers.

## Important Limitations

- Billcraft Pro does not process real payments or verify banking transactions.
- Receipts represent payment information entered by the user.
- PDF export uses the browser's built-in print functionality.
- Currency changes do not automatically convert existing amounts.
- Discounts are calculated before taxes.
- Tax calculations are simplified and may not satisfy every jurisdiction's requirements.
- Multi-user access and cloud synchronization are not supported.
- Production business use would require additional security, authentication, and audit controls.

## Browser Compatibility

The application is designed for modern browsers, including:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari

## Contributing

Contributions and suggestions are welcome.

1. Fork this repository.
2. Create a new branch.
3. Make your changes.
4. Test your changes.
5. Submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).

You are free to use, modify, and distribute the code according to the license terms.
