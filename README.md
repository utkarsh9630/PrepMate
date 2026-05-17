# LinkedIn Data Engineering Job Search Automation

This script automates a LinkedIn job-search workflow from Chrome. It is intended to search for **Data Engineer / Data Engineering roles in the United States**, filter for jobs **posted today**, identify listings where the user is likely to be a strong or top applicant based on resume skills, and export the best matches into a spreadsheet.

# Demo Link-: https://drive.google.com/file/d/14aMfInT0pT5DTAh8wbXEglQESXjYITpn/view?usp=sharing

## What the Script Does

The workflow follows these high-level steps:

1. Opens Google Chrome.
2. Navigates to LinkedIn Jobs.
3. Searches for data engineering roles in the United States.
4. Filters results to jobs posted today.
5. Reviews job listings against the user's resume or skill summary.
6. Selects the top 10 most relevant listings where the user appears to be a strong applicant.
7. Creates a spreadsheet containing the selected listings.
8. Saves the spreadsheet to Google Drive.

## Expected Inputs

The script may require the following inputs or local resources:

- A LinkedIn account already logged in through Chrome.
- A resume file available locally, for example:
  - `Utkarsh_resume.rtf`
  - `Utkarsh_resume.pdf`
  - `Utkarsh_resume.docx`
- Access to Google Drive through the same browser session.
- Search parameters such as:
  - Job title: `Data Engineer` or `Data Engineering`
  - Location: `United States`
  - Date posted: `Today`
  - Number of listings to export: `10`

## Suggested Spreadsheet Columns

The generated spreadsheet should include columns similar to the following:

| Column | Description |
|---|---|
| Rank | Ranking from 1 to 10 |
| Job Title | Title of the job listing |
| Company | Company name |
| Location | Job location or remote status |
| Posted Date | Date or freshness of the posting |
| LinkedIn URL | Direct link to the job posting |
| Match Reason | Why the user is a strong applicant |
| Key Required Skills | Skills mentioned in the job description |
| Resume Skill Match | Matching skills found in the resume |
| Notes | Any additional comments |

## Example Output

The final spreadsheet might be named:

```text
linkedin_data_engineering_jobs_today_top_10.xlsx
```

or

```text
linkedin_data_engineering_jobs_today_top_10.csv
```

## How to Run

Update this section based on the actual script language and filename.

### Python Example

```bash
python linkedin_job_search.py
```

### Node.js Example

```bash
node linkedin_job_search.js
```

## Configuration

If the script supports configuration, use values like these:

```text
JOB_TITLE="Data Engineer"
LOCATION="United States"
DATE_POSTED="Today"
MAX_RESULTS=10
RESUME_PATH="./Utkarsh_resume.rtf"
OUTPUT_FILE="linkedin_data_engineering_jobs_today_top_10.xlsx"
SAVE_TO_DRIVE=true
```

## Notes

- LinkedIn page structure can change, so selectors may need updates over time.
- The script should avoid sending job applications automatically unless explicitly configured to do so.
- Some actions may require manual login, CAPTCHA completion, or two-factor authentication.
- Google Drive upload may require browser login or API credentials depending on implementation.
- Use the script responsibly and follow LinkedIn's terms and rate limits.

## Troubleshooting

### LinkedIn does not open

Confirm that Chrome is installed and that the script has permission to control the browser.

### Jobs are not filtered to today

Check whether LinkedIn changed the date filter label or page structure.

### Resume cannot be read

Verify that the resume file exists and that the script supports its file format.

### Spreadsheet is not saved to Drive

Confirm that Google Drive is accessible and that the script has upload permissions.

## Future Improvements

- Add support for multiple job titles.
- Add duplicate detection.
- Score each listing based on resume match percentage.
- Include salary, seniority level, and remote/hybrid filters.
- Export both Excel and CSV formats.
- Add a summary sheet with top matching skills and companies.
