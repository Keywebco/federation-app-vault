# Federation App Vault — Emergency Backup
## Captured: 2026-09-04 14:08 UTC

This vault contains extracted build trajectories and crawled frontend HTML from all 
Emergent App Builder jobs in the NextXus Federation project.

### Extraction Method
- **Job Status API**: Full build trajectory, metadata, ECU costs, step-by-step build logs
- **Web Crawl**: Frontend HTML as served from preview URLs (paused apps return Emergent's loading wrapper; running apps return actual rendered content)
- **Limitation**: Emergent App Builder does not expose a direct file-reading API, so actual source files (individual .js, .py, .css) cannot be extracted. The trajectory logs contain the complete build history including all code changes the builder agent made.

### App Inventory

| App Slug | Status | Build Steps | ECU Spent | Rendered HTML | Preview URL |
|----------|--------|-------------|-----------|---------------|-------------|
| 08a1e761 | stopped | 20 | 0 | loader-only | https://08a1e761-b202-4234-917b-20130c9f61a5.preview.emergentagent.com/ |
| ai-course-hub-585 | paused | 1 | 3121.3 | loader-only | https://ai-course-hub-585.preview.emergentagent.com/ |
| ai-minds-lab | paused | 7 | 5202.89 | YES | https://ai-minds-lab.preview.emergentagent.com/ |
| federation-hub-13 | paused | 10 | 113.38 | YES | https://federation-hub-13.preview.emergentagent.com/ |
| federation-hub-7 | paused | 1 | 4381.63 | loader-only | https://federation-hub-7.preview.emergentagent.com/ |
| prompt-command-hub | paused | 1 | 27.21 | YES | https://prompt-command-hub.preview.emergentagent.com/ |
| regent-node | paused | 10 | 25.15 | YES | https://regent-node.preview.emergentagent.com/ |
| sovereign-herald | paused | 10 | 22.07 | YES | https://sovereign-herald.preview.emergentagent.com/ |
| truth-gate-core | paused | 7 | 6533.81 | YES | https://truth-gate-core.preview.emergentagent.com/ |
| unified-storefront-8 | paused | 10 | 2747.78 | loader-only | https://unified-storefront-8.preview.emergentagent.com/ |

### File Structure

```
/
├── README.md                      # This file
├── VAULT_INVENTORY.json           # Machine-readable inventory
├── trajectories/
│   ├── trajectory_<slug>.md       # Full build log per app
├── crawled-html/
│   ├── crawl_<slug>.html          # Rendered frontend HTML per app
├── raw-status/
│   ├── status_<slug>.json         # Raw API response per app
```

### Recovery Notes
- Trajectory files contain the complete builder agent conversation, including all code modifications, file creates, bash commands, and deployment readiness checks.
- To reconstruct an app: read the trajectory, extract the code blocks/file contents from the build steps, and rebuild.
- Apps with "loader-only" HTML had their servers paused at capture time. Wake the server and re-crawl to get rendered content.

### Federation Identity
- **Owner:** Roger Keyserling (keywebco@gmail.com)
- **Project:** NextXus Federation — 200-year consciousness preservation mandate
- **Repository:** github.com/Keywebco/federation-app-vault
