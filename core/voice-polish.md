# /voice-polish

## Purpose
Polish an existing article's voice without redoing the entire 11-step workflow. This command preserves all research, structure, citations, and factual content while applying authentic voice throughout.

## Usage
```
/voice-polish "[article_file_path]" "[archive_urls_or_sample_urls]" "[target_voice_description]"
```

## Parameters
1. **article_file_path**: Path to the existing article that needs voice polishing
2. **archive_urls_or_sample_urls**: URLs for voice calibration (comma-separated)
3. **target_voice_description**: Brief description of desired voice (e.g., "New Yorker wit + British parental humor")

## Process

### Step 1: Article Analysis
- Read the existing article file
- Extract and preserve:
  - All factual content and statistics
  - Research citations and references
  - Article structure and headings
  - Tables and data
  - SEO elements (meta description, keywords)
  - Internal linking HTML
  - Word count

### Step 2: Voice Calibration
- Execute `/voice-calibrate` with provided URLs
- Create voice analysis document specific to this polishing task
- Identify target voice characteristics:
  - Humor style and frequency
  - Sentence structure patterns
  - Cultural references
  - Metaphor preferences
  - Transition styles
  - Opening/closing patterns

### Step 3: Content Mapping
Create a detailed map preserving:
- Every statistic and fact
- All research citations
- Complete article structure
- Table data integrity
- Technical accuracy
- SEO keywords naturally placed

### Step 4: Voice Transformation
Rewrite the article section by section:
- **Preserve**: All facts, figures, citations, structure
- **Transform**: Sentence style, humor injection, cultural references
- **Enhance**: Transitions, metaphors, parenthetical asides
- **Maintain**: SEO value and keyword placement

### Step 5: Quality Checks
- Verify all original facts remain intact
- Confirm citations match exactly
- Check word count is similar (±10%)
- Ensure SEO elements preserved
- Validate voice consistency throughout

## Voice Transformation Guidelines

### What to Change
1. **Sentence Structure**
   - Generic: "IGCSE registration requires careful planning."
   - Polished: "IGCSE registration requires the sort of careful planning usually reserved for military campaigns or destination weddings."

2. **Humor Injection**
   - Add 2-3 witty observations per 500 words
   - Use parenthetical asides for comedic effect
   - Include cultural references appropriate to audience

3. **Transitions**
   - Replace bland connectors with conversational bridges
   - Use rhetorical questions
   - Add personality to section introductions

4. **Metaphors and Analogies**
   - Generic descriptions → vivid comparisons
   - Technical explanations → relatable scenarios
   - Abstract concepts → concrete imagery

### What to Preserve Exactly
1. **All Data**
   - Statistics and percentages
   - Dates and deadlines
   - Costs and fees
   - Requirements and criteria

2. **All Research**
   - Direct quotes
   - Citation details
   - Source references
   - Academic findings

3. **All Structure**
   - Heading hierarchy
   - Section organization
   - Table layouts
   - List formats

4. **All SEO Elements**
   - Keywords and placement
   - Meta descriptions
   - Internal link HTML
   - URL slugs

## Example Transformations

### Original (Generic Voice)
"The IGCSE examination system operates on a two-session annual cycle. The May/June session is the primary examination period, with registration closing in February. Late registration incurs additional fees."

### Polished (New Yorker Wit + British Parental Humor)
"The IGCSE examination system runs on a two-session annual cycle with all the flexibility of a Swiss railway timetable. The May/June session serves as the main event (think Wimbledon, but with more tears), with registration closing in February sharp. Miss that deadline and late fees arrive with the reliability of British weather—unwelcome but inevitable."

## Output Format

### Polished Article File
```markdown
# [Original Title - Preserved Exactly]

*[Original Meta Description - May be lightly polished]*

## [All Original Sections Preserved]

[Voice-transformed content with all facts intact]

## References
[Exact same references as original]
```

### Voice Polish Report
```markdown
# Voice Polish Report

## Original Article
- File: [path]
- Word Count: [original]
- Voice Style: [detected style]

## Voice Calibration Results
- Archive/Sample URLs analyzed: [list]
- Target Voice: [description]
- Key voice characteristics identified: [list]

## Transformation Summary
- New Word Count: [count]
- Humor Injections: [count]
- Metaphors Added: [count]
- Facts Preserved: 100%
- Citations Verified: ✓

## Quality Checks
- [ ] All data intact
- [ ] Structure preserved
- [ ] Voice consistent
- [ ] SEO maintained
```

## Implementation Notes

### Efficiency Gains
- Avoids redoing 11-step research process
- Preserves weeks of research work
- Focuses effort only on voice refinement
- Maintains competitive analysis value

### When to Use
- Article has strong research but weak voice
- Client requests tone adjustment
- Testing different voice styles
- Updating older content with fresh voice

### When NOT to Use
- Content needs factual updates
- Structure requires reorganization
- Research is outdated
- SEO strategy has changed

## Voice Library Integration
Common voice combinations:
- "New Yorker wit + British parental humor" (OxbridgeGCSETutor standard)
- "Academic authority + conversational warmth"
- "Professional expertise + gentle irreverence"
- "Data-driven + delightfully human"

## Error Handling
- If article file not found: Request correct path
- If URLs invalid: Request proper archive/sample URLs
- If voice calibration fails: Provide manual voice examples
- If word count varies >20%: Flag for review

## Success Metrics
- Voice authenticity score: 90%+
- Fact preservation: 100%
- Reading engagement: 2x baseline
- Client satisfaction: Immediate approval
- Time saved: 10-15 hours vs full rewrite