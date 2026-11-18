# Open-source AI video clippers on GitHub — survey (Nov 2026)

Everything here was read off the repos themselves (READMEs + GitHub API metadata) on 18 Nov 2026.
Two families, because they are not the same tool:

- **A. VOD clippers** — long video / podcast / stream replay → vertical shorts.
- **B. Live clippers** — watch a stream *while it is broadcasting*, clip on the fly.

Star counts and "last push" are from the GitHub API at time of writing. RAM/VRAM is only quoted
where the repo states it — see [RAM](#ram-the-honest-answer) for why that matters.

---

## A. VOD clippers (recorded → shorts)

| Repo | ★ | Lang | Licence | Made for | Notable |
|---|---|---|---|---|---|
| [Anil-matcha/AI-Youtube-Shorts-Generator](https://github.com/Anil-matcha/AI-Youtube-Shorts-Generator) | 6.2k | Python | MIT | YouTube → Shorts, LLM highlight + Whisper | Most-starred. CLI + importable library. API mode offloads work to MuAPI cloud; `--mode local` is the offline path |
| [zhouxiaoka/autoclip_mvp](https://github.com/zhouxiaoka/autoclip_mvp) | 1.3k | Python | MIT | Bilibili/upload → highlight clips, web UI | Docker-first, Chinese docs, no commits since Sep 2025 |
| [jipraks/yt-short-clipper](https://github.com/jipraks/yt-short-clipper) | 1.1k | TypeScript | MIT | YouTube only, Windows desktop | **No Whisper at all** — burns YouTube's own subtitle track. Lowest resource cost of the lot |
| [RafaelGodoyEbert/ViralCutter](https://github.com/RafaelGodoyEbert/ViralCutter) | 485 | Python | GPL-3.0 | YouTube → TikTok/Reels, Opus-Clip-style web UI | Gemini free tier / GPT-4 / local GGUF, WhisperX GPU |
| [xixihhhh/hotclip](https://github.com/xixihhhh/hotclip) | 484 | TypeScript | AGPL-3.0 | Livestream replays + long video + podcasts, CN platforms | **Danmaku (chat) heat as evidence**, Electron app, publishes to Douyin/Kuaishou/Bilibili, 7×24 folder watch |
| [artbyjazi/autoclip](https://github.com/artbyjazi/autoclip) | 395 | Python | MIT | Local-first, any source | Whisper + Ollama, speaker-tracked reframe, 4 caption styles, Docker. Most honest README (states what is *not* verified) |
| [NaufalRizqullah/opensource-clipping](https://github.com/NaufalRizqullah/opensource-clipping) | 322 | Python | MIT | Podcasts, multi-speaker | Split-screen + camera-switch diarization, AI voice-over commentary, Colab/Kaggle GPU backend |
| [ColinGPT9/clips-studio](https://github.com/ColinGPT9/clips-studio) "Clips Kitty" | 321 | Python | AGPL-3.0 | Twitch/Kick/YouTube streams, gaming, **basketball** | Widest feature set: TalkNet active-speaker, podcast multicam, Vertical Live mode, YT publish/schedule, chat box |
| [Shaarav4795/ClippedAI](https://github.com/Shaarav4795/ClippedAI) | 246 | Python | n/a | YouTube → Shorts | Thin wrapper over `clipsai`. 8 GB RAM min, 16 GB recommended |
| [nmbrthirteen/podcli](https://github.com/nmbrthirteen/podcli) | 92 | Python | AGPL-3.0 | Podcasts | CLI + MCP server + web studio, self-contained installer (no prereqs) |
| [mehbul/chopify](https://github.com/mehbul/chopify) | 79 | Python | MIT | Local dashboard + CLI, batch jobs | Resumable projects, editable captions/SRT, semantic clip search. **No LLM needed** by default |
| [fralapo/clippyme](https://github.com/fralapo/clippyme) | 68 | Python | MIT | Self-hosted, unattended | Live monitor + auto-publish; fork of OpenShorts |
| [JeremySNR/cutawan](https://github.com/JeremySNR/cutawan) | 59 | TypeScript | MIT | Desktop installer, podcasts | ChatGPT/Codex login, or API key, or captions-only local. No Docker, no Python needed |
| [sherlock-dev-ai/Clipify-AI-Video-Clipper-FREE](https://github.com/sherlock-dev-ai/Clipify-AI-Video-Clipper-FREE) | 58 | Python | n/a | Windows installer, Shorts | Also has a **Live Studio (beta)** and a faceless-narration studio. Ollama qwen2.5:3b ≈ 2 GB VRAM |
| [kleZ799/clipmint](https://github.com/kleZ799/clipmint) | 51 | Python | MIT | Any genre, desktop | Detects video *type* then ranks by its rules; Gemini→Groq→OpenRouter→Ollama fallback ladder; 8 UI languages; published perf table |
| [hajdu-patrik/clippy](https://github.com/hajdu-patrik/clippy) | 43 | Python | n/a | Chat-driven app + CLI | Qwen3-14B Q6_K via Ollama, versioned edits, **12–16 GB VRAM recommended** |
| [LikithMeruvu/AI-Clipping-Software](https://github.com/LikithMeruvu/AI-Clipping-Software) | 42 | Python | MIT | Minimal Gemini clipper | Tiny README, demo-grade |
| [GrepCut/OpenClipper](https://github.com/GrepCut/OpenClipper) | 21 | TypeScript | MIT | Windows desktop (Tauri + Rust) | Own autoreframe engine (scene cuts + subject tracks), batch render, MCP |
| [PriyeshPandey2000/ai-video-clipper](https://github.com/PriyeshPandey2000/ai-video-clipper) | 21 | TypeScript | MIT | macOS Electron app | OpusClip/Descript/Submagic alternative |
| [thealiraza2/CapShorts](https://github.com/thealiraza2/CapShorts) | 20 | TypeScript | MIT | Editor + auto-subtitle suite | Tauri, word-accurate subtitles |
| [osbytes/reelsaw](https://github.com/osbytes/reelsaw) | 19 | TypeScript | AGPL-3.0 | Self-hosted / multi-tenant | Postgres + pg-boss job queue, S3 storage, MCP, roles, billing hooks. **Heaviest** |

---

## B. Live / livestream clippers (watching while broadcasting)

| Repo | ★ | Lang | Licence | How it clips live |
|---|---|---|---|---|
| [VadlapatiKarthik/autoclipper](https://github.com/VadlapatiKarthik/autoclipper) | 45 | Python | none | YouTube channels + Twitch/Kick live, audience-retention signals, uploads results |
| [lxgicstudios/lxgic-clipper](https://github.com/lxgicstudios/lxgic-clipper) | 12 | Shell | MIT | Records via yt-dlp, audio+scene+Whisper detection, auto-posts to TikTok/Shorts/Reels/X |
| [Cbhhhh211/Stream-Clipper-Factory](https://github.com/Cbhhhh211/Stream-Clipper-Factory) | 11 | Python | MIT | Local video + links, danmaku heat, scoring and export |
| [portal-source/stream-clip-detector](https://github.com/portal-source/stream-clip-detector) | 1 | Python | none | Z-score audio spikes + keyword triggers, watchlist daemon, chat overlay |
| [builtbyuba/ClipMind-AI](https://github.com/builtbyuba/ClipMind-AI) | 1 | Python | n/a | streamlink + ffmpeg rolling ~150 s buffer, audio energy + chat velocity |
| [shubtriple7/StreamSniper](https://github.com/shubtriple7/StreamSniper) | 0 | Python | n/a | Chat-velocity spikes (Twitch IRC, Kick Pusher, YT chat), bilingual subs, ranked 0–100 |
| [xAmirHamza77/StreamCut](https://github.com/xAmirHamza77/StreamCut) | 0 | Python | MIT | Rolling buffer, evaluates every few minutes, auto-watches creators, one-click manual grab, publishes |
| [AthanWs/ClipperX](https://github.com/AthanWs/ClipperX) | 0 | Python | MPL-2.0 | Multi-hour VOD/live: local ASR + diarization + LLM editorial planner + visual director. Windows + CUDA 12.4 |
| [sherlock-dev-ai/Clipify](https://github.com/sherlock-dev-ai/Clipify-AI-Video-Clipper-FREE) | 58 | Python | n/a | "Live Studio (beta)" inside the same Windows app |
| [xixihhhh/hotclip](https://github.com/xixihhhh/hotclip) | 484 | TypeScript | AGPL-3.0 | 7×24 folder watch on 录播姬/OBS recordings, then clips and publishes |
| [ColinGPT9/clips-studio](https://github.com/ColinGPT9/clips-studio) | 321 | Python | AGPL-3.0 | "Vertical Live" mode for already-vertical streams; Twitch/Kick VODs |

**Live clipping is a much smaller, younger field.** The two starred VOD projects that also do live
(hotclip, clips-studio) are the only ones with real traction; everything else in table B is
single-digit stars or unreleased. Treat them as experiments.

---

## Feature matrix

`✓` stated in the README · `–` not claimed · `$` requires a paid API

| Repo | Local-only | Live | Face track | Diarization | Caption styles | Auto-publish | GUI | CLI | MCP/agent | Docker |
|---|---|---|---|---|---|---|---|---|---|---|
| AI-Youtube-Shorts-Generator | partial | – | ✓ | – | ✓ | – | – | ✓ | – | – |
| autoclip_mvp | – | – | – | – | ✓ | – | web | – | – | ✓ |
| yt-short-clipper | ✓ | – | ✓ | – | ✓ | – | desktop | – | – | – |
| ViralCutter | ✓ | – | ✓ | – | ✓ | – | web | – | – | – |
| hotclip | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | desktop | ✓ | ✓ | – |
| autoclip (artbyjazi) | ✓ | – | ✓ | ✓ | ✓ (4) | – | web | – | – | ✓ |
| opensource-clipping | – | – | ✓ | ✓ | ✓ | – | web | ✓ | – | – |
| clips-studio | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | desktop | – | – | ✓ |
| ClippedAI | – | – | – | – | ✓ | – | – | ✓ | – | – |
| podcli | partial | – | ✓ | ✓ | ✓ | – | web | ✓ | ✓ | – |
| chopify | ✓ | – | ✓ | ✓ | ✓ | – | web | ✓ | – | – |
| clippyme | partial | ✓ | ✓ | – | ✓ | ✓ | web | – | – | ✓ |
| cutawan | partial | – | ✓ | ✓ | ✓ | – | desktop | – | – | – |
| Clipify | ✓ | ✓ | ✓ | – | ✓ | – | desktop | – | – | – |
| clipmint | partial | – | ✓ | – | ✓ | – | desktop | – | – | – |
| clippy (hajdu) | ✓ | – | ✓ | – | ✓ | – | web | ✓ | – | – |
| OpenClipper | partial | – | ✓ | – | ✓ | ✓ | desktop | – | ✓ | – |
| reelsaw | partial | – | ✓ | – | ✓ | – | web | ✓ | ✓ | ✓ |
| StreamCut | partial | ✓ | ✓ | – | ✓ | ✓ | web | – | – | ✓ |
| ClipperX | ✓ | – | – | ✓ | ✓ | – | – | ✓ | – | – |
| lxgic-clipper | partial | ✓ | – | – | ✓ | ✓ | – | ✓ | – | – |
| StreamSniper | – | ✓ | – | – | ✓ | – | – | – | – | – |

---

## Which one for which purpose

- **Just want Shorts out of a YouTube video, on Windows, with the least fuss** → `yt-short-clipper`
  (installer, no local model) or `cutawan` (installer, no Docker/Python).
- **Podcasts / interviews with several speakers on camera** → `opensource-clipping` (split-screen +
  camera switching) or `podcli` (multicam edit, same edit from CLI/studio/agent).
- **Twitch / Kick streamer, VODs** → `clips-studio` (built for gaming + reactions) or `hotclip`.
- **Gaming reactions with a webcam pane** → `clips-studio` (Gaming/Reaction switch decides the
  streamer is whoever is talking, not the biggest face).
- **Sports** → `clips-studio` (basketball: score bug, quarters, dunks/threes).
- **Fully offline, no cloud keys, small machine** → `autoclip`, `chopify` (heuristics need no LLM),
  `hotclip` (int8, CPU fine).
- **Team / many users / multi-tenant self-hosting** → `reelsaw`.
- **Wiring it into an agent or your own pipeline** → `podcli`, `OpenClipper`, `reelsaw`, `hotclip`
  (all ship an MCP server); or import `generate_shorts()` from `AI-Youtube-Shorts-Generator`.
- **Live streams** → `StreamCut` (most complete of the small ones: rolling buffer, auto-watch,
  publishing) with `StreamSniper` / `stream-clip-detector` as chat-hype or audio-hype detectors.
- **Bilibili / Douyin / Kuaishou / Xiaohongshu** → `hotclip` (only one that publishes there).

## Which has the most features

**`clips-studio` (Clips Kitty)** — the only one that combines: active-speaker detection (TalkNet,
face *and* audio), podcast multicam with per-shot crops, a vertical-live mode, genre-specific
routing (gaming, reaction, basketball), a non-destructive editor with an AI edit chat, a model
manager, and YouTube upload + scheduling. It is also the only one that states a hard RAM floor and
performance-tests hardware. Cost: 16 GB RAM, AGPL-3.0, Windows-first.

Runner-up depends on axis: `hotclip` for workflow breadth (danmaku evidence, 7×24 unattended,
CLI/MCP/agent, CN platforms), `reelsaw` for infrastructure breadth (queues, S3, roles, observability).

## RAM: the honest answer

Very few repos state memory. Those that do:

| Repo | Stated |
|---|---|
| `clips-studio` | **16 GB RAM required** ("8 GB will analyse a whole video and then render nothing"). GPU optional; RTX 2060 6 GB is where the GPU path starts |
| `reelsaw` | Tiers by machine: qwen2.5:14b ≈ 9 GB + 24 GB RAM or 12 GB GPU → qwen2.5:7b from 12 GB → gemma3:4b below that |
| `clippy` (hajdu) | NVIDIA **12–16 GB VRAM recommended**; CPU works |
| `Clipify` | qwen2.5:3b ≈ **2 GB VRAM**; CPU supported |
| `ClippedAI` | **8 GB+ RAM**, 16 GB recommended |
| `autoclip`, `cutawan`, `chopify`, `hotclip` | GPU **optional**, CPU path works |

- **Lowest RAM:** `yt-short-clipper` — it never runs an ASR model at all (it reads YouTube's own
  subtitles), so there is no Whisper on your machine. After that, `hotclip` (int8 sherpa-onnx small
  model, "no GPU needed") and `chopify` (heuristic selection, no LLM by default).
- **Highest RAM:** `reelsaw` (Postgres + worker containers + a 14B model), then `clips-studio`
  (16 GB floor), then `clippy` and `ViralCutter` (Whisper large-v3 + a 14B-class local LLM).

Rule of thumb from these repos: **Whisper model size dominates RAM, the LLM dominates VRAM.**
`tiny`/`base` int8 ≈ under 1 GB; `large-v3` wants several GB and a GPU to be bearable. A 3–4B local
LLM fits in 8 GB of VRAM; a 14B Q6_K needs ~12–16 GB. Almost every project lets you point the LLM at
a cloud API instead, which moves the cost to dollars and off your RAM.

## Addendum — three repos checked in depth

### `haziqahmedqasmi/PeakCut` — 962★, Python, MIT, created **14 Nov 2026**

Not in the tables above because it is four days old and already overtook most of the field.
Same feature profile as `StreamCut` — because **`StreamCut` is a single-commit re-upload of it**:
`xAmirHamza77/StreamCut` was created 17 Nov, has one commit ("StreamCut v1.0.0"), 0 stars, and a
`studio/` tree with the identical module layout (`admin.py`, `ai.py`, `asr_worker.py`, `live.py`,
`jobs.py`, `notices.py`, …). Both are MIT, so it is legal to fork, but use PeakCut. The earlier
"most complete of the small live clippers" note applies to PeakCut, not StreamCut.

- **VOD + live in one app.** Rolling buffer records a creator's stream and clips while it is still
  broadcasting, scoring on loudness + chat activity + transcript.
- **ASR: `sherpa-onnx` + Parakeet, ~480 MB model, one download, runs on CPU locally.** No Whisper,
  no PyTorch, no CUDA. This is the lightest serious option in this document — it sidesteps the
  single biggest RAM/VRAM cost every other VOD clipper carries.
- **AI is swappable and optional.** Gemini / OpenAI / xAI / Groq / OpenRouter / Claude / Ollama /
  any OpenAI-compatible URL, comma-separated model list tried in order as fallback. No key at all
  still works, falling back to loudness picks.
- **Self-hosted server done properly for its size:** per-user data folders, fair-queue per user,
  self-monitoring (measures CPU/RAM/disk every second and only starts jobs when there is room),
  SQLite locally / PostgreSQL + Caddy HTTPS via Docker, `/admin` dashboard, scrypt passwords,
  salted+hashed session tokens.
- **Honest by design:** refuses to expose itself publicly without accounts (`PEAKCUT_ACCOUNTS=1`),
  treats transcript text as data before showing it to an LLM, and says up front that it is written
  to be installed by an AI assistant (`AGENTS.md`), including the Windows 260-character path trap.
- **No stated RAM figure**, but by construction (no Torch, no Whisper large, CPU ASR) it is the
  low-RAM pick. AI cost: "a one-hour video is read in about four requests."

### `lxgicstudios/lxgic-clipper` — 12★, Shell, MIT

Six bash scripts (`setup`, `clipper-agent`, `record-stream`, `detect-highlights`,
`clip-and-format`, `post-clip`) orchestrated by OpenClaw cron. I read the scripts:

- `detect-highlights.sh` is genuine engineering, not a stub: ffmpeg `volumedetect` for mean/max,
  `astats` per-second RMS with `reset=44100`, scene-change detection at `scene>0.35`, then optional
  Whisper (probed across several binary names). Scores 0–100, `CLIPPER_THRESHOLD` default 70.
- `post-clip.sh` posts through the **Postiz API** (self-hostable, ~32 platforms).
- **No LLM anywhere.** Detection is signal processing, so it will not judge meaning, only loudness,
  cuts and speech density. That is why it is cheap and portable, and also its ceiling.
- **It is a funnel for a paid product.** The README carries a price table ($29/$49/$99 per month,
  "Get it on Whop") for a hosted version and markets 20+ other tools. The scripts are real; treat
  the repo as marketing for the service.
- macOS-leaning (`brew`, `/dev/null`, `chmod +x`). 106 KB, last touched Feb 2026, i.e. it predates
  everything else here and has not kept up.

### `NaufalRizqullah/opensource-clipping` — 322★, Python, MIT

Unchanged from the table above, and worth restating what it costs: it is the **heaviest and least
local** of the three.

- Faster-Whisper **large-v3** + Pyannote diarization + YOLOv8/MediaPipe face tracking + optional
  Kokoro TTS for AI voice-over commentary. Needs CUDA to be bearable; the recommended path is a
  free Colab/Kaggle T4 GPU with a Gemini key.
- Its actual differentiator is **multi-speaker podcast craft**: split-screen, cinematic camera
  switching, 3+ speakers, per-speaker frozen-frame fallback, hook intros, BGM ducking. Nothing
  else here does that as well.
- **No live clipping.** VOD in, clips out.
- Effectively a **cloud-GPU product**: a static GitHub Pages front end driving a Kaggle/Colab
  FastAPI backend. That is clever and free, but it is not "runs on your machine tonight."

### Head to head

| | PeakCut | lxgic-clipper | opensource-clipping |
|---|---|---|---|
| Live while broadcasting | ✓ | ✓ | – |
| Transcription | sherpa-onnx Parakeet, CPU, ~480 MB | optional Whisper binary | faster-whisper large-v3, CUDA |
| LLM clip picking | any provider, or none | none (signal only) | Gemini / NVIDIA NIM, required for ranking |
| Multi-speaker podcast craft | – | – | ✓✓ best in field |
| Auto-posting | YT / IG / TikTok, caps + spacing | Postiz, ~32 platforms | – |
| Accounts / multi-user | ✓ | – | – |
| Footprint | ~760 KB, Python + ffmpeg | 106 KB, bash + ffmpeg | 76 MB + Torch + CUDA + HF token |
| Licence | MIT | MIT | MIT |
| Catch | 4 days old, 27 open issues already | thin, LLM-free, funnels to paid plan | needs a GPU or Colab |

**Pick:** PeakCut if you want one tool that does VOD and live on a normal machine. lxgic only if you
want dumb-but-reliable audio/spike clipping driven by cron and want nothing to do with Python.
opensource-clipping only for real multi-speaker podcasts and you have a GPU or a Colab account.

## Things worth knowing before you pick

- **Star count ≠ quality here.** `AI-Youtube-Shorts-Generator` has 6.2k stars and a 1.3 MB repo; the
  capstone is a CLI you can also import. `reelsaw` has 19 stars and 40 MB of production
  infrastructure. Read the README, not the number.
- **"Free and local" often means "you bring an API key".** Several projects default to Gemini or
  OpenAI for moment selection and only the transcription is local. Only `autoclip`, `chopify`,
  `hotclip`, `clippy`, `Clipify` and `ClipMind` explicitly support a no-key / Ollama path.
- **Licences differ in ways that matter commercially.** MIT on most; **AGPL-3.0** on `clips-studio`,
  `hotclip`, `podcli`, `reelsaw` — fine to use, hostile to shipping a modified closed SaaS.
  `ClippedAI`, `Clipify`, `clippy` and `Cutawan` show `NOASSERTION` — read the file yourself.
- **The clip *selection* is the product, and it is the least verifiable part.** `autoclip` is the
  only README that separates "verified" from "not verified" and admits its reframe quality bar has
  no golden set yet. Take every "AI finds the best moments" claim with that in mind.
- **Most run Whisper from scratch every time.** Only `yt-short-clipper` (YouTube subtitles) and
  `chopify`/`clips-studio` (caching) avoid re-paying transcription on re-runs.

---

*Method: GitHub repository search (`AI video clipper`, `opus clip alternative open source`,
`podcast clipper AI`, `AI clipping highlights video`, `livestream clipper AI`,
`auto clip twitch kick stream`), then each repo's page and README read directly; metadata from
`api.github.com/repos/{owner}/{repo}`.*
