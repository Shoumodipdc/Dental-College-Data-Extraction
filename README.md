# Dental-College-Data-Extraction
Objective
To solve the problem of fragmented healthcare data. Instead of manually searching for college details, this project uses an Automated Data Pipeline to collect, verify, and structure information for 100+ institutions.

The Analyst's Process (ETL)
Extraction (Finding Data): The system automatically searches Google Maps and official websites. It doesn't just "scrape"; it uses a scoring algorithm to make sure it finds the correct college and ignores the wrong ones.

Transformation (Cleaning Data with AI): Websites are full of "fluff" (ads, long paragraphs, irrelevant news). I used Groq AI (Llama 3.1) to act as a digital filter. It reads 15,000+ words of website text and extracts only the Key Performance Indicators (KPIs) we need, like seat intake and recognition status.

Loading (Reporting): The final step turns the AI's findings into a structured table. This allows us to compare colleges side-by-side, spot trends (like urban vs. rural distribution), and check for regulatory compliance.

Why This Matters for Business
Efficiency: It does 10 hours of manual research in 30 seconds.

Data Integrity: It uses AI to cross-verify facts across multiple sources, ensuring the data is accurate.

Insights: By structuring the data, we can now create charts and reports to help students or investors make better decisions.

Technical Tools
Python: The core engine.

Groq AI: Used for "Feature Engineering" (turning text into numbers/categories).

Crawl4AI: Used for high-speed, parallel web reading.

SerpApi: Used for geospatial data (location and reviews).
