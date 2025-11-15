<html lang="en">
<body>
  <h1>E-Commerce Project SQL</h1>
<h2>Project Summary</h2>
  <p>
    Analyze session-level e-commerce data to understand conversion drivers, funnel drop-offs,
    and user behavior. Analysis is done in <strong>MySQL</strong>.
  </p>

  <h2>Dataset (high-level)</h2>
  <ul>
    <li><strong>SessionID</strong> — unique session identifier</li>
    <li><strong>UserID</strong> — unique user identifier</li>
    <li><strong>Timestamp</strong> — event date/time</li>
    <li><strong>PageType</strong> — home / product_page / cart / checkout / confirmation</li>
    <li><strong>DeviceType</strong> — Desktop / Mobile / Tablet</li>
    <li><strong>Country</strong>, <strong>ReferralSource</strong></li>
    <li><strong>TimeOnPage_seconds</strong>, <strong>ItemsInCart</strong>, <strong>Purchased</strong></li>
  </ul>

  <h2>Key Insights (summary)</h2>
  <div class="kpi">Overall conversion: <strong>20.2%</strong></div>
  <div class="kpi">Top referral: <strong>Google (21.6%)</strong></div>
  <div class="kpi">Peak hour: <strong>15:00 (3 PM)</strong></div>

  <table>
    <thead>
      <tr><th>Finding</th><th>Short implication</th></tr>
    </thead>
    <tbody>
      <tr><td>Buyers spend more time on Cart (≈100s)</td><td>Cart is final review stage — optimize UX and trust signals</td></tr>
      <tr><td>Non-buyers spend more time on Home (≈98s)</td><td>Improve home recommendations and CTAs to drive product discovery</td></tr>
      <tr><td>Higher cart depth → higher conversion</td><td>Promote bundles and bulk discounts to increase AOV</td></tr>
      <tr><td>Conversions peak mid-afternoon and mid-month</td><td>Schedule promotions and campaign pushes in these windows</td></tr>
    </tbody>
  </table>

  <h2>Business Recommendations</h2>
  <ul>
    <li>Prioritize spend on Google & Email (higher conversion ROI).</li>
    <li>Optimize mobile checkout and cart UX to reduce drop-offs.</li>
    <li>Run targeted mid-day and mid-month promotions for higher lift.</li>
    <li>Use cart-size based remarketing and bundle offers to increase conversions.</li>
  </ul>

  <h2>Project Files / Folder Structure</h2>
  <pre><code>
ecommerce-conversion-analysis/
├─ README.html                # (this file)
├─ sql_queries/
│  ├─ 01_create_schema.sql
│  ├─ 02_load_data.sql
│  ├─ 03_session_summary.sql
│  └─ ...
├─ datasets/
│  └─ ecom.csv
└─ report/
   └─ Ecommerce_Conversion_Analysis.pdf
  </code></pre>

  <h2>How to run (quick)</h2>
  <ol>
    <li>Load <code>customer_journey.csv</code> into MySQL (or your DB).</li>
    <li>Create normalized tables: <code>users</code>, <code>sessions</code>, <code>events</code>, <code>aggregatedb_date</code>.</li>
    <li>Run the analysis SQL scripts in <code>sql_queries/</code> to generate summary tables.</li>
    <li>Export summary tables to Excel for charts and dashboards.</li>
  </ol>

  <h2>Skills Demonstrated</h2>
  <ul>
    <li>SQL data modeling, joins, aggregations, CTEs, window functions</li>
    <li>Translating analysis into business recommendations</li>
  </ul>

  <footer>
    <p>Author: <strong>Tuhin Basu</strong> &nbsp;|&nbsp; Contact: https://www.linkedin.com/in/tuhinbasu | tuhinbasu97@gmail.com</p>
  </footer>
</body>
</html>
