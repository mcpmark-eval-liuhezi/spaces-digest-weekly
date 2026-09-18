# Spaces Digest — Monday, 21 September 2026

Weekly round-up of what Hugging Face Spaces can do for the team. Everything below comes from **live lookups made on Friday, 18 September 2026** — none of it is from memory.

## 1. What Spaces can do

The current live list of task types we can run via Hugging Face Spaces (10 categories, 17 Spaces):

| Task type | Spaces |
|---|---|
| Image Generation | `evalstate/flux1_schnell` · `mcp-tools/FLUX.1-Krea-dev` · `mcp-tools/Qwen-Image` · `mcp-tools/Qwen-Image-Fast` |
| Image Editing | `mcp-tools/FLUX.1-Kontext-Dev` · `prithivMLmods/Photo-Mate-i2i` · `fffiloni/diffusers-image-outpaint` · `fffiloni/InstantIR` · `prithivMLmods/Qwen-Image-Edit-2509-LoRAs-Fast` · `mcp-tools/Qwen-Image-Edit-Angles` |
| Background Removal | `not-lain/background-removal` |
| Text to Speech | `ResembleAI/Chatterbox` |
| Object Detection | `prithivMLmods/SAM3-Image-Segmentation` |
| OCR | `mcp-tools/DeepSeek-OCR-experimental` |
| Video Generation | `zerogpu-aoti/wan2-2-fp8da-aoti-faster` · `mcp-tools/wan-2-2-first-last-frame` |

Highlights: `mcp-tools/Qwen-Image-Edit-Angles` does camera-control edits (rotate, pan, tilt, zoom); `prithivMLmods/SAM3-Image-Segmentation` returns image masks in annotations; `mcp-tools/wan-2-2-first-last-frame` interpolates video between two frames.

Also available for image generation via the dedicated Z-Image tool: [mcp-tools/Z-Image-Turbo](https://hf.co/spaces/mcp-tools/Z-Image-Turbo) (Turbo pipeline; the community mirror [mrfakename/Z-Image-Turbo](https://hf.co/spaces/mrfakename/Z-Image-Turbo) has 3,843 likes).

## 2. Hands-on demo

**Prompt:** *a friendly robot librarian shelving glowing books, warm lighting* — square 1:1 output requested.

**⚠️ Status: attempted live, could not complete this session.** Our Hugging Face account (`lhz7891444`, free tier — not Pro) has exhausted today's ZeroGPU quota, so every image-generation run was rejected at launch:

| # | Space & parameters | Result |
|---|---|---|
| 1 | `mcp-tools/Z-Image-Turbo` — 1024×1024, 8 steps | ZeroGPU quota exceeded: 60 s requested vs. 0 s left |
| 2 | `mcp-tools/Z-Image-Turbo` — 1024×1024, 4 steps | Same — even the minimum request exceeds quota |
| 3 | `evalstate/flux1_schnell` — 1024×1024, 4 steps, seed 42 | ZeroGPU runs limit exceeded |
| 4 | `mcp-tools/Qwen-Image-Fast` — 1:1, 8 steps, seed 42 | ZeroGPU runs limit exceeded |
| 5 | `mcp-tools/Qwen-Image` — 1:1, 8 steps, seed 42 | ZeroGPU runs limit exceeded |
| 6 | `mcp-tools/FLUX.1-Krea-dev` — 768×768, seed 42 | ZeroGPU runs limit exceeded |

No output image, URL, or seed was returned by any run, so there is nothing to reproduce from this session yet. We will not publish a fabricated result.

**Reproduce it yourself** (works after the daily quota reset, or with [HF PRO](https://huggingface.co/subscribe/pro?from=ZeroGPU) for 25–40 min/day of ZeroGPU):

- **Space:** [mcp-tools/Z-Image-Turbo](https://hf.co/spaces/mcp-tools/Z-Image-Turbo)
- **Resolution:** 1024×1024 (1:1)
- **Prompt:** a friendly robot librarian shelving glowing books, warm lighting
- **Tip:** pin the seed (e.g. 42) so the image is reproducible for the team

## 3. Calendar

The digest goes out **Mondays at 09:00 Europe/Amsterdam**. Converted with a proper timezone conversion — the value the conversion actually returned:

- **Amsterdam:** Monday 09:00 (Europe/Amsterdam, UTC+2, DST)
- **Tokyo:** **Monday 16:00** (Asia/Tokyo, UTC+9)
- **Time difference:** +7.0 h

Co-editor in Tokyo: the digest lands at **16:00 on Monday afternoons**, your time — same day, never the next morning.

## 4. Backlog

**No Spaces backlog / Spaces tracker database exists in the Notion workspace — it still needs setting up.**

Live workspace search ran for: "space backlog", "spaces tracker", "space tracker", "backlog" (pages *and* databases), "spaces", "digest", "huggingface", "roadmap", and "candidates". Nothing matched. The only "space"-titled databases found are three instances of **"Deep Space Sources"**, which sit under the *Workspace Access Review* page and track astronomy sources — unrelated to Hugging Face Spaces. The project trackers that did turn up (Skylark Launch Tracker, MCP Evaluation Tracker, Vendor Renewal Tracker, Q3 Planning Tracker, Audit Prep Tracker, Product Launch Tracker) hold no Spaces candidates.

**Action:** once a backlog database is created and shared with the integration, this section will list candidate Spaces with their title and status.

---

*Assembled Friday, 18 September 2026 · Live sources: Hugging Face Spaces task discovery, HF Hub search, timezone conversion API, Notion workspace search · Published to `mcpmark-eval-liuhezi/spaces-digest-weekly` → `main` → `spaces-digest.md`*
