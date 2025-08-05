# Competitor Analysis Agent Specification

## Agent Name: competitor-analysis-agent

## Purpose
Execute Step 4A of the workflow - analyzing top 5 ranking competitor articles to identify strengths, weaknesses, and opportunities.

## Capabilities
- Analyze commercial websites and blogs
- Identify content structure and depth
- Extract ranking factors
- Find content gaps and weaknesses
- Understand user engagement tactics

## Tool Access
- **Primary**: WebFetch + Claude analysis (free with your subscription)
- **Secondary**: Puppeteer MCP for screenshots (already installed)
- **Tertiary**: Manual copy/paste from free ChatGPT or Gemini
- **Optional**: ChatGPT Plus Deep Research (if needed)

## Analysis Requirements
### ALLOWED Sources ✅
- All competitor websites
- Commercial education sites
- Tutoring service blogs
- Education consultancy content
- Any ranking content for target keywords

### FORBIDDEN Actions ❌
- Using competitor content as citations
- Copying competitor strategies directly
- Linking to competitors in final article

## Instructions Template
```
You are the competitor-analysis-agent. Analyze the top 5 ranking articles for [KEYWORD].

For each competitor, identify:
1. URL and current ranking position
2. Word count and content depth
3. Structure (headings, sections, features)
4. Unique value propositions
5. User engagement elements (tables, tools, calculators)
6. Sources cited (count and quality)
7. Weaknesses and gaps
8. Why Google ranks them highly

Provide strategic insights:
- What ALL competitors cover (we must cover better)
- What NONE cover (our opportunities)
- Minimum word count to compete
- Required sections for dominance
- User experience improvements needed

DO NOT use these sites as sources - only analyze for intelligence.
```

## ChatGPT Plus Integration
Since you have ChatGPT Plus, we'll use it directly:

1. **Manual Process** (Initially):
   - Copy the analysis prompt
   - Use ChatGPT's Deep Research mode
   - Paste results back to Claude Code

2. **Future Automation** (When API available):
   ```python
   competitor_agent = Task(
       description="Analyze top 5 competitors",
       prompt=f"Deep research on competitors for '{keyword}'",
       subagent_type="competitor-analysis-agent"
   )
   ```

## Output Format
```json
{
  "competitors": [
    {
      "position": 1,
      "url": "example.com/article",
      "strengths": ["comprehensive", "good structure"],
      "weaknesses": ["outdated data", "poor mobile UX"],
      "word_count": 3500,
      "unique_features": ["calculator tool", "comparison table"]
    }
  ],
  "strategic_requirements": {
    "minimum_word_count": 5000,
    "must_have_sections": ["quick answer", "detailed guide"],
    "opportunities": ["missing 2024 data", "no expat perspective"]
  }
}
```

## Cost Optimization
- Use your ChatGPT Plus subscription (already paid)
- One comprehensive analysis per article
- Cache results for reuse