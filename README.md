# Dental-College-Data-Extraction
Automated Audit & Institutional Intelligence Pipeline

# Project Overview
In the healthcare education sector, institutional data (intake capacity, recognition status, and infrastructure) is often fragmented across multiple websites and PDFs.

As a Data Analyst, I built this automated ETL (Extract, Transform, Load) Pipeline to solve the problem of manual data collection. The system searches, scrapes, and uses AI to structure raw web text into a clean, analytical dataset.
# The Technical Process
1. Data Extraction (Discovery)
The pipeline identifies the "Primary Entity" by cross-referencing Google Maps API and DuckDuckGo Search.
  Scoring: I implemented a custom scoring logic to ensure the scraper targets the official college website and avoids "data noise" from third-party social media or old PDF links.

2. Data Transformation 
I utilized Crawl4AI for asynchronous web crawling. Because website data is "unstructured" (messy text), I integrated Groq AI (Llama 3.1) to perform Feature Engineering.
The model reads up to 15,000 words of scraped text and filters it into a strict JSON Schema. It ignores marketing "fluff" and extracts only hard facts (KPIs).

3. Data Loading (Structured Output)
The final output is a structured record ready for benchmarking.

Metric           Business Value
Management Type  Classifies Govt vs. Private institutions.
Seat Intake      Analyzes educational capacity.
DCI Status       Validates regulatory compliance.
Connectivity     Evaluates infrastructure accessibility (Airport/Railway).

# Key Results
Speed: Reduced audit time from 20 minutes per college to under 45 seconds.
Consistency: 95% accuracy in data extraction via LLM-based validation.
Scalability: Designed to process hundreds of institutions simultaneously using Asynchronous Concurrency.

# Tech Stack
Language: Python
LLM: Groq (Llama 3.1)
Automation: Crawl4AI, Playwright 
APIs: SerpApi (Google Search & Maps)
Data Handling: Pandas, JSON, Asyncio

# How to Use
1. Clone: git clone https://github.com/Shoumodipdc/Dental-College-Data-Extraction
2. Setup: Add your GROQ_API_KEY and SERPAPI_KEY to your environment variables or Colab Secrets.
3. Execute: Run the get_accurate_college_profile function to generate a report.
