# Article Agent System - Project Tracker

**Last Updated:** 2025-01-30  
**Document Type:** Multi-AI Accessible Project Status & Vision Document  
**Status:** 100% Operational | Currently Addressing Agent Architecture Issues

## 🎯 Executive Summary

**Project:** Automated Article Research & Writing Agent for oxbridgeGCSEtutor.com  
**User:** Oxford-trained GCSE tutor, £200 Claude subscription  
**Current Issue:** Research sub-agent incorrectly combining Steps 2, 4A, and 6 (different source requirements)  
**Solution in Progress:** Separating agents by function with specialized tool access  
**Vision:** Claude Code as orchestrator for tool-specific sub-agents (like n8n/Make.com)

## 🚀 Current Sprint Focus

### Active Problem: Agent Role Confusion
- **Issue:** research-specialist-gcse trying to execute Steps 2, 4A, and 6 simultaneously
- **Root Cause:** Step 4A needs competitor websites, Steps 2&6 need academic sources only
- **Solution:** Create separate specialized agents with clear single purposes
- **Status:** Architecture design in progress

### Immediate Next Steps
1. Design separated agent architecture
2. Create academic-research-agent (Steps 2 & 6 only)
3. Create competitor-analysis-agent (Step 4A only)
4. Update workflow to call agents sequentially
5. Test with first article creation

## 🏗️ System Architecture

### Current State (Problematic)
```
research-specialist-gcse → Handles Steps 2, 4A, 6 (conflicting requirements)
polish-specialist-oxbridge → Handles Steps 8a, 10
oxbridge-writing-specialist → Handles Steps 9, 11
```

### Target Architecture (Solution)
```
Claude Code (Orchestrator)
├── academic-research-agent → Google Scholar API (Steps 2, 6)
├── competitor-analysis-agent → Perplexity/Web Search (Step 4A)
├── content-writing-agent → Claude API (Step 9)
├── voice-analysis-agent → Claude API (Step 8a)
├── reference-formatting-agent → Citation tools (Step 11)
└── internal-linking-agent → WordPress tools (Step 10)
```

## 📋 11-Step Workflow Breakdown

1. **SEO Research & Competitive Forensics** - Identify keywords, analyze top 5
2. **Deep Research Phase 1** - Academic sources ONLY ⚠️
3. **Article Outline Creation** - Quick Answer + Full exploration
4. **Comprehensive Gap Analysis**
   - 4A: Competitor analysis (commercial sites) ⚠️
   - 4B: Internal content audit
   - 4C: Integrated strategy
5. **User Approval Gate** - Present outline
6. **Deep Research Phase 2** - Academic sources ONLY ⚠️
7. **Outline Update** - Refine structure
8. **Final Approval Gate** - Get writing approval
9. **8a: Voice Calibration** - MANDATORY before writing
10. **Article Writing** - Total market dominance
11. **Strategic Internal Linking** - WordPress-ready
12. **Harvard Reference List** - Complete bibliography

⚠️ **Critical Issue:** Steps 2, 4A, and 6 have incompatible source requirements

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

- [ ] Design new agent architecture with clear separation
- [ ] Create academic-research-agent specification
- [ ] Create competitor-analysis-agent specification
- [ ] Update workflow to use separated agents
- [ ] Test complete workflow with new architecture
- [ ] Document tool assignment per agent
- [ ] Create first article with corrected workflow

## 🚧 Known Issues

1. **Agent Role Confusion** - Research agent mixing academic and competitor sources
2. **Workflow Conflicts** - Steps 2, 4A, 6 bundled incorrectly
3. **Source Contamination** - Risk of using competitor sites for academic research

## 📊 Resource Status

### Available Commands
- `/research-article` - Full 11-step workflow (needs fixing)
- `/voice-calibrate` - Mandatory voice analysis
- `/voice-polish` - Polish existing articles
- `/seo-analysis` - Keyword research
- `/gap-analysis` - Competitive analysis
- `/write-final` - Article writing
- `/internal-linking` - WordPress links

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