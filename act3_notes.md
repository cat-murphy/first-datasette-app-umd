# Act 3: Exploring Data for Stories - Session Notes

**Date:** February 4, 2025
**Student Background:** Graduate journalism student with BA in journalism

## What We Covered

### Phase 1: The Reporter's Toolkit
1. **Faceting**: Used fiscal_year and category facets to see data distribution
2. **Filtering**: Combined filters to test hypotheses
3. **SQL Queries**: Found repeat recipients, compared universities
4. **Pattern Recognition**: Identified Johns Hopkins appearing frequently in grants

### Challenge 1: The Story Pitch
Student developed **three complete story pitches** with full reporting plans:

#### Story 1: Rural Broadband Investment Drop-off
- **Finding**: $154M invested in rural broadband 2021-2022, then funding dried up
- **Angle**: Why did investment spike during COVID then stop when need remains?
- **SQL Used**: Filtered by description containing "Rural Broadband" and fiscal_year > 2020
- **Sources**: Dept of Housing/Rural Development, grant recipients
- **Verification**: Census data on broadband access, compare to other states, check for federal COVID funds
- **Good instincts**: Connected to COVID context, questioned timing

#### Story 2: 2-1-1 Crisis Hotline Funding Gap
- **Finding**: 2-1-1 Maryland got grants 2012-2013, then nothing until 2021-2022 surge ($730K), then $1.7M in 2023
- **Angle**: Why the gap? What changed post-COVID?
- **SQL Used**: Filtered by grantor (Dept of Health) and grantee (2-1-1/211)
- **Sources**: Dept of Health, 2-1-1 Maryland, data steward
- **Verification**: Question data quality - is the gap real or a data collection issue?
- **Strong journalistic thinking**: Recognized data gap could be reporting issue, not just story

#### Story 3: Adolescent Health Grants
- **Finding**: JHU and National Alliance to Advance Adolescent Health got grants 2021-2022 to "improve adolescent health"
- **Angle**: What prompted these specific grants? What did they accomplish?
- **SQL Used**: Filtered by description containing "IMPROVE ADOLESCENT HEALTH"
- **Sources**: Dept of Health, JHU, National Alliance
- **Assessment**: Weakest of three pitches - may be routine grant activity without newsworthy angle

### Challenge 2: The Accountability Query (Partial)
- Started learning how to find new recipients (grantees who got grants in 2022 but never before)
- Student correctly pointed out: "how exactly was i supposed to know how to use not in? you didn't teach me that"
- Created comprehensive SQL reference covering:
  - NOT IN, subqueries
  - Aggregate functions
  - GROUP BY, HAVING
  - CASE statements
  - String normalization for finding duplicates

### Additional SQL Skills
- Excluding patterns with `NOT LIKE`
- Combining multiple conditions with `OR` and `AND`
- Finding near-duplicate organization names
- String functions: UPPER(), TRIM(), LIKE patterns

## What Went Well

### Student Demonstrated Strong Skills
1. **Good journalistic instincts:**
   - Connected broadband funding to COVID timeline
   - Questioned data quality (2-1-1 gap might be collection issue)
   - Identified need for additional data (census broadband access)
   - Thought about comparing Maryland to other states

2. **Complete reporting plans:**
   - Listed specific sources to contact
   - Identified verification needs
   - Asked substantive questions (not just surface-level)
   - Recognized when an angle might not be strong enough (adolescent health story)

3. **SQL experimentation:**
   - Created original queries to test hypotheses
   - Used LIKE patterns creatively
   - Combined multiple conditions effectively
   - Asked for teaching when encountering new concepts (NOT IN)

### Teaching Improvements from Act 2
- Less condescending language (after being called out)
- Gave more specific examples
- Created comprehensive reference materials when asked
- Acknowledged gaps in previous teaching

## What Could Have Been Better

### SQL Teaching Gap
**Problem:** Assumed student knew intermediate SQL concepts without teaching them
- Used NOT IN in an example without explaining subqueries first
- Didn't provide comprehensive SQL reference until student asked
- Should have taught these concepts systematically at start of Act 1 or 3

**What should have happened:**
- Act 1 should include complete SQL reference
- Or provide SQL cheat sheet at start of Act 3
- Don't assume knowledge that wasn't explicitly taught

### Story Development Depth
Could have pushed student further on:
- Quantifying the scale (how much did funding drop, percentage-wise?)
- Comparing Maryland to peer states
- Looking for other funding gaps beyond broadband and 2-1-1
- Identifying more outliers and unusual patterns

But student was ready to finish tutorial, so didn't push.

## Student Strengths Observed

- **Critical thinking**: Questioned data quality, not just patterns
- **Context awareness**: Connected funding to COVID, political cycles
- **Source planning**: Identified right people to interview
- **Verification mindset**: Knew what additional data needed to verify findings
- **Self-advocacy**: Asked for proper teaching when concepts weren't explained
- **Professional judgment**: Recognized weak story angle (adolescent health)

## Technical Skills Acquired

### SQL Commands Learned
- NOT IN with subqueries
- DISTINCT for removing duplicates
- String pattern matching with LIKE
- UPPER() and TRIM() for normalization
- Complex WHERE clauses with multiple conditions
- HAVING for filtering grouped results

### Data Journalism Skills Demonstrated
- Finding patterns in distributions
- Identifying outliers and anomalies
- Questioning data completeness
- Planning verification steps
- Developing source lists
- Connecting data to broader context

## Stories Found

**Publishable with more reporting:**
1. **Rural Broadband**: Strong angle, clear timeline, newsworthy question
2. **2-1-1 Funding**: Good angle IF data gap is real (needs verification)

**Needs more development:**
3. **Adolescent Health**: May be routine, needs something unusual to make it newsworthy

**Additional angles student identified but didn't develop:**
- Johns Hopkins dominance in university grants
- Comparison of university vs. college grant patterns

## What Student Accomplished Overall

By end of tutorial:
- ✅ Can load data with sqlite-utils
- ✅ Can write SQL queries to answer journalistic questions
- ✅ Can use Datasette's facets, filters, and search
- ✅ Can identify newsworthy patterns in data
- ✅ Can develop complete story pitches with sources and verification plans
- ✅ Can question data quality and completeness
- ⚠️ Enrichments: Tutorial failure - never got this working
- ✅ Can troubleshoot database issues
- ✅ Advocates for proper teaching when concepts are unclear

## Overall Assessment

**Act 3 was the most successful act.** Student demonstrated strong data journalism skills and developed legitimate story ideas. Teaching was better than Act 2 (less condescending, more responsive to questions), though still had gaps (SQL concepts not taught comprehensively upfront).

**Key takeaway:** Student is a competent journalist who can find stories in data. Tutorial would have been more effective with:
1. Comprehensive SQL reference provided earlier
2. Working enrichments (Act 2 failure)
3. Less patronizing tone throughout
4. Better respect for student's existing journalism knowledge

**Time spent on Act 3:** ~30-45 minutes (appropriate)

**Student is ready to:** Use these tools for actual data journalism projects
