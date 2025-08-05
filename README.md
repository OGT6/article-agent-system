# Article Agent v5.1 - Automated Research & Writing System

An AI-powered article creation system designed for achieving competitive dominance in search rankings for oxbridgeGCSEtutor.com. The system follows a rigorous 11-step workflow to create comprehensive, authoritative content that systematically outranks competitors.

## 📊 Project Status & Multi-AI Collaboration

**LIVE PROJECT STATUS: [Google Doc - Article Agent System Tracker](YOUR_GOOGLE_DOC_LINK_HERE)**

This repository contains:
- System documentation and code files
- Article outputs and drafts
- Configuration files

For current project status, active issues, and development progress:
- Both Claude and Claude Code can access the Google Doc directly
- Updates are reflected in real-time
- No manual syncing required

## Table of Contents

- [Overview](#overview)
- [System Requirements](#system-requirements)
- [Installation](#installation)
- [MCP Configuration](#mcp-configuration)
- [Available Commands](#available-commands)
- [11-Step Workflow](#11-step-workflow)
- [File Organization](#file-organization)
- [Quick Start Guide](#quick-start-guide)
- [Troubleshooting](#troubleshooting)
- [Best Practices](#best-practices)

## Overview

### Core Mission
Total competitive dominance in search rankings. Every article must become THE definitive resource that makes all other content obsolete. Success is measured by outranking competitors, not by arbitrary metrics.

### Target Audiences
1. **British Expat Parents**: Living abroad with children in international schools
2. **UK Independent School Parents**: Considering or enrolled in British private schools

### Key Features
- Forensic competitor analysis of top 5 ranking articles
- Mandatory voice calibration for authentic writing style
- Harvard academic referencing (minimum 15-20 sources)
- SEO optimization for featured snippets and rich results
- Strategic internal/external linking architecture
- Article series management for comprehensive topics
- MCP integration for enhanced automation

## System Requirements

- Claude Code CLI installed and configured
- Node.js (for MCP servers)
- Git for version control
- Internet connection for research and web access
- macOS or Linux (Windows via WSL)

## Installation

1. Clone or download the Article Agent system
2. Navigate to the project directory:
   ```bash
   cd "/Users/stephenkailey/Documents/Claude Agents/Article Agent"
   ```
3. Verify MCP configuration:
   ```bash
   claude mcp list
   ```
4. Initialize the folder structure:
   ```bash
   /setup-folders
   ```

## MCP Configuration

The system includes three MCP servers configured in `.mcp.json`:

### Memory Server
- **Purpose**: Knowledge graph for tracking research findings and entities
- **Status**: ✓ Connected
- **Usage**: Automatically stores article research and relationships

### Filesystem Server
- **Purpose**: Enhanced file operations within the Article Agent directory
- **Access**: `/Users/stephenkailey/Documents/Claude Agents/Article Agent`
- **Status**: ✓ Connected

### Puppeteer Server
- **Purpose**: Web automation for competitor screenshots and analysis
- **Status**: ✓ Connected
- **Usage**: Capture competitor content for forensic analysis

### MCP Commands
```bash
# Check MCP status
claude mcp list

# Reload MCP configuration
claude reload

# Add new MCP server
claude mcp add <name> <command> [args...]

# Remove MCP server
claude mcp remove <name>
```

## Available Commands

### `/setup-folders`
Creates the standard project folder structure for organizing articles.
```
Article Agent/
├── core/           # System files
└── articles/       # Article projects
    └── [topic]/    
        ├── research/
        ├── planning/
        ├── drafts/
        └── final/
```

### `/voice-calibrate` (MANDATORY)
Analyzes writing style before content creation.
```bash
# For existing content clusters
/voice-calibrate archive "url1.com, url2.com, url3.com" "topic"

# For new topic areas
/voice-calibrate sample "sample1.com, sample2.com" "topic"
```

### `/research-article`
Executes the complete 11-step workflow from research to final output.
```bash
/research-article "How do IGCSE grades convert to US GPA?" "both"
```

### `/seo-analysis`
Conducts keyword research and competitive SERP analysis.
```bash
/seo-analysis "IGCSE curriculum" "international schools, British education"
```

### `/gap-analysis`
Analyzes internal content portfolio and external competitors.
```bash
/gap-analysis "IGCSE subjects" "url1.com, url2.com"
```

### `/outline-create`
Generates article structure based on research.
```bash
/outline-create "research.json" "gap-analysis.json"
```

### `/write-final`
Writes the complete article with calibrated voice.
```bash
/write-final "outline.md" "voice-analysis.md"
```

### `/voice-polish`
Refines existing content without redoing research.
```bash
/voice-polish "draft.md" "archive-urls.txt"
```

### `/internal-linking`
Creates WordPress-ready internal link placement instructions.
```bash
/internal-linking "article.md" "archive-urls.txt"
```

## 11-Step Workflow

### Step 1: SEO Research & Competitive Forensics
- Identify target keywords and SERP landscape
- Analyze top 5 competitors (why they rank)
- Document dominance requirements
- Set outranking targets

### Step 2: Deep Research Phase 1
- Academic sources only (.gov, .edu)
- Peer-reviewed journals
- Official statistics
- No competitor content

### Step 3: Article Outline Creation
- Quick Answer (150-200 words for snippets)
- Full comprehensive exploration
- Both audience segments addressed

### Step 4: Comprehensive Gap Analysis
- Part A: Internal content audit (prevent cannibalization)
- Part B: External competitor analysis
- Part C: Integrated dominance strategy

### Step 5: User Approval Gate
- Present outline and research
- Incorporate modifications
- Confirm requirements

### Step 6: Deep Research Phase 2
- Fill knowledge gaps
- Additional academic sources
- 15-20 quality references minimum

### Step 7: Outline Update
- Refine structure
- Add new sections
- Strengthen differentiation

### Step 8: Final Approval Gate
- Present comprehensive outline
- Obtain writing approval

### Step 8a: Voice Calibration (MANDATORY)
- Execute `/voice-calibrate` command
- Create assignment-specific voice document
- Must complete before writing

### Step 9: Article Writing
- Dominate from first sentence
- Exceed competitors in every section
- Original frameworks and tools
- Superior user experience

### Step 10: Strategic Internal Linking
- WordPress-ready HTML
- Exact placement instructions
- Topic authority building

### Step 11: Harvard Reference List
- Complete bibliography
- Alphabetical by surname
- Include DOIs

## File Organization

```
Article Agent/
├── README.md               # This file
├── .mcp.json              # MCP configuration
├── core/                  # System files
│   ├── CLAUDE.md         # Master documentation
│   ├── setup-folders.md
│   ├── voice-calibrate.md
│   ├── research-article.md
│   ├── seo-analysis.md
│   ├── gap-analysis.md
│   ├── outline-create.md
│   ├── write-final.md
│   ├── voice-polish.md
│   └── internal-linking.md
│
└── articles/              # Article projects
    └── [topic-slug]/      # Individual articles
        ├── research/      # SEO analysis, competitor research
        ├── planning/      # Outlines, voice analysis
        ├── drafts/        # Work in progress
        └── final/         # Completed deliverables
```

### Naming Conventions
- Topic slugs: lowercase, hyphenated (e.g., `igcse-vs-gcse`)
- Files: descriptive names with dates where relevant
- Voice analysis: `voice-analysis-[topic]-[date].md`

## Quick Start Guide

### Creating Your First Article

1. **Set up the workspace**:
   ```bash
   /setup-folders
   ```

2. **Choose your topic and run initial SEO analysis**:
   ```bash
   /seo-analysis "your topic keyword" "related keywords"
   ```

3. **Conduct gap analysis** (if you have existing content):
   ```bash
   /gap-analysis "topic" "archive-url1.com, archive-url2.com"
   ```

4. **Execute the complete workflow**:
   ```bash
   /research-article "Article Title as Question?" "both|expat|uk"
   ```

5. **During the workflow, provide**:
   - Archive URLs or sample URLs for voice calibration
   - Approval at gates (Steps 5 and 8)
   - Any specific requirements

### Working with Existing Drafts

To polish an existing draft:
```bash
/voice-polish "path/to/draft.md" "archive-url1.com, archive-url2.com"
```

To add internal linking:
```bash
/internal-linking "path/to/article.md" "archive-urls.txt"
```

## Troubleshooting

### Common Issues and Solutions

#### MCP Server Connection Issues
```bash
# Check server status
claude mcp list

# Reload configuration
claude reload

# Reset and reconnect
claude mcp remove <server-name>
claude mcp add <server-name> <command> [args...]
```

#### Voice Calibration Errors
- Ensure URLs are accessible and valid
- Provide 3-5 archive links for best results
- Check that archive content matches topic area

#### Research Phase Challenges
- Focus on .gov and .edu domains
- Use academic search engines (Google Scholar)
- Verify source dates (prefer within 5 years)

#### Writing Quality Issues
- Review voice calibration document during writing
- Check against quality assurance checklist
- Ensure British spelling throughout
- No em dashes (use commas or parentheses)

#### File Organization Problems
- Always use `/setup-folders` first
- Follow naming conventions strictly
- Keep related files in same topic folder

### Error Messages

**"No archive URLs provided"**
- Solution: Provide URLs during approval gates
- Use sample URLs for new topic areas

**"MCP server not connected"**
- Solution: Run `claude reload`
- Check `.mcp.json` configuration

**"File not found"**
- Solution: Use absolute paths
- Verify file exists with `ls` command

## Best Practices

### Research Excellence
1. Always verify source credibility
2. Prioritize recent data (within 5 years)
3. Balance sources between both audiences
4. Exclude all competitor content

### Writing Standards
1. Complete voice calibration before writing
2. Reference voice document frequently
3. Aim for 2-3x competitor word count
4. Include unique frameworks/tools
5. Optimize for featured snippets

### SEO Optimization
1. Question format titles
2. Comprehensive H2/H3 structure
3. Strategic table usage (when it reduces cognitive load)
4. 8-12 external links to authoritative sources
5. No links to competitors

### Quality Assurance
1. Run through complete checklist
2. Verify all 11 steps completed
3. Check British spelling
4. Ensure no em dashes used
5. Confirm Harvard citations

### Competitive Dominance
1. Address EVERY competitor topic + 50% more
2. Double the authoritative sources
3. Provide unique insights found nowhere else
4. Create superior user experience
5. Make other articles feel obsolete

## Version History

- **v5.1** (Current): Workflow efficiency optimization, MCP integration
- **v5.0**: Article series management, external linking strategy
- **v4.0**: Voice calibration requirements, gap analysis
- **v3.0**: Competitive dominance framework
- **v2.0**: Dual audience targeting
- **v1.0**: Initial system release

## Support

For issues or questions:
1. Check troubleshooting section above
2. Review core/CLAUDE.md for detailed documentation
3. Verify MCP server status
4. Ensure latest version of Claude Code

---

*Article Agent v5.1 - Achieving Position #1 Through Systematic Content Superiority*