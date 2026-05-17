# 📊 Premium Dynamic Payment Calculator (INR)

An enterprise-grade, high-performance client-side financial amortization matrix and simulation dashboard designed specifically for the Indian banking system context. Featuring a premium, responsive dark-mode glassmorphic visual language, this system calculates real-time interest compounding variances, periodic loan decay velocities, and multi-conditional repayment amortization pipelines with zero server latency.

🔗 **Live Production Server:** [paymentcalculator.free.nf](http://paymentcalculator.free.nf)

---

## 🎨 Design System & Aesthetic Language

The dashboard implements a customized modern dark design engineered around visual hierarchy and high scannability:

* **Glassmorphism Backdrop:** Implemented via Tailwind utilities combining high blur radius (`backdrop-filter: blur(16px)`) with subtle, translucent boundaries (`rgba(255, 255, 255, 0.05)`) to achieve floating layer depth over radial base gradients.
* **Accent Signaling:** Features glowing neon purple and deep indigo design tokens to draw emphasis to primary functional elements, input matrices, and key calculation outcomes.
* **Fluid Keyframe Interactivity:** Range input elements utilize smooth cubic-bezier micro-transitions (`transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1)`) on interactive slider points to enhance tactile input tracking.
* **Layout Optimization:** Built with responsive CSS grids, adapting from complex multi-column viewports on 4K monitors to single-column interactive feeds on mobile devices.

---

## ✨ Core Functional Features

### 1. Real-Time Calculation Engine
The underlying algorithms run immediately on input hooks (`input` and `change` event streams). Moving a slider array instantly streams fresh mathematical processing down to text interfaces, data graphs, and structural tables without requiring interface updates or refresh lag.

### 2. Dual Repayment Architectures
* **Standard Amortization (Equated Monthly Installments):** Computes reducing balance structures where the periodic installment remains stable while the internal principal-to-interest split dynamically balances across the lifecycle.
* **Terminal Balloon Payments Structure:** Configured for institutional structured loans, allowing an operator to define an end-of-term lump sum payment. The algorithm lowers periodic overhead outlays by deferring a set portion of the principal straight to the final closing date.

### 3. Localization Matrix (Indian Numbering Format)
Standard browser locales format currencies via Western standards (grouping by thousands, e.g., `500,000.00`). This application bypasses that default behavior via custom string parsing algorithms explicitly built for Indian Banking Units (**Lakhs** and **Crores**), formatting structural boundaries safely as `₹5,00,000.00`.

### 4. Interactive Telemetry Visuals
Renders graphical datasets via **Chart.js**, featuring synchronous point-tracking overlays. It maps:
* **Remaining Balance Decay** (Visualizing asset risk reduction metrics)
* **Cumulative Principal Paid Accrual** (Tracking equity building velocity)
* **Cumulative Interest Accrual** (Showing total true cost projection tracks)

---

## 🧮 Mathematical Formulas Implemented

The application logic engine computes periodic values using standard financial calculations. Let $P$ represent the Principal Amount, $r$ represent the Periodic Interest Rate, $n$ represent the Total Number of Payments, and $B$ represent the Terminal Balloon Amount.

### Standard Reducing Balance Amortization (EMI)
When a regular structured payment path is active, the static installment amount ($M$) is derived via:

$$M = \frac{P \cdot r \cdot (1 + r)^n}{(1 + r)^n - 1}$$

### Advanced Balloon Payment Structural Formula
When a customized commercial Terminal Balloon layout is activated, the periodic payment layout ($M$) is calculated by factoring in the present value of the terminal lump sum:

$$M = \frac{P \cdot r \cdot (1 + r)^n - B \cdot r}{(1 + r)^n - 1}$$

### Data Point Compounding Adjustments
The Periodic Interest Rate ($r$) and Total Number of Payments ($n$) adapt dynamically to the **Payment Interval Dropdown Selection**:
* **Monthly:** $r = \frac{\text{Annual Rate}}{12}$, $n = \text{Years} \cdot 12$
* **Quarterly:** $r = \frac{\text{Annual Rate}}{4}$, $n = \text{Years} \cdot 4$
* **Half-Yearly:** $r = \frac{\text{Annual Rate}}{2}$, $n = \text{Years} \cdot 2$
* **Yearly:** $r = \frac{\text{Annual Rate}}{1}$, $n = \text{Years} \cdot 1$

---

## 🛠️ Stack Architecture & CDNs

The dashboard uses a serverless client-side architecture to minimize load times and maximize security by handling all calculations directly in the browser:

* **Markup Layer:** HTML5 (Validated semantic structure)
* **Design Core Framework:** Tailwind CSS Engine via runtime compilation node CDN
* **Data Plotting Vector Engine:** Chart.js Framework via secure global mirror link
* **Calculation Automation System:** Vanilla Javascript (Native ECMAScript 6+ standard compliance)

---

## 💻 Local Sandbox Setup Instructions

To setup a local copy of this repository on your computer for offline review or extension:

```bash
# 1. Clone the workspace from your GitHub link
git clone [https://github.com/AdityawithA/Payment-Calculator.git](https://github.com/AdityawithA/Payment-Calculator.git)

# 2. Step inside the repository path
cd Payment-Calculator

# 3. Open index.html directly inside your default web browser
# Windows users
start index.html

# macOS users
open index.html
