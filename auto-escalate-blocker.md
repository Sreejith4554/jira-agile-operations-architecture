# Automation Rule — Escalate Stale Blocker

**Trigger:** Scheduled, every weekday morning  
**JQL condition:** `labels = blocker AND statusCategory != Done AND updated <= -24h`  
**Actions:**
1. Add label `stale-blocker`.
2. Comment with the next required action and owner reminder.
3. Notify assignee and dependency owner.
4. If priority is Highest, notify project lead / PMO channel.
5. Write `Escalated At` timestamp.

**Guardrail:** Do not repeatedly notify more than once per 24-hour window.
