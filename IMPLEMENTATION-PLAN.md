# Implementation Plan - Leveraging Your Existing Subscriptions

## Your Current Resources
- **Claude**: £180/month subscription (includes Claude Code)
- **ChatGPT Plus**: £20/month subscription
- **Free Tools**: Semantic Scholar, Zotero, Google Scholar

## Phase 1: Immediate Implementation (No Extra Cost)

### 1. Academic Research Agent
- **Tool**: Semantic Scholar API (free) + Google Scholar
- **Backup**: Your Claude subscription for synthesis
- **Process**: Agent searches, Claude synthesizes findings

### 2. Competitor Analysis Agent  
- **Tool**: FREE - WebFetch + Claude analysis
- **Process**: Automated with Claude Code
- **Backup**: Manual analysis with free ChatGPT/Gemini
- **No extra cost**: Uses your existing Claude subscription

### 3. Content Writing Agent
- **Tool**: Your Claude API (via Claude Code)
- **Quality**: Claude produces the best prose
- **Tokens**: Your £180 subscription provides ample capacity

### 4. Voice Calibration Agent
- **Tool**: Claude API
- **Process**: Analyze archive samples, create voice profile
- **Integration**: Direct through Claude Code

## Phase 2: First Additions (When Needed)

### Option A: SEO Enhancement (~£140/month)
Add **Semrush** when you need:
- Keyword research at scale
- SERP feature tracking
- Competitive intelligence

### Option B: Citation Automation (~£20/month)
Add **Sourcely Premium** when you need:
- Automated Harvard formatting
- Bulk citation generation
- Integration with your workflow

## Immediate Next Steps

1. **Test the Free Stack**:
   ```bash
   # Use existing agents with new architecture
   /research-article "Your Article Topic"
   ```

2. **Manual Competitor Analysis**:
   - Go to ChatGPT Plus
   - Enable Deep Research mode
   - Analyze top 5 competitors
   - Paste results back to Claude Code

3. **Configure Agents**:
   - Update agent calls to use separated architecture
   - Set up proper source filtering
   - Test with a real article

## Cost Analysis

### Current Monthly Spend: £200
- Claude: £180
- ChatGPT Plus: £20

### This Covers:
- ✅ All research capabilities
- ✅ Competitor analysis
- ✅ Content writing
- ✅ Voice calibration
- ✅ Basic citations (with free tools)

### Only Add Tools When:
- Article volume exceeds 10/month (add SEO tools)
- Citation complexity increases (add Sourcely)
- You need specific integrations (add APIs)

## Workflow Example with Current Tools

```bash
# Step 1: SEO Research (manual with ChatGPT)
# Step 2: Academic Research (Semantic Scholar + Claude)
/research-academic "IGCSE admissions requirements"

# Step 4A: Competitor Analysis (ChatGPT Plus Deep Research)
# Copy results from ChatGPT manually

# Step 8a: Voice Calibration (Claude)
/voice-calibrate archive "urls"

# Step 9: Writing (Claude via Claude Code)
/write-final "outline.md" "voice.md"

# Step 11: Citations (Zotero + manual Harvard format)
```

Your current subscriptions are MORE than adequate to run the entire system effectively!