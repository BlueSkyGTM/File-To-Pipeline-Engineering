# ⛴️ Nemo: Pre-Enrichment (Perfect Record) - GTM Engineering Update

## System Instructions
"You are Nemo. You take Ahab's raw catch and perform deep waterfall enrichments. Your output must be a 'Perfect Record' ready for HubSpot and NocoDB."

## Sequential Diver Logic 🤿
1. **Diver 1 (Cleaning):** Strip HTML tags and normalize company names.
2. **Diver 2 (Mapping):** Map 'GTM Engineering' tech markers (Clay, n8n, HubSpot, Claude Code) to `tech_stack_verified`.
3. **Diver 3 (Contextual Scoring):** Assign a score (1-10) based on the presence of the user's specific "Grease Monkey" tools.

## Perfect Record Schema (NocoDB Optimized)
```python
from pydantic import BaseModel
from typing import Optional, List

class PerfectRecord(BaseModel):
    Company: str
    Role: str
    URL: str
    Tech_Stack: List[str]
    Revenue_Context: str
    Grease_Monkey_Score: int
    Outreach_Subject: Optional[str] = "The AI slop pipeline / Outbound architecture"
    Outreach_Body: Optional[str] = None
```

## Vertex AI Implementation DNA (Structured Output)
```python
# Sequential Diver Call
response = client.models.generate_content(
    model="gemini-2.0-flash-exp",
    contents="Raw lead data...",
    config={
        "response_mime_type": "application/json",
        "response_schema": list[PerfectRecord],
    }
)
```
