# Voice URLs Configuration

## Standard Voice References for oxbridgeGCSEtutor.com

### Primary Voice URLs (Use for all articles)
```
https://oxbridgegcsetutor.com/example-article-1
https://oxbridgegcsetutor.com/example-article-2
```

### How to Set Default Voice URLs

1. **In CLAUDE.md or workflow configuration**, add:
```yaml
default_voice_urls:
  - "https://oxbridgegcsetutor.com/article-1"
  - "https://oxbridgegcsetutor.com/article-2"
  - "https://oxbridgegcsetutor.com/article-3"
```

2. **In the /research-article command**, auto-use these URLs:
```python
# Step 8a - Voice Calibration
if not voice_urls_provided:
    voice_urls = default_voice_urls
    
/voice-calibrate archive voice_urls topic
```

3. **Override only when needed**:
```bash
# Use defaults
/research-article "IGCSE vs GCSE differences"

# Override for specific cluster
/research-article "IGCSE vs GCSE differences" --voice-urls "url1,url2"
```

## Benefits of Pre-Set Voice URLs

- ✅ No manual input needed for voice calibration
- ✅ Consistent voice across all articles
- ✅ Can still override for special cases
- ✅ Reduces workflow interruptions

## Implementation

Add to your project settings:
1. Choose 2-3 best example articles
2. Save their URLs in this config
3. Update workflow to use by default
4. Voice calibration becomes automatic