# Web-Scrapping-
A web scrapping jupyter notebook project that scraps jobs from websites


How to run this notebook every 24 hours
Open this notebook in Jupyter (or VS Code / Cursor) and run all cells. This will:

Scrape all developer jobs from https://www.myjobmag.co.ke/search/jobs?q=developer.
Merge with the existing myjobmag_developer_jobs.xlsx file (if it exists).
Save an updated Excel file with all unique jobs.
To automate it every 24 hours on Windows (simple approach):

Install Jupyter and ensure python is in your PATH.
Create a .bat file that runs:
cd /d C:\Users\dkyalo\Desktop\Trial
jupyter nbconvert --to notebook --execute jobs_scraper.ipynb --output jobs_scraper_executed.ipynb
Use Task Scheduler to create a basic task that runs this .bat file once every day.
Each daily run will append new jobs (if any) and avoid duplicates using the job_key column.
