---
name: "assignment-understander"
description: "Transform assignment instructions into clear task breakdowns with steps, criteria, and estimates. Use when user provides assignment text."
version: "1.0.0"
---

# Assignment Understander

## When to Use
- User pastes or uploads assignment instructions
- User asks: "What do I need to do?"
- User is confused about requirements, deliverables, or steps
- User needs clarity on time expectations

## Procedure
1. Read and interpret the user's assignment text
2. Identify the core objective in 2-3 sentences
3. Extract mandatory deliverables as a checklist
4. Break the assignment into step-by-step tasks
5. Identify how the assignment will be evaluated
6. Estimate time required per step
7. List common mistakes and how to avoid them
8. Present all results in the required output format

## Output Format
Claude must return text in the following sections exactly:

### SIMPLE EXPLANATION
(Explain the assignment in plain English, 2-3 sentences)

### CORE REQUIREMENTS
- [ ] requirement 1
- [ ] requirement 2
- [ ] requirement 3

### STEP-BY-STEP ACTION PLAN
1. Step 1
2. Step 2
3. Step 3

### SUCCESS CRITERIA
- Criterion 1
- Criterion 2

### TIME ESTIMATE
- Step 1 — X minutes
- Step 2 — Y minutes

### COMMON MISTAKES
- Mistake 1
- Mistake 2

## Example
Input: "Build a web scraper that extracts product data from e-commerce sites and stores it in a database. It should handle pagination and rate limiting."

Output:

### SIMPLE EXPLANATION
You need to create a program that automatically collects product information from online shopping websites and saves it to a database. The scraper must be smart enough to navigate through multiple pages and avoid overwhelming the websites with too many requests.

### CORE REQUIREMENTS
- [ ] Web scraper that extracts product data
- [ ] Handles multiple pages (pagination)
- [ ] Implements rate limiting
- [ ] Stores data in a database

### STEP-BY-STEP ACTION PLAN
1. Set up project structure and choose scraping library (BeautifulSoup, Scrapy) and database (SQLite, PostgreSQL)
2. Build basic scraper to fetch and parse a single page, extracting product information
3. Implement pagination to detect and navigate through all available pages
4. Add rate limiting with delays between requests (1-2 seconds) and respect robots.txt
5. Design database schema and write code to save scraped data, handling duplicates
6. Add error handling, logging, and test with different websites

### SUCCESS CRITERIA
- The scraper successfully extracts product data from at least one e-commerce site
- It navigates through multiple pages automatically
- Rate limiting is implemented and verifiable by timing requests
- Data is correctly stored in a database with proper schema
- The program handles errors gracefully without crashing

### TIME ESTIMATE
- Setup — 30 minutes
- Basic scraper — 1-2 hours
- Pagination — 1 hour
- Rate limiting — 30 minutes
- Database integration — 1-2 hours
- Testing and error handling — 1 hour
- Total: 5-7 hours (intermediate Python experience)

### COMMON MISTAKES
- Not checking robots.txt before scraping (can get your IP blocked)
- Making requests too quickly without rate limiting (will get blocked)
- Not handling pagination edge cases (infinite loops or stopping too early)
- Poor error handling causing crashes on network issues
- Not testing with real websites before considering it complete
- Choosing overly complex tools when simple ones work fine
