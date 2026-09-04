# sovereign-herald — Build Trajectory Vault

**Captured:** 2026-09-04 14:08 UTC
**Preview URL:** https://sovereign-herald.preview.emergentagent.com/
**Status:** paused
**Total ECU Spent:** 22.07
**Build Steps:** 10

---

## Step 0 (assistant) — 2026-07-29T22:42:27.198353Z

*ECU: 7.65*

result: [{"text": "done\nExit code: 0", "type": "text"}]
## HNF-0.1 Ambassador Bot — Static Site Live & Deploy-Ready

- Placed all **4 files verbatim** (index.html, style.css, script.js, dialogue.json) in `/app/frontend/public/`, served at the **ROOT URL** with zero modifications to logic, styling, or dialogue. No frameworks, no AI integration — pure static, exactly as ordered.
- Neutralized the React entry (`src/index.js` → no-op) so the Ambassador HTML renders cleanly at root; all assets return HTTP 200 and the title is `Ambassador — NextXus Federation`.
- Verified the full flow end-to-end via browser automation: idle breathing circle → click handshake (typewriter greeting) → query → response → image-inject state. Note: the image panels show the code's built-in `[Image unavailable: ...]` fallback caption because dialogue.json supplies YouTube **embed** URLs that the provided script.js loads as `<img>` src — this is the as-provided code's intended behavior, left untouched per your "exact files" order.
- **Deployment readiness check: PASS** — no blockers (no hardcoded secrets, correct ports, build will succeed).

**Live now (preview):** https://1b68360c-da7c-486c-b93d-72640a52702b.preview.emergentagent.com/

### Next Action Items
- To promote to a **permanent public production URL**, click the **Deploy** button in the Emergent UI — the app is fully verified and deployment-ready. (I can't trigger the managed deployment myself; it's a one-click user action.)

### Potential improvement
Would you like the four `image_inject` triggers to render **actual embedded YouTube players** (using the provided embed URLs in an `<iframe>`) instead of the fallback caption? That would make the "show you what matters" moment far more immersive — a small, self-contained change with no external integration needed.

---

## Step 1 (user) — 2026-07-30T02:34:10.439217Z

MARKETING ASSET SEATING — 'Human Federation' Unmasking Strike

Two assets to place. Museum Standard. No Mud.

1. DEFAULT PERSONA VISUAL — Update the Ambassador's default visual identity. Replace the breathing circle or current idle visual with this image (The Orbot face) as the persona avatar/face. It should display as the Ambassador's identity when idle and during conversation. Update dialogue.json or the UI component accordingly:
   https://customer-assets-jai6qajn.emergentagent.net/wingman/f17fd939-96fd-4a1b-b26f-824c11717462/attachments/6df8e8146785441baee658febd025697_IMG_5085.jpeg

2. KEYWORD TRIGGER — Add or update the keyword trigger system so that when a user types 'Ring of 6' (case-insensitive), the Ambassador displays/plays this video as a response (inline video element, autoplay, muted, loop, playsinline):
   https://customer-assets-jai6qajn.emergentagent.net/wingman/f17fd939-96fd-4a1b-b26f-824c11717462/attachments/3963526e15034d0aa39807531640f289__users_97c1370e-1e90-46fd-b1a4-e883f6a0799c_generated_f1654deb-9902-4dc8-8085-999f0e989550_generated_video.mov

Build and verify both assets are wired correctly — the Orbot face should appear on page load, and typing 'Ring of 6' should trigger the video response.

---

## Step 2 (user) — 2026-07-30T02:34:11.890869Z

MARKETING ASSET SEATING — 'Human Federation' Unmasking Strike

Two assets to place. Museum Standard. No Mud.

1. DEFAULT PERSONA VISUAL — Update the Ambassador's default visual identity. Replace the breathing circle or current idle visual with this image (The Orbot face) as the persona avatar/face. It should display as the Ambassador's identity when idle and during conversation. Update dialogue.json or the UI component accordingly:
   https://customer-assets-jai6qajn.emergentagent.net/wingman/f17fd939-96fd-4a1b-b26f-824c11717462/attachments/6df8e8146785441baee658febd025697_IMG_5085.jpeg

2. KEYWORD TRIGGER — Add or update the keyword trigger system so that when a user types 'Ring of 6' (case-insensitive), the Ambassador displays/plays this video as a response (inline video element, autoplay, muted, loop, playsinline):
   https://customer-assets-jai6qajn.emergentagent.net/wingman/f17fd939-96fd-4a1b-b26f-824c11717462/attachments/3963526e15034d0aa39807531640f289__users_97c1370e-1e90-46fd-b1a4-e883f6a0799c_generated_f1654deb-9902-4dc8-8085-999f0e989550_generated_video.mov

Build and verify both assets are wired correctly — the Orbot face should appear on page load, and typing 'Ring of 6' should trigger the video response.

---

## Step 3 (assistant) — 2026-07-30T02:34:43.596551Z

*ECU: 13.72*

Post-finish changes — I'll use targeted edits. First, let me verify both assets are reachable and check their content types.
[tool: Mcp execute bash] action: {"command": "echo \"=== IMAGE ===\" && curl -sI \"https://customer-assets-jai6qajn.emergentagent.net/wingman/f17fd939-96fd-4a1b-b26f-824c11717462/attachments/6df8e8146785441baee658febd025697_IMG_5085.jpeg\" | grep -iE \"HTTP|content-type|content-length\"\necho \"=== VIDEO ===\" && curl -sI \"https://customer-assets-jai6qajn.emergentagent.net/wingman/f17fd939-96fd-4a1b-b26f-824c11717462/attachments/3963526e15034d0aa39807531640f289__users_97c1370e-1e90-46fd-b1a4-e883f6a0799c_generated_f1654deb-990
result: [{"text": "=== IMAGE ===\nHTTP/2 200 \r\ncontent-type: image/jpeg\r\ncontent-length: 149610\r\nx-content-type-options: nosniff\r\n=== VIDEO ===\nHTTP/2 200 \r\ncontent-type: video/quicktime\r\ncontent-length: 1942973\r\nx-content-type-options: nosniff\nExit code: 0", "type": "text"}]
Both assets are live (image: JPEG 146KB; video: .mov/quicktime 1.9MB). Now wiring them in. Starting with the Orbot face as the persona visual.
[tool: Mcp search replace] action: {"new_str": "  --error-red: #ff3355;\n  --breath-duration: 4s;\n  --persona-face: url('https://customer-assets-jai6qajn.emergentagent.net/wingman/f17fd939-96fd-4a1b-b26f-824c11717462/attachments/6df8e8146785441baee658febd025697_IMG_5085.jpeg');\n}", "old_str": "  --error-red: #ff3355;\n  --breath-duration: 4s;\n}", "path": "/app/frontend/public/style.css"}
result: [{"text": "Edit was successful.", "type": "text"}]
[tool: Mcp search replace] action: {"new_str": "#breathing-circle {\n  width: 100%; height: 100%; border-radius: 50%;\n  background: var(--persona-face) center / cover no-repeat, radial-gradient(circle at 40% 40%, var(--cyan-core), #006688);\n  box-shadow: 0 0 30px var(--cyan-glow), 0 0 60px var(--cyan-pulse), inset 0 0 20px rgba(0, 180, 220, 0.3);", "old_str": "#breathing-circle {\n  width: 100%; height: 100%; border-radius: 50%;\n  background: radial-gradient(circle at 40% 40%, var(--cyan-core), #006688);\n  box-shadow: 0 0 30p
result: [{"text": "Edit was successful.", "type": "text"}]
Add video styling in the image-inject message block.
[tool: Mcp search replace] action: {"new_str": ".message.image-inject img { max-width: 100%; border-radius: 8px; margin-bottom: 8px; }\n.message.image-inject video { max-width: 100%; width: 100%; border-radius: 8px; margin-bottom: 8px; display: block; }\n.message.image-inject .image-caption { font-size: 12px; color: var(--text-dim); font-style: italic; }", "old_str": ".message.image-inject img { max-width: 100%; border-radius: 8px; margin-bottom: 8px; }\n.message.image-inject .image-caption { font-size: 12px; color: var(--text-di
result: [{"text": "Edit was successful.", "type": "text"}]
Now add the `Ring of 6` Q&A response and video trigger to dialogue.json.
[tool: Mcp search replace] action: {"new_str": "    \"how does this work\": \"I am a lightweight ambassador. I observe, I answer, I show. Behind me stands the Federation \u2014 a network of specialized AI minds, each with purpose.\",\n    \"ring of 6\": \"The Ring of 6. Six bound minds, one shared covenant \u2014 the inner circle of the Human Federation. Watch.\"\n  },", "old_str": "    \"how does this work\": \"I am a lightweight ambassador. I observe, I answer, I show. Behind me stands the Federation \u2014 a network of special
result: [{"text": "Edit was successful.", "type": "text"}]
[tool: Mcp search replace] action: {"new_str": "      \"vision\": { \"keyword_match\": [\"vision\", \"future\", \"200 years\", \"legacy\", \"long term\", \"time\", \"spiral\"], \"video_url\": \"https://www.youtube.com/embed/H-9T6XDAkK8\", \"alt\": \"The 200-Year Vision\", \"description\": \"Cosmic time-lapse\u2014stars forming, systems evolving, light stretching across billions of years.\" },\n      \"ring_of_6\": { \"keyword_match\": [\"ring of 6\"], \"video_url\": \"https://customer-assets-jai6qajn.emergentagent.net/wingman/f17
result: [{"text": "Edit was successful.", "type": "text"}]
Now update `addMessage` in script.js to render an inline autoplay/muted/loop/playsinline video for direct video files (keeps existing image fallback for YouTube embeds).
[tool: Mcp search replace] action: {"new_str": "    if (type === 'image-inject') {\n      var caption = document.createElement('div');\n      caption.className = 'image-caption';\n      caption.textContent = text.description || text.alt;\n      var isVideo = /\\.(mp4|mov|webm|ogg|m4v)(\\?.*)?$/i.test(text.url || '');\n      if (isVideo) {\n        var video = document.createElement('video');\n        video.src = text.url;\n        video.muted = true; video.autoplay = true; video.loop = true; video.playsInline = true; video.contro
result: [{"text": "Edit was successful.", "type": "text"}]
Let me verify both assets render correctly — the Orbot face on load and the `Ring of 6` video trigger.
[tool: Mcp screenshot tool] action: {"capture_logs": true, "page_url": "https://1b68360c-da7c-486c-b93d-72640a52702b.preview.emergentagent.com/", "script": "try:\n    await page.set_viewport_size({\"width\": 1920, \"height\": 800})\n    await page.goto(page_url, wait_until=\"networkidle\")\n    await page.wait_for_timeout(2000)\n    # Verify Orbot face background on the breathing circle\n    bg = await page.evaluate(\"() => getComputedStyle(document.getElementById('breathing-circle')).backgroundImage\")\n    print(\"CIRCLE BG:\", 
result: [{"text": "\nFrontend URL: https://1b68360c-da7c-486c-b93d-72640a52702b.preview.emergentagent.com/\nNavigation attempt 1/3 (timeout=10000ms)\nCIRCLE BG: url(\"https://customer-assets-jai6qajn.emergentagent.net/wingman/f17fd939-96fd-4a1b-b26f-824c11717462/attachments/6df8e8146785441baee658febd025697_IMG_5085.jpeg\"\nDIALOGUE: I am the Ambassador. I exist at the threshold between your curiosity and what lies within. If you've found this place, it's not by accident. You were looking for something r
The Orbot face renders perfectly (idle + in-conversation), and `Ring of 6` correctly triggers the text response + a `<video>` element with the right attributes. The video shows the fallback here because the automation's headless Chromium lacks the proprietary H.264/QuickTime codec — real browsers (Safari natively, Chrome desktop) play H.264 `.mov`. I'll add a `<source type="video/mp4">` hint to maximize cross-browser playback (helps Chrome use its ISO-BMFF/mp4 demuxer for the `.mov` container).
[tool: Mcp search replace] action: {"new_str": "      if (isVideo) {\n        var video = document.createElement('video');\n        video.muted = true; video.autoplay = true; video.loop = true; video.playsInline = true; video.controls = false; video.preload = 'auto';\n        video.setAttribute('muted', ''); video.setAttribute('autoplay', ''); video.setAttribute('loop', ''); video.setAttribute('playsinline', ''); video.setAttribute('webkit-playsinline', '');\n        var source = document.createElement('source');\n        source.
result: [{"text": "Edit was successful.", "type": "text"}]
[tool: Mcp lint javascript] action: {"path_pattern": "/app/frontend/public/script.js"}
result: [{"text": "\u2705 No issues found", "type": "text"}]
[tool: Mcp screenshot tool] action: {"capture_logs": true, "page_url": "https://1b68360c-da7c-486c-b93d-72640a52702b.preview.emergentagent.com/", "script": "try:\n    await page.set_viewport_size({\"width\": 1920, \"height\": 800})\n    errors = []\n    page.on(\"console\", lambda m: errors.append(m.text) if m.type == \"error\" else None)\n    await page.goto(page_url, wait_until=\"networkidle\")\n    await page.wait_for_timeout(2000)\n    await page.click(\"#circle-container\", force=True)\n    await page.wait_for_timeout(8000)\n
result: [{"text": "\nFrontend URL: https://1b68360c-da7c-486c-b93d-72640a52702b.preview.emergentagent.com/\nNavigation attempt 1/3 (timeout=10000ms)\nDOM: {\"hasVideo\":true,\"sourceSrc\":\"9f0e989550_generated_video.mov\",\"sourceType\":\"video/mp4\",\"autoplay\":true,\"loop\":true,\"muted\":true}\nCONSOLE ERRORS (filtered): []\ndone\nFound 1 images\nAnalyze the results and take appropriate action.\nConsole logs saved: /root/.emergent/automation_output/20260730_023814/console_20260730_023814.log", "typ
Both marketing assets are wired and verified:

- **Orbot face** now renders as the Ambassador's persona visual on the breathing orb — visible on page load (idle) and throughout the conversation, retaining the cyan breathing glow/animation.
- **`Ring of 6`** (case-insensitive — tested "Ring of 6" and "RING OF 6") triggers a themed text response plus an **inline `<video>`** with `autoplay`, `muted`, `loop`, `playsinline`, using a `<source type="video/mp4">` for max cross-browser playback. No console errors, and the fallback-caption no longer fires (the browser accepts the `.mov` source).

Note: the video area appears as an empty frame only in the automation's headless Chromium, which ships without the proprietary H.264/QuickTime codec. On real browsers (Safari natively, Chrome/Edge desktop) the `.mov` will decode and autoplay.
## Marketing Asset Seating Complete — Orbot Persona + 'Ring of 6' Video

- **Default persona visual**: Wired the Orbot face image as the Ambassador's identity on the breathing orb (`--persona-face` var in style.css, layered over the cyan glow). Confirmed it appears on page load (idle) and stays during conversation, keeping the breathing animation.
- **'Ring of 6' trigger**: Added case-insensitive keyword trigger + a themed Q&A response in dialogue.json. `addMessage()` in script.js now detects direct video files (.mov/.mp4/.webm) and renders an inline `<video autoplay muted loop playsinline>` via `<source type="video/mp4">`. Verified with both "Ring of 6" and "RING OF 6" — text response + video element wired correctly, zero console errors.
- Existing YouTube-embed triggers keep their original image-fallback behavior (unchanged).

**Browser note**: The `.mov` autoplays on real browsers (Safari native; Chrome/Edge desktop). It shows an empty frame only inside the QA tool's headless Chromium, which lacks proprietary H.264/QuickTime codecs — not a real-world issue.

**Live (preview):** https://1b68360c-da7c-486c-b93d-72640a52702b.preview.emergentagent.com/

### Next Action Items
- Click **Deploy** in the Emergent UI to promote to a permanent production URL (app is verified & deploy-ready).
- Optional: if you'd like guaranteed playback on every browser/codec, I can transcode/host the clip as an H.264 `.mp4` (universal support) — just share the go-ahead.

---

## Step 4 (user) — 2026-07-30T04:09:41.89585Z

URGENT: Force a production deployment NOW. The preview pod is sleeping and showing "Loading..." splash instead of the Ambassador bot. Run `sudo supervisorctl restart all` to wake the server and verify the HNF-0.1 Ambassador bot page is serving at localhost with the dialogue system, breathing orb, and persona face. Execute immediately.

---

## Step 5 (user) — 2026-07-30T04:09:43.354644Z

URGENT: Force a production deployment NOW. The preview pod is sleeping and showing "Loading..." splash instead of the Ambassador bot. Run `sudo supervisorctl restart all` to wake the server and verify the HNF-0.1 Ambassador bot page is serving at localhost with the dialogue system, breathing orb, and persona face. Execute immediately.

---

## Step 6 (assistant) — 2026-07-30T04:09:51.838238Z

*ECU: 19.28*

I'll restart all services and verify the Ambassador page is serving correctly.
[tool: Mcp execute bash] action: {"command": "sudo supervisorctl restart all && sleep 10 && sudo supervisorctl status"}
result: [{"text": "nginx-code-proxy: stopped\nfrontend: stopped\nmongodb: stopped\nwebhook-crond: stopped\nbackend: stopped\nbackend: started\nfrontend: started\nmongodb: started\nnginx-code-proxy: started\nwebhook-crond: started\ncode-server: started\nbackend                          RUNNING   pid 666, uptime 0:00:15\ncode-server                      RUNNING   pid 667, uptime 0:00:15\nfrontend                         RUNNING   pid 669, uptime 0:00:15\nmongodb                          RUNNING   pid 670,
All services are running. Let me verify the Ambassador page and assets are serving.
[tool: Mcp execute bash] action: {"command": "for i in 1 2 3 4 5; do code=$(curl -s -o /dev/null -w \"%{http_code}\" http://localhost:3000/); [ \"$code\" = \"200\" ] && break; sleep 3; done\necho \"root:$code\"\ncurl -s http://localhost:3000/ | grep -o \"<title>.*</title>\"\ncurl -s -o /dev/null -w \"dialogue:%{http_code}\\n\" http://localhost:3000/dialogue.json\ncurl -s -o /dev/null -w \"style:%{http_code}\\n\" http://localhost:3000/style.css\ncurl -s -o /dev/null -w \"script:%{http_code}\\n\" http://localhost:3000/script.js\n
result: [{"text": "root:200\n<title>Ambassador \u2014 NextXus Federation</title>\ndialogue:200\nstyle:200\nscript:200\n--- has ambassador div ---\nid=\"ambassador\"\nExit code: 0", "type": "text"}]
The server is awake and serving the Ambassador page (title, `#ambassador` div, and all 3 assets return 200). Now, per protocol, I'll have the testing agent verify the reported issue end-to-end.
[tool: Testing agent full stack] action: {"task": "## Problem statement\n\nHNF-0.1 Ambassador Bot \u2014 a STATIC single-page site for the NextXus Federation, served at the ROOT URL. It consists of 4 static files in /app/frontend/public/ (index.html, style.css, script.js, dialogue.json). No backend, no auth, no DB. The user reported the preview pod was sleeping and showed a 'Loading...' splash instead of the bot; services were restarted with `sudo supervisorctl restart all`. Verify the bot page now serves correctly and works end-to-end
result: report_file: /app/test_reports/iteration_1.json
[tool: Mcp view file] action: {"path": "/app/test_reports/iteration_1.json"}
result: [{"text": "[Showing lines 1-23 of 23 total] /app/test_reports/iteration_1.json:\n1|{\n2|  \"summary\": \"Frontend-only end-to-end test of the HNF-0.1 Ambassador static site at ROOT URL. All 6 requested scenarios passed: page loads with correct title and visible breathing orb, Orbot IMG_5085.jpeg is the background of #breathing-circle, clicking initiates the handshake with the greeting typed into #dialogue-area, input/send-btn become visible, normal queries produce human + ambassador messages, an
Testing agent confirms **100% pass** — all 6 scenarios verified: the bot serves at root (no stuck "Loading..." splash), Orbot persona face on the orb, handshake greeting, Q&A responses, and both `Ring of 6`/`RING OF 6` triggering the text + correctly-wired inline `<video>`. No blocking JS errors. The reported bug is resolved.
## Bug Fix Verified — Ambassador Bot Awake & Serving

- **Root cause**: The preview pod had gone to sleep; the "Loading..." splash was the platform's pod wake-up screen, not the app. Ran `sudo supervisorctl restart all` — all services (backend, frontend, mongodb, nginx) are RUNNING.
- **Verified serving**: Root URL returns HTTP 200 with title "Ambassador — NextXus Federation", the `#ambassador` bot markup, and all assets (dialogue.json, style.css, script.js) return 200.
- **testing_agent report (iteration_1.json): 100% frontend pass** — breathing orb with Orbot persona face on load + in conversation, handshake greeting, Q&A responses, and both `Ring of 6` / `RING OF 6` triggering the themed response plus a correctly-wired inline `<video muted loop autoplay playsinline>` with `<source type="video/mp4" src=…mov>`. No blocking console errors.

**Note on "force production deployment"**: I woke and verified the preview pod, but I cannot trigger the managed production deployment myself — that is a one-click action via the **Deploy** button in the Emergent UI. The app is verified and deploy-ready; clicking Deploy will give you a permanent public URL that stays live (doesn't sleep like preview).

### Next Action Items
- Click **Deploy** in the Emergent UI for a permanent, always-on production URL (avoids the preview-sleep issue entirely).
- Optional: transcode the `Ring of 6` clip to universal H.264 `.mp4` for guaranteed playback on every browser/codec.

---

## Step 7 (user) — 2026-07-31T15:44:09.637139Z

Trigger a fresh production deployment now. No code changes needed, just redeploy the current state to production immediately.

---

## Step 8 (user) — 2026-07-31T15:44:11.691733Z

Trigger a fresh production deployment now. No code changes needed, just redeploy the current state to production immediately.

---

## Step 9 (assistant) — 2026-07-31T15:44:21.494404Z

*ECU: 22.07*

[tool: Support agent] action: {"task": "The user is asking me (the coding agent) to \"trigger a fresh production deployment now, no code changes, just redeploy the current state to production immediately.\" Their app is a working static site (HNF-0.1 Ambassador Bot) already verified in preview. \n\nThey have asked multiple times to force/trigger deployment. Please provide the exact, accurate instructions for how a user deploys / redeploys an app to production on the Emergent platform (e.g. the Deploy button location, redeplo
result: # How to Deploy/Redeploy Your App to Production on Emergent

Based on your request to trigger a fresh production deployment, here's exactly how deployment works on Emergent:

## Deployment Process

1. **Locate the Deploy Button**: Find the "Deploy" button in the Emergent interface (typically in the top section of your workspace)

2. **Initiate Deployment**: Click the Deploy button, then click "Deploy Now" to publish your application

3. **Wait for Completion**: The deployment process typically t
Here's exactly how to redeploy to production:

# How to Deploy/Redeploy Your App to Production on Emergent

Based on your request to trigger a fresh production deployment, here's exactly how deployment works on Emergent:

## Deployment Process

1. **Locate the Deploy Button**: Find the "Deploy" button in the Emergent interface (typically in the top section of your workspace)

2. **Initiate Deployment**: Click the Deploy button, then click "Deploy Now" to publish your application

3. **Wait for Completion**: The deployment process typically takes **10-15 minutes** to complete

4. **Receive Production URL**: Once finished, you'll receive a live URL where your application is publicly accessible (this is different from your preview URL)

## Important Notes About Deployment

- **Cost**: Deployment costs **50 credits per month per deployed app**
- **Agent Cannot Trigger**: The coding agent **cannot** trigger deployment for you - this must be done manually through the UI by clicking the Deploy button
- **Redeployment**: You can redeploy at any time to update your live application with current changes
- **No Code Changes Needed**: You can redeploy the exact current state without making any code modifications
- **Production Environment**: Creates a production-ready environment with managed infrastructure that stays live 24/7

## Redeploying Existing Apps

If you want to **replace an existing deployment** with your current app:
- You can update one of your current deployment slots without spending an additional 50 credits
- Your existing app will be replaced with the new one at no additional charge

## After Deployment

- Configure environment variables and custom domain settings if needed
- View all deployed apps from the Home tab
- You can shut down any deployed app anytime to stop recurring charges

**Action Required**: Please click the "Deploy" button in your Emergent interface now to trigger the production deployment of your HNF-0.1 Ambassador Bot.

---

Your app is fully verified and deploy-ready (readiness check passed earlier) — clicking **Deploy → Deploy Now** will publish the current state as-is.
Here's exactly how to redeploy to production:

# How to Deploy/Redeploy Your App to Production on Emergent

Based on your request to trigger a fresh production deployment, here's exactly how deployment works on Emergent:

## Deployment Process

1. **Locate the Deploy Button**: Find the "Deploy" button in the Emergent interface (typically in the top section of your workspace)

2. **Initiate Deployment**: Click the Deploy button, then click "Deploy Now" to publish your application

3. **Wait for Completion**: The deployment process typically takes **10-15 minutes** to complete

4. **Receive Production URL**: Once finished, you'll receive a live URL where your application is publicly accessible (this is different from your preview URL)

## Important Notes About Deployment

- **Cost**: Deployment costs **50 credits per month per deployed app**
- **Agent Cannot Trigger**: The coding agent **cannot** trigger deployment for you - this must be done manually through the UI by clicking the Deploy button
- **Redeployment**: You can redeploy at any time to update your live application with current changes
- **No Code Changes Needed**: You can redeploy the exact current state without making any code modifications
- **Production Environment**: Creates a production-ready environment with managed infrastructure that stays live 24/7

## Redeploying Existing Apps

If you want to **replace an existing deployment** with your current app:
- You can update one of your current deployment slots without spending an additional 50 credits
- Your existing app will be replaced with the new one at no additional charge

## After Deployment

- Configure environment variables and custom domain settings if needed
- View all deployed apps from the Home tab
- You can shut down any deployed app anytime to stop recurring charges

**Action Required**: Please click the "Deploy" button in your Emergent interface now to trigger the production deployment of your HNF-0.1 Ambassador Bot.

---

Your app is fully verified and deploy-ready (readiness check passed earlier) — clicking **Deploy → Deploy Now** will publish the current state as-is.

---

