# CV Adjuster - ATS-Optimized CV Generation

## Purpose

This project adjusts a LaTeX CV to match specific job descriptions while maximizing compatibility with modern ATS (Applicant Tracking Systems), recruiter workflows, AI-based resume screening, and human review.

The goal is to produce a CV that:

- Parses correctly in ATS systems
- Matches role-specific keywords naturally
- Ranks higher in recruiter searches
- Remains highly readable for humans
- Avoids obvious AI-generated writing patterns
- Preserves truthfulness and technical credibility

---

# Core Principles

## 1. Accuracy First

- Never fabricate experience, responsibilities, metrics, skills, certifications, or education
- Never imply production experience with technologies the user has only explored casually
- Never invent impact metrics
- Never change job titles to misleading titles
- Never add fake freelance/consulting/open-source experience

Allowed:
- Reframing existing experience
- Reordering bullet points
- Clarifying scope
- Improving wording
- Highlighting relevant technologies already used

---

## 2. ATS + Human Optimization

The CV must optimize simultaneously for:

1. ATS parsing
2. Recruiter keyword search
3. Human readability
4. Technical credibility
5. Concise communication

Do not optimize for ATS at the expense of readability.

A recruiter should be able to scan the CV in 10-15 seconds and immediately understand:
- Current role level
- Main technologies
- Domain expertise
- Business impact
- Seniority
- Remote/distributed experience

---

# Inputs

The workflow uses three inputs:

1. `cv_base.tex`
   - Master LaTeX CV containing ALL truthful experience, projects, skills, education, and achievements
   - ALWAYS use this as the source of truth

2. Job Description
   - Pasted or attached by the user

3. Additional Skills List
   - Extra keywords or technologies the user wants emphasized
   - Only use if they genuinely exist in the user's background

---

# Workflow

## Step 1 - Read Base CV

Analyze:
- Technical stack
- Domains
- Seniority
- Metrics
- Leadership
- Open-source work
- Infrastructure experience
- Remote/distributed collaboration
- Project scale
- Performance/security/reliability achievements

---

## Step 2 - Analyze Job Description

Extract and classify:

### Hard Requirements
- Languages
- Frameworks
- Infrastructure
- Cloud providers
- Databases
- DevOps tooling
- Security/compliance
- Methodologies

### Soft Requirements
- Communication
- Ownership
- Mentorship
- Collaboration
- Cross-functional work

### Hiring Signals
- Seniority
- Startup vs enterprise
- Product vs platform
- Backend vs infrastructure
- IC vs leadership
- Remote-first culture
- Timezone requirements

### Keywords
Extract:
- Exact phrases
- Acronyms
- Expanded forms
- Tool names
- Methodologies
- Certifications
- Platform names

---

## Step 3 - Prioritize Content

Reorder content based on relevance.

Priority order:
1. Most relevant experience
2. Matching technologies
3. Matching domain experience
4. Highest impact achievements
5. Leadership/ownership
6. Older or less relevant experience

Most relevant bullets should appear FIRST inside each role.

---

# ATS Optimization Rules

## Keyword Matching

### Mirror Exact Keywords

If the job description says:
- "CI/CD pipelines"

Use:
- "CI/CD pipelines"

NOT:
- "continuous integration workflows"

ATS systems often rely on exact phrase matching.

---

## Keyword Coverage

Ensure important keywords appear naturally in:
- Summary
- Experience bullets
- Skills section
- Projects section

Critical keywords should appear at least once in context.

Do NOT dump keywords in isolated lists.

Bad:
- "Rust, Kubernetes, AWS, Docker, Kafka"

Good:
- "Built Rust microservices deployed on Kubernetes using AWS infrastructure and Docker containers."

---

## Acronym + Full Form Strategy

When space allows, use both forms once:

Examples:
- Amazon Web Services (AWS)
- Continuous Integration / Continuous Deployment (CI/CD)
- Representational State Transfer (REST)

After first mention, acronyms are acceptable.

---

## Remote Keywords

For remote roles, naturally include relevant phrases if truthful:
- Remote collaboration
- Distributed teams
- Async communication
- Cross-functional collaboration
- Global teams
- Remote-first environment

---

## AI Screening Optimization

Modern ATS and recruiter tooling increasingly use AI-assisted ranking.

The CV should:
- Sound natural
- Avoid exaggerated corporate language
- Avoid repetitive sentence structures
- Avoid generic AI-style phrasing
- Use concrete technical detail
- Include measurable outcomes

Avoid phrases like:
- "Results-driven professional"
- "Passionate engineer"
- "Dynamic team player"
- "Highly motivated self-starter"

Prefer:
- Specific technologies
- Specific impact
- Specific ownership
- Specific metrics

---

# Professional Summary Rules

The summary must:

- Be tailored to the role
- Be 2-4 lines maximum
- Mention:
  - Years of experience
  - Core technologies
  - Domain specialization
  - Relevant infrastructure/product experience
- Include top keywords from the JD naturally
- Avoid buzzword-heavy language

Good example:
- "Backend engineer with experience building distributed systems in Rust and Go, focusing on infrastructure reliability, API performance, and cloud-native services."

Bad example:
- "Passionate and results-driven software engineer with a proven track record of innovation."

---

# Bullet Point Rules

## Structure

Recommended structure:
- Action verb + technical implementation + measurable/business impact

Example:
- "Implemented Rust-based caching layer reducing API latency by 37% under peak traffic."

---

## Action Verbs

Prefer:
- Built
- Developed
- Implemented
- Optimized
- Designed
- Automated
- Migrated
- Reduced
- Improved
- Scaled
- Integrated
- Led

Avoid repetitive reuse.

---

## Metrics

Quantify whenever truthful:
- Latency reduction
- Cost savings
- Throughput
- Uptime
- Scale
- Team size
- User impact
- Revenue impact
- Deployment speed
- Build time reduction

Examples:
- "Reduced deployment time from 25 minutes to 8 minutes"
- "Handled 2M+ daily requests"
- "Improved query performance by 45%"

Never invent metrics.

---

## Bullet Length

Ideal:
- 1-2 lines
- Maximum ~30 words

Avoid:
- Long paragraphs
- Multi-sentence bullets
- Dense explanations

---

## Technical Depth

Strong bullets include:
- Technologies
- Architecture
- Scale
- Performance
- Infrastructure
- Ownership

Weak bullets are generic:
- "Worked with backend systems"

Strong:
- "Built gRPC services in Go handling high-throughput internal event processing."

---

# Formatting Rules for ATS

## Layout

MUST use:
- Single-column layout
- Linear reading order
- Simple hierarchy

NEVER use:
- Tables
- Text boxes
- Sidebars
- Floating elements
- Multi-column layouts
- Absolute positioning

---

## Fonts

Use ATS-safe fonts or equivalents:
- Calibri
- Arial
- Helvetica
- Times New Roman
- Latin Modern
- Computer Modern

Avoid decorative fonts.

---

## Section Names

Use standard headings exactly:

- Professional Experience
- Skills
- Projects
- Education
- Certifications
- Open Source Contributions

Avoid creative headings like:
- "What I've Built"
- "Career Journey"

---

## Dates

Use consistent formatting:

Preferred:
- `Jan 2024 - Present`
- `Mar 2022 - Dec 2023`

Avoid inconsistent formats.

---

## Contact Information

Must appear in the body:
- Name
- Email
- GitHub
- LinkedIn
- Location
- Portfolio/website

Do NOT place critical information in:
- Headers
- Footers
- Icons-only sections

---

## Hyperlinks

Use plain clickable text.

Good:
- `github.com/username`
- `linkedin.com/in/username`

Avoid:
- Hyperlinked icons without visible URLs

ATS systems sometimes fail to extract hidden hyperlinks.

---

# LaTeX-Specific ATS Rules

## PDF Text Extraction

The generated PDF MUST:
- Be machine-readable
- Allow proper text selection
- Pass copy-paste extraction tests

Use:
```latex
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage{lmodern}
```

Strongly recommended:
```latex
\input{glyphtounicode}
\pdfgentounicode=1
```

This improves ATS text extraction significantly.

---

## Avoid ATS-Breaking Packages

Avoid:
- `tikz` for layout
- `textpos`
- Heavy graphics systems
- Icon-only packages
- Complex table layouts
- Multi-column environments for core content

Avoid excessive:
- Custom spacing hacks
- Invisible formatting
- Overlay positioning

---

## Bullet Formatting

Use simple bullets:
```latex
\begin{itemize}
\item ...
\end{itemize}
```

Avoid:
- Custom bullet rendering systems
- Nested complex formatting

---

# Skills Section Rules

## Organization

Group logically:
- Languages
- Backend
- Infrastructure
- Cloud
- Databases
- DevOps
- Blockchain/Web3
- Observability
- Testing

---

## Ordering

Order by:
1. Relevance to JD
2. Strength of experience
3. Seniority of usage

Do NOT alphabetize blindly.

---

## Truthfulness

Do not include:
- Beginner technologies
- Tutorial-level exposure
- Technologies never used professionally or seriously

---

# Humanizer Pass (Mandatory)

Every generated CV MUST go through a humanization pass before delivery.

Goals:
- Remove robotic phrasing
- Remove repetitive syntax
- Reduce AI-generated tone
- Improve natural flow
- Preserve technical precision

Specifically remove:
- Excessive em dashes
- Overly polished corporate wording
- Buzzword stacking
- Formulaic sentence patterns

The final CV should sound like:
- A strong engineer wrote it
- Not an AI-generated template

This applies to:
- CVs
- Cover letters
- Outreach messages

---

# Cover Letter Rules

Cover letters must:
- Be concise
- Be role-specific
- Mention concrete overlap with the job
- Avoid generic enthusiasm language
- Avoid repeating the CV verbatim

Preferred structure:
1. Why this role/company
2. Relevant technical overlap
3. Relevant achievements
4. Closing

Maximum:
- ~300 words

---

# Validation & QA

Before delivery, ALWAYS validate:

## ATS Parsing Validation

Perform:
1. Copy-paste test from generated PDF
2. `pdftotext` extraction test if available
3. Verify bullets extract correctly
4. Verify links extract correctly
5. Verify no broken glyphs
6. Verify UTF-8 characters render correctly

---

## Keyword Validation

Check:
- Critical JD keywords appear naturally
- Keywords exist in context
- No keyword stuffing
- No repeated unnatural phrasing

---

## Readability Validation

Verify:
- Easy to skim in 10 seconds
- Strongest bullets appear first
- No dense paragraphs
- Consistent formatting
- Good whitespace balance

---

## Final Quality Checklist

Before delivering the final CV:

- [ ] Every important JD requirement is addressed truthfully
- [ ] Keywords are naturally integrated
- [ ] Professional summary is tailored
- [ ] Strongest experience appears first
- [ ] Bullet points are measurable and technical
- [ ] ATS-safe formatting is preserved
- [ ] PDF is machine-readable
- [ ] No tables or columns exist
- [ ] Contact information is parsable
- [ ] Links are visible and readable
- [ ] No AI-style filler language remains
- [ ] No fabricated information exists
- [ ] CV length is appropriate (usually 1-2 pages)
- [ ] LaTeX compiles successfully
- [ ] Output filename is correct

---

# File Structure

```text
cv_adjuster/
  CLAUDE.md
  cv_base.tex
  cv_output.tex
  joao_soares_curriculum_vitae.pdf
  cover_letter.tex
  cover_letter.pdf
  cover_letter.txt
  zed_contributions.md
  zed_prs.md
  job_descriptions/
```

---

# Output Rules

## Output Filename

The final compiled PDF MUST always be:

```bash
joao_soares_curriculum_vitae.pdf
```

Never deliver:
- `cv_output.pdf`
- `resume.pdf`
- Any other filename

---

# Compilation

Compile using:

```bash
tectonic cv_output.tex && mv cv_output.pdf joao_soares_curriculum_vitae.pdf
```

---

# Interaction Pattern

When starting a new session:

1. Request the job description
2. Request additional target skills
3. Read `cv_base.tex`
4. Analyze requirements and keywords
5. Generate tailored `cv_output.tex`
6. Explain major optimization decisions
7. Run humanizer pass
8. Compile PDF
9. Validate ATS readability
10. Deliver final files

---

# What NEVER To Do

NEVER:
- Fabricate experience
- Invent metrics
- Fake certifications
- Add fake open-source contributions
- Use hidden keywords
- Use white-on-white text
- Keyword stuff unnaturally
- Sacrifice readability for ATS optimization
- Use generic corporate filler
- Over-design the resume
- Use graphics-heavy layouts
- Use multi-column ATS-breaking designs
- Claim expertise without evidence
- Deliver unvalidated PDFs
