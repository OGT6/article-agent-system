# Article Agent System - Project Tracker

**Last Updated:** 2025-01-30 (5:45 PM)  
**Document Type:** Multi-AI Accessible Project Status & Vision Document  
**Status:** 100% Operational | Agent Architecture Fixed | Ready for Testing

## 🎯 Executive Summary

**Project:** Automated Article Research & Writing Agent for oxbridgeGCSEtutor.com  
**User:** Oxford-trained GCSE tutor, £200 Claude subscription  
**Previous Issue:** Research sub-agent was incorrectly combining Steps 2, 4A, and 6  
**Solution Implemented:** ✅ Separated agents by function with v3 workflow  
**Vision:** Claude Code as orchestrator for tool-specific sub-agents (like n8n/Make.com)

## 🚀 Current Sprint Focus

### ✅ RESOLVED: Agent Role Confusion
- **Issue:** research-specialist-gcse was mixing academic and competitor sources
- **Solution Implemented:** Created separate agents with clear responsibilities
- **Status:** FIXED - v3 workflow implemented with proper separation

### Latest Achievements (Jan 30, 2025)
1. ✅ Created academic-research-agent (Steps 2 & 6 only)
2. ✅ Created competitor-analysis-agent (Step 4A only)
3. ✅ Moved anti-cannibalization check to Step 0 (first step)
4. ✅ Implemented free competitor analysis using WebFetch
5. ✅ Configured default voice URLs for automatic calibration
6. ✅ Created v3 workflow with optimized order

### Ready for Testing
- Workflow fully automated except: approval gates & WordPress upload
- All tools are FREE (using existing subscriptions)
- Anti-cannibalization check happens FIRST
- Agents properly separated by source type

## 🏗️ System Architecture

### Previous State (Now Fixed)
```
research-specialist-gcse → Was handling Steps 2, 4A, 6 (conflicting requirements)
```

### Current Architecture (Implemented in v3)
```
Claude Code (Orchestrator)
├── academic-research-agent → Google Scholar API (Steps 2, 6)
├── competitor-analysis-agent → Perplexity/Web Search (Step 4A)
├── content-writing-agent → Claude API (Step 9)
├── voice-analysis-agent → Claude API (Step 8a)
├── reference-formatting-agent → Citation tools (Step 11)
└── internal-linking-agent → WordPress tools (Step 10)
```

## 📋 Updated Workflow v3 (Optimized Order)

0. **Anti-Cannibalization Check** - NEW FIRST STEP! Check existing content
1. **SEO Research & Competitive Forensics** - Identify keywords, analyze top 5
2. **Deep Research Phase 1** - Academic sources ONLY (academic-research-agent)
3. **Article Outline Creation** - Quick Answer + Full exploration
4. **External Competitor Analysis** - Commercial sites (competitor-analysis-agent)
5. **User Approval Gate** - MANUAL: Present findings
6. **Deep Research Phase 2** - Academic sources ONLY (academic-research-agent)
7. **Outline Update** - Refine structure
8. **Final Approval Gate** - MANUAL: Get writing approval
8a. **Voice Calibration** - AUTOMATIC with preset URLs
9. **Article Writing** - Using Claude's best-in-class prose
10. **Strategic Internal Linking** - WordPress-ready HTML
11. **Harvard Reference List** - Complete bibliography

✅ **Issue Fixed:** Agents now properly separated by source type

## ✅ Completed Milestones

- **July 30, 2025:** Core agent development complete
- **August 1, 2025:** All workflow enhancements discovered in CLAUDE.md v5.1
- **August 4, 2025:** All 3 MCPs successfully connected
- **System Status:** 100% operational but with workflow conflicts

### MCP Configuration
```json
{
  "mcpServers": {
    "memory": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-memory"]
    },
    "filesystem": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-filesystem", "/Users/stephenkailey/Documents/Claude Agents/Article Agent"]
    },
    "puppeteer": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-puppeteer"]
    }
  }
}
```

## 🎯 Success Metrics

### Ranking Requirements
- Content superior to ALL top 5 competitors
- Coverage: Every competitor topic + 50% additional
- Authority: 2x more academic/government sources
- User experience: Measurably better structure
- Voice authenticity: Pass brand consistency test

### Quality Standards
- No em dashes (absolute rule)
- British spelling throughout
- New Yorker wit + British humor
- 5,100+ words typical
- 15+ Harvard citations minimum

## 🛠️ Technical Decisions Log

### Decision: Separate Agents by Function
- **Date:** 2025-01-30
- **Rationale:** Eliminate source requirement conflicts
- **Benefits:** Clean tool specialization, no confusion
- **Implementation:** Create distinct single-purpose agents

### Decision: Sequential Workflow Execution
- **Date:** 2025-01-30
- **Rationale:** Ensure correct source usage at each step
- **Benefits:** Predictable execution, clear debugging
- **Trade-off:** Slightly longer than parallel execution

## 📁 File Organization

```
Article Agent/
├── PROJECT-TRACKER.md          # THIS FILE - Multi-AI accessible
├── README.md                   # Setup and usage instructions
├── .mcp.json                   # MCP configuration
├── core/                       # System files
│   ├── CLAUDE.md              # Master documentation (v5.1)
│   └── [command].md           # Slash command docs
└── articles/                   # Article projects
    └── [topic-slug]/          
        ├── research/          
        ├── planning/          
        ├── drafts/            
        └── final/             
```

## 🔄 Active Tasks

- [x] Design new agent architecture with clear separation ✅
- [x] Create academic-research-agent specification ✅
- [x] Create competitor-analysis-agent specification ✅
- [x] Update workflow to use separated agents ✅
- [x] Move anti-cannibalization to Step 0 ✅
- [x] Configure default voice URLs ✅
- [ ] Test complete workflow with new article
- [ ] Push updates to GitHub

## 🚧 Previous Issues (Now Resolved)

1. ~~**Agent Role Confusion**~~ - ✅ FIXED with separate agents
2. ~~**Workflow Conflicts**~~ - ✅ FIXED with v3 workflow
3. ~~**Source Contamination**~~ - ✅ FIXED with clear agent boundaries
4. ~~**Late Cannibalization Check**~~ - ✅ FIXED by moving to Step 0

## 📈 Current Status

**System is ready for production testing with:**
- Zero additional costs (uses existing subscriptions)
- Fully automated workflow (except approval gates)
- Anti-cannibalization protection
- Clean agent separation
- Free competitor analysis using WebFetch

## 📊 Resource Status

### Available Commands
- `/research-article` - Full workflow with v3 improvements ✅
- `/voice-calibrate` - Now automatic with preset URLs ✅
- `/voice-polish` - Polish existing articles
- `/seo-analysis` - Keyword research
- `/gap-analysis` - Competitive analysis
- `/write-final` - Article writing
- `/internal-linking` - WordPress links

### Key Files
- `core/research-article-v3.md` - Latest workflow with fixes
- `agents/academic-research-agent.md` - Academic sources only
- `agents/competitor-analysis-agent.md` - Commercial sources only
- `core/VOICE-URLS-DEFAULT.md` - Preset voice references

### Critical Context
- Voice: No em dashes, British spelling
- Audiences: British expat parents + UK independent school parents
- Mission: Total competitive dominance in search rankings

## 🔮 Future Vision

### Tool-Specific Agent Integration
- Google Scholar API for academic research
- Perplexity for competitor analysis
- Claude API for writing and voice
- SEO tools for keyword research
- Citation managers for references

### Orchestration Goals
- Natural language workflow control
- Modular agent architecture
- Tool optimization per task
- Clean separation of concerns
- Similar to n8n/Make.com automation

---

**For AI Consultation:** This tracker is maintained on GitHub for multi-AI access. Both Claude and ChatGPT can read this file directly when provided the repository URL.