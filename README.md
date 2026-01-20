# WeReelit Invoice Generator

A lightweight, single-file HTML invoice template designed for WeReelit freelance video editing services. This tool allows you to generate and export professional invoices directly from your browser.

## Features
* **Zero Installation:** Runs entirely in the browser using Tailwind CSS (CDN).
* **Click-to-Edit:** All text fields (Client Name, Date, Prices, Items) are directly editable on the screen.
* **Print Ready:** Custom CSS ensures the layout looks perfect when saving as a PDF, automatically hiding buttons and helper text.
* **Responsive Design:** Looks good on desktop and mobile screens.

## How to Use
1.  **Open:** Save the code as `invoice.html` and open it in Chrome, Edge, or Safari.
2.  **Edit:** Click directly on any text (e.g., "[Client Name]", "₹1200") to type the actual details.
3.  **Export:** Click the **"Save as PDF"** button at the bottom of the page.
4.  **Save:** In the print dialog, ensure "Save as PDF" is selected and "Background Graphics" is checked (if available) to keep the colors.

## Customization
To permanently change the brand colors or fonts, edit the `tailwind.config` script located in the `<head>` section of the file:

```javascript
colors: {
    brand: {
        dark: '#114238', // Dark Green
        light: '#72CFA6', // Light Green
        gray: '#f3f4f6'
    }
}
```


## Now Updating Invoice with Advance Features

### Key Changes Made:

Split Interface: The screen is now divided.

Left Side: A control panel/form to input details.

Right Side: The live preview of the invoice.

Invoice Type Selector: Added a dropdown to switch between "Advance Payment" and "Final Payment".

Advance Mode: Calculates the specific advance amount (e.g., 30%) and highlights that as the payable amount.

Final Mode: Shows the Total, subtracts the Advance already paid, and shows the Balance Due.

Real-time Updates: As you type in the form, the invoice updates instantly.

Auto-Calculation: You only need to enter the "Total Amount" and "Advance %". The code automatically calculates the math for INR amounts.
