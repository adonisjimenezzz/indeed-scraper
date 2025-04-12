## Indeed Scraper: Robust Job Market Analysis

The Indeed Scraper provides a robust foundation for job market analysis and data collection with advanced capabilities that make it resilient against multiple anti-scraping measures!

This comprehensive scraper offers:

**Stealth Mode with Rotating Identity**

* Browser fingerprint randomization
* User agent rotation
* Proxy support
* Human-like behavior simulation
* Advanced anti-detection measures

**Asynchronous Support**

* Concurrent page scraping with Playwright
* Managed browser contexts for parallel operations
* Semaphore-based concurrency control
* Unified API that works in both sync and async modes

**AI-Enhanced Job Description Analysis**

* Skill extraction for technical, soft, and domain skills
* Sentiment analysis for company culture
* Job description summarization
* Salary estimation for listings without salary info
* Market insights generation

**Usage Examples**

The script includes examples that demonstrate how to use the scraper:

```python
# Basic usage
scraper = IndeedScraper(headless=True)
jobs = scraper.scrape_jobs("data scientist", "remote", max_pages=1)
print(f"Found {len(jobs)} jobs")

# Advanced usage with async and AI analysis
import asyncio

async def run_async_example():
    scraper = IndeedScraper(async_mode=True, ai_analysis=True)
    jobs = await scraper.scrape_jobs_async(
        "software engineer",
        "New York",
        job_type=["full-time"],
        get_details=True
    )
    print(f"Found {len(jobs)} jobs with async mode")

asyncio.run(run_async_example())
