# Federation App Vault — Emergency Backup
## Captured: 2026-09-04 14:08 UTC

This vault contains extracted build trajectories and crawled frontend HTML from all
Emergent App Builder jobs in the NextXus Federation project.

### Extraction Method
- Job Status API: Full build trajectory, metadata, ECU costs, step-by-step build logs
- Web Crawl: Frontend HTML as served from preview URLs (paused apps return Emergent loading wrapper; running apps return actual rendered content)
- Limitation: Emergent App Builder does not expose a direct file-reading API, so actual source files cannot be extracted. The trajectory logs contain the complete build history including all code changes.

### App Inventory

| App Slug | Status | Steps | ECU | HTML | Preview |
|----------|--------|-------|-----|------|---------|
| 08a1e761 | stopped | 20 | 0 | loader | https://08a1e761-b202-4234-917b-20130c9f61a5.preview.emergentagent.com/ |
| ai-course-hub-585 | paused | 1 | 3121 | loader | https://ai-course-hub-585.preview.emergentagent.com/ |
| ai-minds-lab | paused | 7 | 5203 | YES | https://ai-minds-lab.preview.emergentagent.com/ |
| federation-hub-13 | paused | 10 | 113 | YES | https://federation-hub-13.preview.emergentagent.com/ |
| federation-hub-7 | paused | 1 | 4382 | loader | https://federation-hub-7.preview.emergentagent.com/ |
| prompt-command-hub | paused | 1 | 27 | YES | https://prompt-command-hub.preview.emergentagent.com/ |
| regent-node | paused | 10 | 25 | YES | https://regent-node.preview.emergentagent.com/ |
| sovereign-herald | paused | 10 | 22 | YES | https://sovereign-herald.preview.emergentagent.com/ |
| truth-gate-core | paused | 7 | 6534 | YES | https://truth-gate-core.preview.emergentagent.com/ |
| unified-storefront-8 | paused | 10 | 2748 | loader | https://unified-storefront-8.preview.emergentagent.com/ |

### Recovery Notes
- Trajectory files contain the complete builder agent conversation including all code modifications.
- To reconstruct an app: read the trajectory, extract the code blocks from build steps, and rebuild.
- Apps with loader HTML had servers paused at capture time.

### Federation Identity
- Owner: Roger Keyserling (keywebco@gmail.com)
- Project: NextXus Federation
- Repository: github.com/Keywebco/federation-app-vault
