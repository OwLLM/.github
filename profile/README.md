<div align="center">

<img src="https://raw.githubusercontent.com/OwLLM/owllm/main/assets/OWLLM_Hero.png" alt="OwLLM" width="560" />

# Your AI workstation — on your hardware, under your control

**Run local models. Bring cloud APIs and subscriptions. Build agent teams.  
Fine-tune models, verify work, ship releases, and operate your other machines from one desktop app.**

[![Latest release](https://img.shields.io/github/v/release/OwLLM/owllm?display_name=tag&sort=semver&style=for-the-badge&label=Latest&color=3ec5d8)](https://github.com/OwLLM/owllm/releases/latest)
[![Windows, Linux, macOS](https://img.shields.io/badge/Windows%20%7C%20Linux%20%7C%20macOS-shipping-2ea043?style=for-the-badge)](#download)
[![License](https://img.shields.io/badge/license-proprietary-8b5cf6?style=for-the-badge)](https://github.com/OwLLM/owllm/blob/main/LICENSE)

[**Download**](#download) ·
[**See what it does**](#one-workstation-the-whole-workflow) ·
[**Get started**](#quick-start) ·
[**Read the architecture**](#safety-is-part-of-the-architecture)

</div>

---

## Download

<table>
<tr>
<td width="25%" align="center" valign="top">

### Windows

Windows 10 / 11 · x64

[**Download `.exe`**](https://github.com/OwLLM/owllm/releases/latest/download/OwLLM.Desktop.Setup.exe)

Native CUDA inference  
WSL2 isolation

</td>
<td width="25%" align="center" valign="top">

### Linux

AppImage

[**Download `.AppImage`**](https://github.com/OwLLM/owllm/releases/latest/download/OwLLM.Desktop.AppImage)

Portable package  
NVIDIA, AMD, Intel probes

</td>
<td width="25%" align="center" valign="top">

### Debian / Ubuntu

Native package

[**Download `.deb`**](https://github.com/OwLLM/owllm/releases/latest/download/OwLLM.Desktop.deb)

Desktop integration  
bubblewrap isolation

</td>
<td width="25%" align="center" valign="top">

### macOS

Apple Silicon · Metal

[**Download `.dmg`**](https://github.com/OwLLM/owllm/releases/latest/download/OwLLM.Desktop.Setup.dmg)

Unified-memory sizing  
Lima isolation (beta)

</td>
</tr>
</table>

All four links resolve to stable asset names in the
[latest GitHub release](https://github.com/OwLLM/owllm/releases/latest).

---

## One workstation, the whole workflow

Most AI apps end at a chat window. OwLLM connects the entire lifecycle around
the model: finding it, running it, teaching it, giving it tools, coordinating
specialists, checking their work, publishing the result, and operating the
machines it runs on.

| | Capability | What it means in practice |
|---|---|---|
| 💻 | **Code projects** | A persistent coding workspace with plans, rules, diffs, files, terminal, browser, project history, and optional second-agent collaboration. |
| 🎭 | **Agent teams** | An orchestrator delegates to specialist agents. Team mode and the focused Coder → Critic → Publisher solo loop share the same project. |
| 📓 | **Notebook + memory** | Capture working notes, digest them into larger next steps, feed or auto-feed the queue, and keep durable project facts separate from recent worklog. |
| 🌐 | **Native agent browser** | Agents open localhost or live sites, inspect pages, click, type, fill forms, and test desktop, phone, and tablet layouts in an OwLLM-owned browser. |
| 🧩 | **Tools, skills, and MCP** | Native GGUF tool-calling, per-agent capabilities, reusable skills, and MCP servers with discovery and schema checks. |
| 🧠 | **Model workshop** | Browse and run Local GGUF models, build datasets, fine-tune with LoRA/QLoRA, export and quantize GGUF, or perform model-safety research. |
| ✅ | **Verification Gate + Publisher** | Completion depends on a real command and exit code. Publisher can version, build, sign, release, and verify an updater from the project rail. |
| 🖥 | **Fleet Control** | Pair OwLLM installations, use models on another device, open a remote shell, or let approved agents run commands over an authenticated encrypted channel. |
| 📱 | **Messaging bridges** | Route Telegram, WhatsApp, Discord, Slack, LINE, or email into a chosen project and model. |

---

## From an idea to a verified release

1. **Start with the job, not a blank agent form.** Choose a web app, mobile app,
   software project, research task, writing job, data workflow, personal
   assistant, or a custom setup.
2. **Brainstorm into a real brief.** The co-founder flow can research the idea,
   write `BRIEF.md`, propose a team, and seed the implementation Notebook.
3. **Run the right specialists.** An orchestrator delegates along a visible
   execution graph; Solo Loop keeps smaller work focused.
4. **Keep work separated.** Code pages and team agents use private Git
   worktrees and branches, then merge with conflict detection.
5. **Steer without stopping.** Mid-run messages become live steering; Notebook
   steps can feed the current run or automatically launch the next clean step.
6. **Prove the result.** The Verification Gate runs the repository's actual
   check. Publisher handles the deterministic release steps only after the
   project is ready.

The conversation, selected models, project rules, Notebook, and useful memory
return when the project is reopened.

---

## Use the model that fits the job

| Model source | Support |
|---|---|
| **Local** | GGUF inference through `llama.cpp`, automatic server start, hardware-aware model fit and context sizing, and local vision projectors. |
| **Cloud APIs** | Anthropic, OpenAI, Gemini, Kimi, and OpenAI-compatible providers can work beside local models in the same project. |
| **Subscriptions** | Use supported Claude Code, Codex, Gemini, and Kimi CLI subscriptions you already have; activity streams into the same OwLLM run view. |
| **Another OwLLM device** | Offer a paired computer's models in the picker, or split the OpenAI-compatible inference server from the machines running the agents. |

Local and cloud models are peers. A project can keep sensitive work local,
choose a cloud model for one specialist, and use a stronger GPU on another
machine without changing the workflow.

---

## Build, adapt, and test models locally

- **Find the right model:** Hugging Face search, curated recommendations, and
  fit ratings based on the selected GPU or unified-memory budget.
- **Build datasets:** turn PDF, DOCX, URL, and text sources into instruction
  JSONL with a selected model.
- **Fine-tuning:** train LoRA/QLoRA adapters on your own hardware with live
  progress and resumable workflows.
- **Convert and quantize:** export Transformers models to GGUF in practical
  Q4–Q8 or F16 variants.
- **Work with vision:** compatible downloads fetch the required vision
  projector so pasted images work with local models.
- **Compare before deployment:** test local, API, and subscription models in
  the multi-column chat playground before assigning them to agents.

---

## Safety is part of the architecture

- **Local-first by default.** Local prompts, project files, model data, and
  memory stay on systems you control. Cloud traffic happens only when a cloud
  model or service is selected.
- **OS-level tool isolation.** Agent commands can run inside WSL2 on Windows,
  Lima on macOS, or bubblewrap on Linux. The project remains visible while the
  rest of the host filesystem stays outside the working boundary.
- **Layered protection.** Isolated worktrees, workspace write boundaries,
  dangerous-command guards, scoped tools, and real verification checks cover
  different failure modes.
- **Network serving is opt-in.** Remote inference requires an explicit setting
  and key. Use it on a trusted network, VPN, or tunnel — never as an
  unauthenticated public endpoint.
- **Remote control is opt-in and paired.** A matching account can help devices
  discover each other, but it does not grant control. The target approves the
  device and its permissions and can stop a live session.
- **Credentials stay runtime-only.** Keys, tokens, certificates, browser
  sessions, and account data are excluded from repositories and application
  builds. Project environment recipes store labels and URLs, not passwords or
  cookies.

See the [repository overview](https://github.com/OwLLM/owllm#readme) for the
technical context behind these trust boundaries.

---

## More than one computer

OwLLM treats your machines as a small, user-owned AI infrastructure:

- Keep native CUDA inference on a GPU workstation while agents run inside a
  safer Linux environment elsewhere.
- Pair another OwLLM machine and use its model catalogue from the same picker.
- Sync projects across PCs with a three-way merge coordinator that never
  force-pushes or silently chooses a side of a real conflict.
- Use Fleet Control for authenticated diagnostics, interactive shells, WSL
  commands, and deliberately approved agent access.
- Connect a NanoKVM or PiKVM when an agent must see and operate a separate
  machine beyond the OS — including recovery and BIOS-level workflows.
- See live, anonymous OwLLM presence and your own fleet on the World Map.

The model, the agents, the tools, and the controlled machine do not need to live
on the same computer.

---

## Quick start

1. [Download the package for your OS](#download) and launch OwLLM.
2. Let onboarding detect the hardware and install the runtime modules needed
   for that machine.
3. Download a local model from **Models**, or connect an API/subscription from
   **Accounts**.
4. Open **Coding** for one focused agent, **Agentic Team** for coordinated work,
   or **Train** to adapt a model.
5. Keep the isolation badge on for tool-using projects, and define the
   repository's real verification command before publishing.

---

## Learn, discuss, and report

- 📘 [Quick start](#quick-start)
- 🧭 [Repository and technical overview](https://github.com/OwLLM/owllm#readme)
- 🖥 [Platform downloads](#download)
- 🚀 [Latest release and changelog](https://github.com/OwLLM/owllm/releases/latest)
- 💬 [Discussions](https://github.com/OwLLM/owllm/discussions)
- 🐛 [Issues](https://github.com/OwLLM/owllm/issues)

## License

OWLLM is proprietary software owned by **Far island Corporation Ltd.**
Official unmodified executables may be used free of charge; the source is not
licensed for copying, modification, redistribution, sublicensing, or sale.
See the complete [OWLLM license](https://github.com/OwLLM/owllm/blob/main/LICENSE).

---

<div align="center">

**Your models. Your agents. Your machines. One workstation.**

</div>

