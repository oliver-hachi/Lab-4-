# Lab 4 AI Log

## 1. ChatGPT - Discovery Questions (Step 2)

**Purpose:** Generate discovery questions for property professionals and local sponsors.

**Prompt Used:**
Help me create 8 neutral discovery questions for a neighborhood listing platform.

**Useful Output:**
ChatGPT suggested questions about managing property listings, accurate information, business promotion, content approval, platform usefulness, and website accessibility.

**Rejected Output:**
No specific suggestions were rejected.

**Verification:**
I reviewed the questions to make sure they were relevant, neutral, and did not ask for private information.

## 2. Gemini - Question Review (Step 2)

**Purpose:** Check the questions for leading wording and privacy risks.

**Prompt Used:**
Review these 8 interview questions for bias, leading questions, and private information.

**Useful Output:**
Gemini suggested improving questions 5, 7, and 8.

**Rejected Output:**
No specific suggestions were rejected.

**Verification:**
I reviewed Gemini's feedback and updated questions 5, 7, and 8. I also checked that the questions covered success measures and accessibility, as required by the lab instructions.

## 3. Google AI Studio - Theme Extraction (Step 4)

**Purpose:** Identify common themes and possible product requirements from simulated interview responses.

**Prompt Used:**
Analyze the simulated responses from property professionals and local sponsors. Identify 3–5 main themes, explain each theme, identify the supporting responses, and suggest one possible product requirement for each theme. Do not present assumptions as proven facts.

**Useful Output:**
Google AI Studio identified three themes:
- Information accuracy and listing management.
- Essential listing details.
- Business discovery and success measures.

It also suggested possible product requirements related to editing listings, displaying important property details, and tracking business discovery.

**Rejected Output:**
No specific themes were rejected. The suggested requirements were treated as possibilities rather than confirmed stakeholder needs.

**Verification:**
I compared the generated themes with the six simulated responses and updated `docs/interview-notes.md`. I checked that the documentation clearly states that the interviews were simulated and that the findings have not been validated by real stakeholders.

## 4. Commit Record

**Initial Commit:** `d7b3cc1`

**Initial Commit Message:** `Complete Lab 4 Steps 1-5`

**Documentation Update Commit:** `85cb946`

**Documentation Update Message:** `Update Lab 4 documentation`

The discovery materials were committed and pushed to `lab-4-branch`. Additional changes will be recorded in new commits.
# Lab 4 Part 2 Database Storage, Schema, & Row Level Security (RLS)
**AI Tool Used:** ChatGPT

**Prompt Used:** 
Help me draft a PostgreSQL schema for properties, sponsors, property_sponsors, profiles, and inquiries, including primary keys, foreign keys, nullability, and appropriate delete behavior.
Help me plan Row-Level Security (RLS) policies for public users, authenticated owners, and administrators.
"Create a security test matrix to verify that unauthorized database reads and writes are blocked.

### AI Assistance and Useful Output

ChatGPT helped draft the PostgreSQL migration file
migrations/001_create_core_tables.sql containing the five required tables:
properties
sponsors
property_sponsors
profiles
inquiries

The draft include: primary keys, foreign keys, required fields, default values, and deletion behaviors. RLS is enabled on all five tables.

ChatGPT also helped create tests/rls-test-matrix.md to document expected access permissions and unauthorized-access scenarios.

### Manual Review and Verification
Confirmed that the migration file contains all five required tables.
Reviewed primary keys, foreign-key relationships, nullability, and deletion behaviors.
Confirmed that RLS enablement statements are included for all five tables.
Confirmed that .env.local is ignored by Git.
Created a test matrix for public access, owner permissions, private inquiries, and administrator authorization.

### Limitations and Remaining Work
The migration has not yet been executed against a PostgreSQL database.
RLS policies have not yet been implemented or tested.
The authentication provider and secure user-identification mechanism still need to be confirmed.
Administrator authorization must be enforced through a trusted server-side mechanism.
The security test results must be recorded after the tests are executed.

No security tests are reported as passed at this stage.
EOF
