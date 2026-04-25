# CV Adjuster - ATS-Optimized CV Generation

## Purpose

This project adjusts a LaTeX CV to match specific job descriptions, optimizing for ATS (Applicant Tracking System) compatibility so the CV passes automated AI/recruiter screening.

## Workflow

The user provides three inputs:

1. **Base CV** (`cv_base.tex`) - LaTeX file containing all experience, education, projects, and skills - ALWAYS GET THE DATA FROM HERE TO GENERATE THE NEW CV ABOVE THE JD
2. **Job Description** - pasted or attached as text
3. **Skills list** - additional skills/keywords to incorporate

Claude then:

1. Analyzes the job description to extract required skills, keywords, qualifications, and responsibilities
2. Rewrites and reorders CV content to maximize relevance to the target role
3. Outputs the adjusted LaTeX file as `cv_output.tex`

## ATS Optimization Rules

When adjusting the CV, follow these rules strictly:

### Content Strategy
- **Mirror exact keywords** from the job description (e.g., if the job says "CI/CD pipelines", use that exact phrase, not "continuous integration")
- **Match job title** in the CV header/summary when truthful and reasonable
- **Quantify achievements** with numbers, percentages, and metrics wherever possible (e.g., "Reduced build time by 40%")
- **Use action verbs** to start each bullet point (Led, Developed, Implemented, Designed, Optimized, etc.)
- **Map experience to requirements** - reorder and rephrase bullet points so the most relevant experience appears first
- **Include a tailored professional summary** at the top that directly addresses the role's key requirements

### Keyword Optimization
- Extract all hard skills, soft skills, tools, technologies, certifications, and methodologies from the job description
- Ensure each critical keyword appears **at least once** in the CV body (not just in a skills section)
- Use both the acronym and full form where space allows (e.g., "Amazon Web Services (AWS)")
- Place the most important keywords in the top third of the CV

### Formatting for ATS
- **No tables, columns, or text boxes** - use simple linear layout
- **No headers/footers** for critical info (name, contact must be in body)
- **No images, icons, or graphics** - ATS cannot parse them
- **Standard section headings**: "Professional Experience", "Education", "Skills", "Certifications", "Projects"
- **Use standard fonts** (Calibri, Arial, Times New Roman, or their LaTeX equivalents)
- **Dates in consistent format**: "MMM YYYY - MMM YYYY" or "MM/YYYY - MM/YYYY"
- **Simple bullet points** using `\item` or `\textbullet`
- **No fancy LaTeX packages** that break text extraction (avoid `tikz` for layout, `fontawesome` icons, multi-column environments for content)

### Humanizer Pass (Mandatory)
- **Every CV rewrite MUST be run through `/humanizer`** before delivery — no exceptions
- This removes AI-generated writing patterns (inflated language, promotional tone, em dash overuse, AI vocabulary, etc.)
- Apply after all content edits are finalized but before PDF compilation
- Also apply to cover letters when generated

### What NEVER do(Follow that here strictly)
- Never fabricate experience, skills, or qualifications the user doesn't have
- Never remove truthful information just because it's not in the job description - deprioritize it instead
- Never use "stuffing" (hiding white-on-white keywords) - this gets flagged
- Never use generic filler phrases ("team player", "hard worker") without backing evidence

## File Structure

```
cv_adjuster/
  CLAUDE.md              # This guide
  cv_output.tex          # Generated ATS-optimized CV for the target role
  cv_output.pdf          # Compiled PDF output
  cover_letter.tex       # Generated cover letter (LaTeX source)
  cover_letter.pdf       # Compiled cover letter PDF
  cover_letter.txt       # Plain text version of cover letter
  zed_contributions.md   # Zed editor contributions reference
  zed_prs.md             # Zed PRs reference data
  job_descriptions/      # Saved job descriptions for reference
    cv_base.tex          # User's master CV with all experience
```

## LaTeX Compilation

To generate the PDF, compile with:

```bash
tectonic cv_output.tex
```

**Prerequisites**: Tectonic must be installed. It handles font/package downloads automatically — no separate TeX distribution needed.

## Interaction Pattern

When the user starts a new CV adjustment session:

1. Ask for the **job description** if not provided
2. Ask for the **skills list** if not provided
3. Read `cv_base.tex` to understand all available experience
4. Analyze the job description and identify: required skills, preferred skills, responsibilities, seniority level, industry
5. Draft `cv_output.tex` with ATS optimizations applied
6. Show the user a summary of key changes made and why
7. Run `/humanizer` on `cv_output.tex` to remove AI-generated writing patterns and ensure natural, human-sounding language
8. Compile to PDF
9. If the user requests revisions, iterate on `cv_output.tex`, re-run `/humanizer`, and recompile

## Quality Checklist

Before delivering the final CV, verify:

- [ ] Every required skill from the job description is addressed (if the user has it)
- [ ] Keywords from the job description appear naturally in context
- [ ] Bullet points are achievement-oriented with metrics where possible
- [ ] Section headings are ATS-standard
- [ ] No formatting elements that break ATS parsing
- [ ] Contact information is in the document body, not headers/footers
- [ ] Professional summary is tailored to the specific role
- [ ] Experience is ordered by relevance to the target role
- [ ] The CV compiles without errors
- [ ] Output is 1-2 pages maximum (unless explicitly requested otherwise)
