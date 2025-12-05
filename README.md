<h1>Invoice Generator – Total Care Property Solutions</h1>

<p>This project is a lightweight, browser-based <strong>Invoice Generator</strong> that allows any company to quickly create, preview, print, and download invoices as PDF using only HTML, CSS, and JavaScript. No backend is required.</p>

<h2>📌 Features</h2>
<ul>
    <li>Dynamic form to enter invoice details.</li>
    <li>Auto-generates description and fee fields.</li>
    <li>Invoice preview with professional layout.</li>
    <li>Automatic tax calculation (10%).</li>
    <li>Auto print dialog + optional PDF download.</li>
    <li>Uses <strong>html2pdf.js</strong> for PDF generation.</li>
</ul>

<h2>📁 File Structure</h2>
<pre>
invoice-generator/
│
├── index.html        # Input form page
├── print.html        # Invoice preview + PDF generation
└── tcps_h_logo.png   # Replace with your own logo
</pre>

<h2>🚀 How It Works</h2>
<ol>
    <li><strong>User fills form on <code>index.html</code></strong>.<br>
        They enter company name, address, invoice number, and number of descriptions.</li>
    <li><strong>User clicks "Type Descriptions"</strong> which auto-creates input fields.</li>
    <li><strong>Submitting form opens <code>print.html</code></strong> with all data using URL parameters.</li>
    <li><strong><code>print.html</code> generates the full invoice:</strong>
        <ul>
            <li>Calculates tax, totals, grand total</li>
            <li>Displays invoice date & due date (+14 days)</li>
            <li>Shows payment received</li>
            <li>Computes remaining due</li>
        </ul>
    </li>
    <li><strong>Page asks user: "Do you want to download PDF?"</strong><br>
        If yes → PDF downloads using html2pdf.js.</li>
    <li>Print dialog is triggered automatically.</li>
</ol>

<h2>🛠 Customization Guide</h2>

<h3>1. Replace Logo</h3>
<p>Replace the file <code>tcps_h_logo.png</code> or change:</p>
<pre>&lt;img src="your_logo.png" alt="Company Logo"&gt;</pre>

<h3>2. Edit Company Details in <code>print.html</code></h3>
<pre>
&lt;b&gt;Address:&lt;/b&gt; your address here &lt;br&gt;
&lt;b&gt;Email:&lt;/b&gt; your email here &lt;br&gt;
&lt;b&gt;Phone:&lt;/b&gt; your phone here &lt;br&gt;
&lt;b&gt;ABN:&lt;/b&gt; your business number &lt;br&gt;
</pre>

<h3>3. Change Tax Rate</h3>
<p>Located in <code>print.html</code>:</p>
<pre>const tax = fee * 0.1;</pre>

<h3>4. Change Due Date</h3>
<pre>dueDate.setDate(dueDate.getDate() + 14);</pre>

<h3>5. Customize CSS</h3>
<p>All styles are inside &lt;style&gt; tags. Modify freely to match your company theme.</p>

<h2>🌐 Requirements</h2>
<ul>
    <li>Any modern browser</li>
    <li>Internet (only for html2pdf CDN)</li>
    <li>No server needed (fully front-end)</li>
</ul>

<h2>📦 Ideal For</h2>
<ul>
    <li>Cleaning services</li>
    <li>Property management</li>
    <li>Freelancers & contractors</li>
    <li>Small businesses</li>
</ul>

<h2>📄 License</h2>
<p>This project is free to use and modify for any personal or commercial purpose.</p>
