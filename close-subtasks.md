# Automation Rule — Parent Closure Guard

**Trigger:** Parent issue transitions to Done.

**Condition:** Search for subtasks where `statusCategory != Done`.

**If open subtasks exist:** block/revert parent completion and comment with unresolved items.  
**If none exist:** allow completion and stamp closure metadata.

This rule protects reporting quality by preventing a completed parent from hiding unfinished execution work.
