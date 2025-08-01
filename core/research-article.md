# Research Article Command

Execute the complete 10-step article research and writing workflow for creating SEO-optimized educational content targeting British expat parents and UK independent school parents.

## Usage
`/research-article [TOPIC] [PRIMARY_AUDIENCE: expat|uk|both]`

## Example
`/research-article "Should my child take IB or A-levels?" both`

## Workflow Overview

This command orchestrates the entire 11-step process:

1. **SEO Research** - Keyword analysis and search intent
2. **Deep Research Phase 1** - Academic source gathering
3. **Article Outline** - Quick Answer + Full Answer structure
4. **Comprehensive Gap Analysis** - Internal audit + competitor analysis to prevent cannibalization
5. **User Approval** - First checkpoint
6. **Deep Research Phase 2** - Fill knowledge gaps
7. **Outline Update** - Refine based on new research
8. **Final Approval** - Second checkpoint
9. **Article Writing** - Create final content
10. **Internal Linking** - WordPress-ready link placement instructions
11. **Harvard References** - Complete citation list

## Process Details

### Initial Setup
1. Confirm topic and target audience(s)
2. Create topic slug from title (lowercase, hyphenated)
3. Create article folder structure:
   ```
   articles/[topic-slug]/
   ├── research/
   ├── planning/
   ├── drafts/
   └── final/
   ```
4. Identify primary and secondary keywords
5. Set research parameters
6. **MANDATORY: Voice Calibration (Assignment-Specific)**
   - Determine: Is this an existing cluster or new topic area?
   - For existing clusters: Request 3-5 archive links
   - For new clusters: Request 2-3 sample URLs
   - Create assignment-specific voice analysis document
   - File: `articles/[topic-slug]/planning/voice-analysis.md`
   - MUST complete before any writing begins

### Research Phase
- Use academic and government sources only
- Minimum 15-20 credible references
- Balance sources for both audiences
- Document all findings with citations

### Outline Development
- Create Quick Answer (150-200 words)
- Structure comprehensive full answer
- Include sections for both audiences
- Plan tables, lists, and formatting

### Gap Analysis (Internal + External)
**Internal Audit (if archive provided):**
- Review existing content for overlap
- Assess cannibalization risks
- Decide update vs new content
- Plan content hierarchy

**External Analysis:**
- Review top 5 competitors
- Identify missing perspectives
- Note unique angles for differentiation
- Focus on dual-audience opportunities

**Integrated Strategy:**
- Prevent internal competition
- Build topic authority
- Maximize portfolio strength

### Writing Phase
- Reference assignment-specific voice analysis document
- Apply documented voice patterns throughout
- Implement calibrated voice (not generic template)
- No em dashes allowed
- British spelling throughout
- Natural integration of both audiences
- Verify each section against voice profile

### Quality Checks
- Voice consistency
- SEO optimization
- Citation accuracy
- Audience balance
- Practical value

### Internal Linking Strategy
- Analyze archive content for connections
- Identify natural link opportunities
- Create WordPress-ready HTML
- Provide exact placement instructions
- Build topic cluster authority

## File Locations

### Research Phase
- SEO Analysis: `articles/[topic-slug]/research/seo-analysis.md`
- Gap Analysis: `articles/[topic-slug]/research/gap-analysis.md`
- Source Notes: `articles/[topic-slug]/research/sources.md`

### Planning Phase
- Outline: `articles/[topic-slug]/planning/outline.md`
- Voice Analysis: `articles/[topic-slug]/planning/voice-analysis.md`

### Writing Phase
- Draft: `articles/[topic-slug]/drafts/draft-v1.md`
- Polished: `articles/[topic-slug]/drafts/draft-polished.md`

### Final Deliverables
- Article: `articles/[topic-slug]/final/article-final.md`
- Internal Linking: `articles/[topic-slug]/final/internal-linking.md`
- References: `articles/[topic-slug]/final/references.md`

## Output Structure

```markdown
# [Question-Format Title]

## Quick Answer
[Snippet-optimized response]

## Now, The Answer You Deserve

### Introduction
[Engaging opening]

### [Main Sections]
[Comprehensive content]

### Audience-Specific Sections
#### For British Expat Parents
[Relevant considerations]

#### For UK-Based Parents
[Relevant considerations]

### Key Takeaways
[Bullet points]

## References
[Harvard format]
```

## Audience Considerations

### When PRIMARY_AUDIENCE = "expat"
- Emphasize international perspectives
- Include repatriation planning
- Currency conversions
- Cultural adaptation

### When PRIMARY_AUDIENCE = "uk"
- Focus on UK system navigation
- Regional considerations
- Entrance exam strategies
- League table context

### When PRIMARY_AUDIENCE = "both"
- Balance content equally
- Find universal themes
- Address unique needs of each
- Highlight commonalities

## Voice Requirements
- New Yorker dry wit meets British middle-class humor
- Educational authority without condescension
- Cultural references that resonate
- Anti-pretentious but intellectually rigorous
- Practical wisdom with gentle humor

## Research Sources
### Required
- Academic journals (.edu)
- Government reports (.gov)
- Educational statistics
- Peer-reviewed studies
- Official education bodies

### Excluded
- Competitor websites
- Marketing materials
- Social media
- Unverified blogs
- Commercial consultancies

## Deliverables
1. Voice analysis document (assignment-specific)
2. SEO research report
3. Initial outline with Quick Answer
4. Gap analysis findings (internal + external)
5. Updated comprehensive outline
6. Final article (competitive length)
7. Internal linking instructions (WordPress-ready)
8. Harvard reference list
9. Meta description
10. SEO optimization checklist

## Success Criteria
- Both audiences well-served
- 15+ academic citations
- Featured snippet potential
- Superior to competitors
- Practically valuable
- Voice consistency
- SEO optimized