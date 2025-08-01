# /setup-folders

## Purpose
Organize the Article Agent workspace with a structured folder system for better file management and scalability.

## Usage
```
/setup-folders
```

## Folder Structure Created

```
Article Agent/
├── core/                           # Core system files
│   ├── CLAUDE.md                  # Main system documentation
│   ├── research-article.md        # Article creation command
│   ├── voice-calibrate.md         # Voice calibration command
│   ├── voice-polish.md            # Voice polish command
│   ├── seo-analysis.md            # SEO analysis command
│   ├── gap-analysis.md            # Gap analysis command
│   ├── outline-create.md          # Outline creation command
│   ├── write-final.md             # Final writing command
│   ├── internal-linking.md        # Internal linking command
│   └── setup-folders.md           # This file
│
└── articles/                       # All article projects
    └── [topic-name]/              # Individual article folders
        ├── research/              # Research documents
        │   ├── seo-analysis.md
        │   ├── gap-analysis.md
        │   └── sources.md
        ├── planning/              # Planning documents
        │   ├── outline.md
        │   ├── voice-analysis.md
        │   └── content-map.md
        ├── drafts/                # Article drafts
        │   ├── draft-v1.md
        │   ├── draft-polished.md
        │   └── draft-final.md
        └── final/                 # Final deliverables
            ├── article-final.md
            ├── internal-linking.md
            └── references.md
```

## Implementation Process

### Step 1: Create Core Folders
```bash
mkdir -p "Article Agent/core"
mkdir -p "Article Agent/articles"
```

### Step 2: Move Core Files
Move all system documentation and slash commands to the core folder:
- CLAUDE.md → core/CLAUDE.md
- All slash command files (*.md) → core/
- Keep only article-specific files in root temporarily

### Step 3: Update Path References
Update all commands to use new paths:
- Article creation saves to: `articles/[topic-slug]/`
- Core commands reference: `core/[command].md`
- Templates stored in: `core/templates/`

### Step 4: Create Article Subfolders
When `/research-article` is run, automatically create:
```bash
mkdir -p "articles/[topic-slug]/research"
mkdir -p "articles/[topic-slug]/planning"
mkdir -p "articles/[topic-slug]/drafts"
mkdir -p "articles/[topic-slug]/final"
```

## Path Updates for Commands

### /research-article
```markdown
# Old paths:
/Users/stephenkailey/Documents/Claude Agents/Article Agent/[topic]-seo-analysis.md

# New paths:
/Users/stephenkailey/Documents/Claude Agents/Article Agent/articles/[topic-slug]/research/seo-analysis.md
```

### /voice-calibrate
```markdown
# Old paths:
/Users/stephenkailey/Documents/Claude Agents/Article Agent/voice-analysis-[topic]-[date].md

# New paths:
/Users/stephenkailey/Documents/Claude Agents/Article Agent/articles/[topic-slug]/planning/voice-analysis.md
```

### /write-final
```markdown
# Old paths:
/Users/stephenkailey/Documents/Claude Agents/Article Agent/[topic]-final-article.md

# New paths:
/Users/stephenkailey/Documents/Claude Agents/Article Agent/articles/[topic-slug]/final/article-final.md
```

## Benefits

1. **Organization**: Clear separation between system files and article content
2. **Scalability**: Easy to manage multiple article projects
3. **Version Control**: Each article has its own folder for drafts
4. **Collaboration**: Easier to share specific article folders
5. **Backup**: Simple to archive completed articles

## Migration Script

For existing files, use this migration pattern:
```bash
# Move core files
mv CLAUDE.md core/
mv *-command.md core/
mv setup-folders.md core/

# Create article folders for existing content
mkdir -p articles/igcse-admissions/
mv igcse-admissions-*.md articles/igcse-admissions/

# Organize by type
mv articles/igcse-admissions/*-outline.md articles/igcse-admissions/planning/
mv articles/igcse-admissions/*-final-article.md articles/igcse-admissions/final/
mv articles/igcse-admissions/*-analysis.md articles/igcse-admissions/research/
```

## Naming Conventions

### Topic Slugs
- Use lowercase
- Replace spaces with hyphens
- Remove special characters
- Keep under 50 characters

Examples:
- "IGCSE Admissions Guide" → `igcse-admissions-guide`
- "A-Level vs IB Comparison" → `a-level-vs-ib-comparison`
- "UK University Applications 2025" → `uk-university-applications-2025`

### File Naming Within Articles
- Research: `seo-analysis.md`, `competitor-1.md`, `sources.md`
- Planning: `outline-v1.md`, `voice-analysis.md`
- Drafts: `draft-2025-01-30.md`, `draft-polished.md`
- Final: `article-final.md`, `internal-linking.md`

## Integration with Existing Commands

All existing slash commands will be updated to:
1. Check for core folder existence
2. Create article subfolders automatically
3. Save files to appropriate locations
4. Reference files using new paths

## Error Handling

- If folders already exist, skip creation
- If files already exist in destination, prompt for overwrite
- Log all file movements for rollback capability
- Maintain backward compatibility during transition

## Success Confirmation

After running `/setup-folders`, you'll see:
```
✓ Core folder created
✓ Articles folder created
✓ X system files moved to core/
✓ Y article files organized
✓ Path references updated in commands
✓ Folder structure ready for use
```

## Future Enhancements

1. **Auto-archiving**: Move completed articles to archive after 90 days
2. **Templates folder**: Store reusable templates in core/templates/
3. **Assets folder**: Add images/resources folder for each article
4. **Metadata files**: Add JSON metadata for each article project
5. **Search index**: Build searchable index of all articles