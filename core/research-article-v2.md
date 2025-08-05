# Research Article Command v2 - With Separated Agents

Execute the complete 11-step article research and writing workflow using specialized agents with clean separation of concerns.

## Usage
`/research-article [TOPIC] [PRIMARY_AUDIENCE: expat|uk|both] [--auto-approve]`

## Example
`/research-article "Should my child take IB or A-levels?" both --auto-approve`

## Updated Workflow with Separated Agents

### Step 1: SEO Research & Competitive Forensics
```bash
# Using WebFetch + Claude analysis (FREE)
WebFetch("google.com/search?q=[keyword]", "Extract top 5 URLs")
```

### Step 2: Deep Research Phase 1 (Academic ONLY)
```bash
# Call academic-research-agent
Task(
    subagent_type="general-purpose",
    prompt="""
    You are the academic-research-agent. Find academic sources for [TOPIC].
    ONLY use: .gov, .gov.uk, .edu, .ac.uk, peer-reviewed journals
    NEVER use: commercial sites, competitors
    Use Semantic Scholar API and academic search engines.
    Return 15-20 sources with summaries.
    """
)
```

### Step 3: Article Outline Creation
```bash
# Claude creates outline based on research
```

### Step 4A: Competitor Analysis (Commercial sites OK)
```bash
# Call competitor-analysis-agent
Task(
    subagent_type="general-purpose", 
    prompt="""
    You are the competitor-analysis-agent. Analyze top 5 competitors for [KEYWORD].
    Use WebFetch to get each competitor's content.
    Identify: structure, word count, gaps, strengths, weaknesses.
    DO NOT use these as sources - only for intelligence.
    """
)
```

### Step 5: User Approval Gate
```bash
if not "--auto-approve" flag:
    # Present findings and wait for approval
else:
    # Continue automatically
```

### Step 6: Deep Research Phase 2 (Academic ONLY)
```bash
# Call academic-research-agent again
Task(
    subagent_type="general-purpose",
    prompt="""
    Find additional academic sources to fill these gaps: [GAPS]
    Same rules as Step 2 - academic sources only.
    """
)
```

### Step 7: Outline Update
```bash
# Claude refines outline
```

### Step 8: Final Approval Gate
```bash
if not "--auto-approve" flag:
    # Wait for approval
else:
    # Continue automatically
```

### Step 8a: Voice Calibration (AUTOMATIC)
```bash
# Use default voice URLs
voice_urls = [
    "https://oxbridgegcsetutor.com/",
    "https://oxbridgegcsetutor.com/igcse-vs-gcse-which-exam-syllabus-is-harder/",
    "https://oxbridgegcsetutor.com/edexcel-igcse-grades-and-boundaries/"
]

/voice-calibrate archive voice_urls topic
```

### Step 9: Article Writing
```bash
# Claude writes using calibrated voice
```

### Step 10: Strategic Internal Linking
```bash
# Generate WordPress-ready HTML
```

### Step 11: Harvard Reference List
```bash
# Format all citations
```

## Key Changes from v1

1. **Separated Agents**: Each agent has ONE job
2. **Clear Source Rules**: Academic agent NEVER sees competitors
3. **Automatic Voice**: Uses pre-configured URLs
4. **Free Tools**: WebFetch instead of paid APIs
5. **Auto-Approve Option**: Skip manual gates

## Cost: £0 Additional
- Uses your Claude subscription
- Free academic APIs
- WebFetch (built-in)
- No extra tools needed

## Output
Same high-quality article, but with:
- ✅ No source contamination
- ✅ Clear agent responsibilities  
- ✅ Automatic voice calibration
- ✅ Optional full automation