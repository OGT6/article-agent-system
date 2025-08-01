# Internal Linking Command

Generate WordPress-ready internal linking instructions with exact HTML code and placement guidance based on archive content analysis to build topic authority and prevent orphan content.

## Usage
`/internal-linking [NEW_ARTICLE_TOPIC] [ARCHIVE_URLS] [TARGET_ARTICLE_URL]`

## Example
`/internal-linking "IGCSE vs A-levels comparison" "archive1.com/igcse-guide, archive2.com/a-level-costs" "https://site.com/igcse-vs-a-levels"`

## Purpose
Strategic internal linking serves multiple SEO and UX objectives:
- **Topic Authority**: Build content clusters that dominate subject areas
- **User Journey**: Guide readers to related valuable content
- **Link Equity**: Distribute ranking power throughout portfolio
- **Dwell Time**: Increase site engagement metrics
- **Crawl Efficiency**: Help Google understand content relationships

## Analysis Process

### Step 1: Archive Content Mapping
Analyze provided archive URLs to identify:
- **Topic Relationships**: How content pieces connect
- **Keyword Overlap**: Shared and complementary terms
- **User Intent Flow**: Natural progression paths
- **Authority Pages**: High-value content to prioritize
- **Content Gaps**: Missing connections to establish

### Step 2: Link Opportunity Identification

#### Natural Connection Points
Find where links feel organic, not forced:
- Topic mentions that need elaboration
- Comparative statements referencing other options
- Background information readers might need
- Next steps or related decisions
- Supporting evidence or examples

#### Anchor Text Strategy
- **Exact Match**: Use sparingly (10-20% max)
- **Partial Match**: Include target keywords naturally
- **Branded**: When referencing specific programs/schools
- **Generic**: Avoid "click here" or "read more"
- **Long-tail**: Natural phrases that include keywords

### Step 3: WordPress-Ready Output

## Deliverable Format

```markdown
# Internal Linking Strategy: [Article Title]

## Quick Summary
- Total recommended links: [X]
- Links TO this article: [X]
- Links FROM this article: [X]
- Topic cluster: [cluster name]

## Links FROM This Article (Outbound)

### Link 1: Supporting Information
**Target Article:** "Complete Guide to IGCSE Subjects"
**Target URL:** https://yoursite.com/igcse-subjects-guide

**Placement:** 
- Section: "Choosing Your Curriculum"
- Paragraph: 3rd paragraph after introducing curriculum options
- After sentence: "...students typically select 8-10 subjects for their IGCSEs."

**WordPress HTML:**
```html
<a href="https://yoursite.com/igcse-subjects-guide">comprehensive guide to IGCSE subject selection</a>
```

**Full Context Example:**
"Most students typically select 8-10 subjects for their IGCSEs. For detailed guidance on building the right subject portfolio for your child's goals, see our <a href="https://yoursite.com/igcse-subjects-guide">comprehensive guide to IGCSE subject selection</a>, which includes university pathway considerations."

**Link Purpose:** 
- Provides depth on subject selection process
- Captures readers researching IGCSE options
- Builds IGCSE topic cluster authority

### Link 2: Cost Comparison
**Target Article:** "Private School Fees UK 2024"
**Target URL:** https://yoursite.com/private-school-fees-uk-2024

**Placement:**
- Section: "Financial Considerations"
- Paragraph: 2nd paragraph discussing costs
- After sentence: "...fees can vary significantly between schools."

**WordPress HTML:**
```html
<a href="https://yoursite.com/private-school-fees-uk-2024">current UK private school fee analysis</a>
```

**Full Context Example:**
"While IGCSE and A-level costs are similar, overall fees can vary significantly between schools. Our <a href="https://yoursite.com/private-school-fees-uk-2024">current UK private school fee analysis</a> breaks down costs by region and school type, including hidden expenses many parents overlook."

[Continue for all outbound links...]

## Links TO This Article (Inbound)

### From Article: "Choosing International Schools in Asia"
**Current Article URL:** https://yoursite.com/international-schools-asia

**Placement Instructions:**
1. Navigate to: Posts > All Posts > "Choosing International Schools in Asia"
2. Find section: "Curriculum Options"
3. Locate paragraph discussing British curricula
4. Add after: "...British families often prefer maintaining UK educational continuity."

**WordPress HTML to Insert:**
```html
For families considering the British curriculum path, our <a href="https://yoursite.com/igcse-vs-a-levels">detailed comparison of IGCSEs and A-levels</a> explores how these qualifications differ for international students.
```

### From Article: "University Applications from International Schools"
**Current Article URL:** https://yoursite.com/university-applications-international

**Placement Instructions:**
1. Navigate to: Posts > All Posts > "University Applications from International Schools"
2. Find section: "Qualification Requirements"
3. Locate paragraph about UK university entry
4. Add after: "...Russell Group universities accept both qualifications equally."

**WordPress HTML to Insert:**
```html
While Russell Group universities accept both qualifications equally, understanding the <a href="https://yoursite.com/igcse-vs-a-levels">practical differences between IGCSEs and A-levels</a> helps families make informed decisions about their child's pathway.
```

[Continue for all inbound links...]

## Topic Cluster Architecture

### Core Pillar Page
**Title:** "British Education Abroad: Complete Guide"
**Role:** Hub connecting all British curriculum content

### Supporting Content Cluster
1. IGCSE vs A-levels (This article)
2. IGCSE Subject Selection Guide
3. A-level Subject Combinations
4. UK University Entry from Abroad
5. Private School Fees Comparison

### Internal Linking Map
```
[Pillar Page]
    ├── IGCSE vs A-levels ←→ Subject Guides
    ├── Subject Guides ←→ University Entry
    └── All pages → Fee Comparison
```

## Implementation Checklist

### Before Publishing
- [ ] Add all outbound links during article upload
- [ ] Note exact placement locations
- [ ] Use provided HTML exactly
- [ ] Check all URLs are correct

### After Publishing
- [ ] Update each existing article with inbound links
- [ ] Verify all links work correctly
- [ ] Check mobile formatting
- [ ] Monitor click-through rates

## Best Practices Applied

### Natural Integration
- Links add value, not just SEO benefit
- Anchor text flows within sentences
- Placement at natural curiosity points
- Context provided before and after

### SEO Optimization
- Varied anchor text (no over-optimization)
- Relevant topical connections
- Balanced link distribution
- No forced or awkward placements

### User Experience
- Links where readers need more info
- Clear value proposition for clicking
- Maintains reading flow
- Mobile-friendly formatting

## Common Mistakes to Avoid

### Over-Linking
- Maximum 2-3 links per 500 words
- Not every mention needs a link
- Avoid linking same page multiple times
- Don't interrupt crucial paragraphs

### Poor Anchor Text
- ❌ "Click here to read more"
- ❌ "This article about IGCSEs"
- ❌ Entire sentences as anchor text
- ❌ Keyword stuffing in anchors

### Forced Connections
- Don't link unrelated content
- Avoid tenuous topic stretches
- Keep within topic clusters
- Maintain user intent alignment

## Tracking Success

### Metrics to Monitor
- Click-through rate on internal links
- Pages per session increase
- Bounce rate reduction
- Time on site improvement
- Topic cluster rankings

### WordPress Plugins for Tracking
- MonsterInsights for click tracking
- Yoast SEO for internal link suggestions
- Link Whisper for opportunity identification
- Google Analytics for user flow

## Remember
Internal linking is about building helpful content ecosystems. Every link should serve the reader first, with SEO benefits as a natural consequence of good UX.
```