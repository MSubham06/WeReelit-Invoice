# WeReelit Invoice Generator

A powerful, single-file HTML invoice tool designed specifically for **WeReelit** freelance video editing services. This tool replaces manual document editing with a dynamic, split-screen interface that calculates prices, formats layouts, and exports professional invoices instantly.

## 🚀 Features

### 🖥️ Interface & Experience
* **Split-Screen Layout:** A control panel on the left for inputting details and a live A4 preview on the right.
* **Resizable Sidebar:** (Desktop) Drag the edge of the sidebar to adjust the workspace width to your preference.
* **Mobile & Tablet Ready:** The layout automatically adapts to a vertical stack on mobile devices. The A4 preview automatically scales down to fit small screens without horizontal scrolling.
* **Zero Installation:** Runs entirely in the browser using Tailwind CSS (CDN). No server, backend, or build step required.

### 💰 Smart Financial Logic
* **Invoice Modes:**
    * **Advance Mode:** Calculates the specific advance percentage (default 30%) and sets it as the "Total Due".
    * **Final Mode:** Shows the Grand Total, subtracts the Advance already received, and calculates the final "Balance Due".
* **Auto-Calculation:**
    * **Package Automation:** Select a Package (Basic, Simple, Intermediate, Advance) to auto-fill base prices, duration, and revision limits.
    * **Video Count Multiplier:** Base Price automatically multiplies by the number of videos.
    * **Additional Costs:** Add extra fees (e.g., Rush Fee) which are added to the Grand Total but excluded from Advance percentage calculations.

### 🎨 Customization & Branding
* **Payment Privacy Control:** Individual checkboxes to Show/Hide **Account Name**, **UPI ID**, and **Phone Number** on the final invoice.
* **Editable Payment Details:** Default Account Name is set to "M SUBHAM" but can be edited on the fly.
* **Custom Notes:** Toggle a "Custom Design Note" field to add specific instructions or details to the invoice body.
* **Status Stamp:** Toggle a professional Green **"PAID"** stamp overlay.
* **Theme Integration:** Custom dark-mode inputs with brand-colored (Green) calendar icons and number spinners.

### 📂 Export & Saving
* **Smart Filenaming:** Files are automatically saved with a structured name: `WeReelit_Invoice_[No]_[ClientName]_[Type]`.
* **Save as PDF:** Uses the browser's native print engine (configured for A4, zero margins, and background graphics).
* **Save as Image:** Generates a high-quality PNG of the invoice using `html2canvas`.

---

## 🛠️ How to Use

1.  **Open the File:** Double-click `invoice.html` to open it in Chrome, Edge, Safari, or Firefox.
2.  **Select Mode:** Choose **"Advance Payment"** (for starting a project) or **"Final Payment"** (for completion).
3.  **Fill Details:**
    * Enter Client Name/Company.
    * Select **Video Style** and **Package**.
    * Adjust **Video Count** (Price updates automatically).
4.  **Configure Payment:**
    * Check/Uncheck the boxes next to UPI or Phone to decide what payment info is visible to the client.
    * Toggle "Mark as PAID" if the invoice is already settled.
5.  **Export:**
    * Click **"Save as Image"** for a quick PNG to share via WhatsApp.
    * Click **"Save as PDF"** for a formal document.

---

## ⚙️ Configuration (For Developers)

The tool uses **Tailwind CSS** via CDN for styling. You can customize the brand colors by editing the `script` tag in the `<head>` section of `invoice.html`:

```javascript
tailwind.config = {
    theme: {
        extend: {
            colors: {
                brand: {
                    dark: '#114238',    // Primary Dark Green
                    darker: '#0d332b',  // Deep Background
                    main: '#1B7F66',    // Brand Accent
                    light: '#72CFA6',   // Highlights/Text
                    text: '#E0FDF4',    
                    white: '#FFFFFF'
                }
            }
        }
    }
}
```
---

### 💡 Why is it better to build your own invoice tool?

Building a custom tool (like the one we just made) is often superior to using generic templates or expensive SaaS software for several reasons:

* **Total Automation:** Unlike Word/Excel templates where you have to manually calculate taxes or totals every time, a custom tool automates the math. You enter "2 videos," and the price instantly doubles—eliminating human error.
* **Exact Workflow Fit:** Off-the-shelf software might not have a "Video Style" dropdown or a specific "Advance Payment" toggle. Custom tools are built *exactly* for your specific business logic (e.g., your specific packages and revision limits).
* **Branding Control:** You aren't stuck with a generic layout. You have 100% control over the colors, logo placement, and fonts, ensuring your invoices look exactly like your brand.
* **One-Time Cost:** Instead of paying a monthly subscription fee for software like QuickBooks or FreshBooks, you build this once and use it forever for free.
* **Data Privacy:** Your client data stays on your local machine. You aren't uploading sensitive client details to a third-party server.

---

## 💼 Need a Tool Like This?

**I can build custom software for your business.**

If you need automated tools, invoice generators, or custom web applications tailored to your workflow, feel free to reach out. I build solutions that save time and look professional.

---

## ⚠️ License & Rights

**All Rights Reserved.**

This repository and the code contained within are the intellectual property of **M SUBHAM / WeReelit**.

* This code is **NOT** open source.
* You are **strictly prohibited** from copying, reusing, redistributing, or selling this code for your own commercial or personal use without explicit written permission.
