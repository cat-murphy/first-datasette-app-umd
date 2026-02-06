# Act 1: Hello sqlite-utils - Session Notes

**Date:** February 4, 2025
**Student Experience Level:** Some command-line experience, not an expert

## What We Covered

### Setup
- Installed sqlite-utils using pip3
- Created data directory
- Downloaded Maryland grant data CSV (3.8MB, 19,482 records)
- Loaded CSV into SQLite database using `sqlite-utils insert`

### Core Concepts Learned
1. **Basic sqlite-utils commands:**
   - `insert` - loading CSV data into SQLite
   - `tables --counts` - checking table structure and row counts
   - `query` - running SQL queries from command line
   - `rows` - viewing table data

2. **SQL query fundamentals:**
   - SELECT, FROM, WHERE, ORDER BY, LIMIT, GROUP BY
   - Column names with spaces require quotes: `"Fiscal Year"`
   - CAST(column AS REAL) to convert text to numbers
   - Aggregate functions: SUM(), COUNT(), AVG()
   - Column aliases with `as name`

3. **Data export formats:**
   - Default output is JSON
   - `--csv` for CSV export
   - `--table` for readable table format
   - `--nl` for newline-delimited JSON
   - Redirecting output to files with `>`

4. **Shell escaping:**
   - Single vs. double quotes for SQL queries
   - Handling parentheses in SQL functions
   - Nested quotes: outer single + inner double, or vice versa

5. **Data maintenance concepts:**
   - Using `--ignore` flag to skip duplicates on insert
   - UPDATE queries to correct existing records
   - Verification queries before/after updates
   - Keeping backup records before corrections

### Challenges Completed
- **Challenge 1:** Quick Data Profiling - explored dataset structure
- **Challenge 2:** Command-Line SQL - wrote custom queries to answer journalistic questions
- **Challenge 3:** Data Extraction - exported data in multiple formats
- **Challenge 4:** Ongoing Data Maintenance - discussed workflows for updates and corrections

## What Went Well

1. **Student engagement:** Student asked good questions and experimented independently
2. **Problem-solving:** Student figured out that column name was `FiscalYear` (no space) on their own
3. **Application:** Student created their own query filtering by specific Grantor
4. **Critical thinking:** Student developed a solid workflow for monthly data updates with verification steps

## What Could Have Gone Better

### Teaching Approach Issues

1. **Too fast at the beginning:**
   - Initially ran commands for the student instead of having them run commands independently
   - Didn't explain what `-m` flag meant until student asked
   - Jumped into commands without breaking them down first
   - Student had to request: "You need to explain the commands"

2. **Incorrect technical information:**
   - Told student to use `--json` flag with query command
   - This flag doesn't exist (options are: `--json-cols`, `--nl`, or default JSON output)
   - Student discovered the error when they tried it: "Error: No such option: --json"
   - Should have verified command syntax before providing examples

3. **Better approach would have been:**
   - Let student run commands from the start
   - Explain each command BEFORE they run it
   - Verify all command syntax before suggesting
   - Provide more scaffolding questions rather than complete solutions

## Student Strengths Observed

- Good debugging instincts (recognized quoting issues)
- Willing to experiment and try variations
- Asked clarifying questions when confused
- Applied concepts to create original queries
- Thought through practical workflows for data maintenance

## Technical Notes

- Using `python3 -m sqlite_utils` because sqlite-utils not in PATH on this system
- macOS system - used curl instead of wget for downloads
- Column names in this dataset: no spaces (e.g., `FiscalYear` not `"Fiscal Year"`)
- Shell escaping: single quotes work best for SQL with functions/parentheses

## Ready for Act 2

Student has solid grasp of:
- Loading and querying data with sqlite-utils
- SQL basics for filtering, aggregating, and sorting
- Export formats for different use cases
- Data maintenance workflows

**Next:** Act 2: Hello Datasette - publishing data to web interface with search capabilities
