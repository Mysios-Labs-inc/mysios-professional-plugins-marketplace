# SKILL.md Frontmatter Fixes

## Problem
5 out of 6 skill files are missing the `name` field in their YAML frontmatter. Only `profile-setup` has it correctly.

## Fix Required
Add the `name` field to the frontmatter of each SKILL.md file.

## Files to Update

### 1. `skills/resume-optimizer/SKILL.md`
**Add this line to the frontmatter (after the opening `---`):**
```yaml
name: resume-optimizer
```

### 2. `skills/job-search/SKILL.md`
**Add this line to the frontmatter:**
```yaml
name: job-search
```

### 3. `skills/cover-letter-generator/SKILL.md`
**Add this line to the frontmatter:**
```yaml
name: cover-letter-generator
```

### 4. `skills/interview-prep/SKILL.md`
**Add this line to the frontmatter:**
```yaml
name: interview-prep
```

### 5. `skills/salary-research/SKILL.md`
**Add this line to the frontmatter:**
```yaml
name: salary-research
```

## Example Format
Each SKILL.md should start like this:
```yaml
---
name: resume-optimizer
description: Generate and optimize resumes...
# ... other frontmatter fields
---

# Skill content starts here...
```

## Quick Fix Method
For each file, edit the frontmatter section at the top and add the `name` field right after the opening `---` line.