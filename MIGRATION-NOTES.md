# Migration Notes - GitHub + Google Docs Hybrid Approach

## Date: 2025-01-30

### What Changed
- PROJECT-TRACKER moved from GitHub to Google Docs for live multi-AI access
- GitHub repository retained for code, documentation, and version control

### New Structure

#### Google Docs (Live Status)
- **Document**: Article Agent System - Live Project Tracker
- **Purpose**: Real-time project status accessible by all AIs
- **Access**: Both Claude (via Projects) and Claude Code (via WebFetch)
- **Updates**: Live - no syncing needed

#### GitHub Repository (Code & Docs)
- **Repository**: https://github.com/OGT6/article-agent-system
- **Contains**:
  - `/core/` - System documentation (CLAUDE.md, commands)
  - `/articles/` - Article outputs and drafts
  - `.mcp.json` - MCP configuration
  - `README.md` - Points to Google Doc for live status
  
### How to Update Status
1. Open Google Doc directly
2. Make changes - both AIs see updates immediately
3. No git commits needed for status updates

### How to Update Code/Docs
1. Make changes locally
2. Git add, commit, push as normal
3. Code changes stay in version control

### Benefits
- ✅ Live status updates without git commits
- ✅ Both AIs read same real-time document
- ✅ Code stays in proper version control
- ✅ Clear separation of concerns