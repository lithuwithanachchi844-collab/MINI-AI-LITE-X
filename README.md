MINI AI LITE X
Free, local-first desktop AI companion for Windows 10/11 · Public preview v1.0.1

MINI AI LITE X is a small Python desktop workspace for chat, local knowledge, notes, writing helpers, procedural artwork, website starters, web-page reading, offline mini-games, and optional local language-model chat. It is free to download. No API key or subscription is required for offline features.
Important resource note: MINI AI LITE X runs on the computer where each person installs it. It uses that person's CPU, RAM, and local disk—not the developer's computer. The app data folder is %USERPROFILE%\MINI_AI_LITE_X_Data. A 200 GB app-data budget is a maximum ceiling, not a reserved allocation or a promise that 200 GB is available. Users must have sufficient disk space and can choose not to download large models. The app does not remotely consume resources from other devices.

Download and install
1. Open the repository's Releases page and download MINI_AI_LITE_X_v1.0.1_Portable.zip.
2. Extract it to a folder you can write to. Do not run it inside the ZIP viewer.
3. Install Python 3.11 or 3.12 from https://www.python.org/downloads/. On Windows, enable Add Python to PATH and ensure Tcl/Tk is included.
4. Double-click Start_MINI_AI_LITE_X.bat.
5. To use basic offline responses immediately, choose Offline rules only in AI Model.
6. For actual local LLM chat, install the optional llama-cpp-python runtime in the app's AI Model tab, download the Qwen2.5 0.5B quantized GGUF model, then choose Load / reload model. Model weights are not bundled. The initial download requires internet; a loaded local model can then run offline.
The ZIP is a portable Python source package, not a standalone executable. A small model is around 400–500 MB, plus runtime dependencies. Compatibility depends on Windows, Python, CPU architecture, and available memory. On a 4 GB RAM machine, close other applications and expect slower generation.
Features
- Chat using a small local model, programmed offline rules, or optional explicitly configured online API.
- Teach & Library: save/search lessons and import text/code files.
- Local notes and tasks.
- Calculator and simple writing transforms.
- Procedural PNG Picture Maker (not a trained image-generation model).
- Website Maker for starter HTML/CSS/JavaScript files.
- Web Research that fetches a user-provided public webpage URL; it is not a full search engine.
- Offline Places lookup using a small built-in city list; not full offline maps.
- Game Creator that creates standalone HTML games playable in a browser without internet.
- A separate personal tracker is available as a private download for the maintainer; it is deliberately not included in this public repository.
CPU, RAM and storage
- Inference uses the CPU by default through the selected local runtime. The app does not secretly mine cryptocurrency or run hidden workloads.
- RAM consumption depends on the model, context length, runtime, and other programs. Use a small quantized model on lower-memory computers. The tracker reports system CPU/RAM and the tracker process's RAM when the operating system exposes those metrics.
- App data is stored on the installing user's own computer under %USERPROFILE%\MINI_AI_LITE_X_Data by default. It includes the database, model downloads, imports, generated images/sites, exports, and backups.
- The app and tracker display folder usage against a 200 GB maximum budget. This is not a 200 GB reservation; available drive space remains the real physical limit. Users should review disk space before downloading models or keeping large archives.
- The app's SQLite chat database has a size guard, but this preview does not enforce a hard operating-system quota across every file on the computer. Keep your own backups and monitor the folder.
Privacy and security
- Default chat mode is Offline local model; if the model is not ready, the app explains setup rather than silently sending chat online. Offline rules only requires no model or key.
- Online API use is optional and may incur provider charges. Prompts sent to an online provider leave the computer and are subject to that provider's terms. Never commit API keys to GitHub.
- On Windows, saved API keys are protected with DPAPI for the current Windows account. They still must exist in process memory during a request, so this is not protection against malware or a compromised account.
- Local SQLite chat, notes, lessons, and activity are not encrypted by this app. Avoid saving secrets in them.
- The tracker is a separate personal tool. It binds to 127.0.0.1 by default and requires a control token. Do not publish the tracker, token, database, or logs. For remote access use a private VPN; never port-forward the tracker to the public internet.
- Resource monitoring reports the host running the tracker. It does not spy on unrelated devices, programs, or networks.
- No telemetry/analytics code is intentionally included. No independent security audit has been performed.
Optional online API
Online AI is not required. Users who choose it must supply their own provider endpoint, model access, and credentials. API charges are separate from ChatGPT subscriptions. Do not include keys in source files, screenshots, issues, logs, or release archives.
Licences and model terms
Application source code is offered under the MIT License in LICENSE. Third-party runtime packages and model weights have separate terms. See THIRD_PARTY_NOTICES.md and the exact upstream model card before downloading, modifying, or redistributing model weights. This repository does not bundle Qwen weights or third-party runtime wheels.
Known limitations / testing status
This is a public preview. It is a Tkinter Python application, not a signed standalone EXE. The local model and runtime must be installed separately. Basic image creation is procedural; offline places are a limited lookup; web research fetches supplied URLs only; the offline rules chatbot is not a general LLM. The project has had source syntax and ZIP integrity checks, but it has not been tested across a clean matrix of Windows devices or independently audited. Please report reproducible bugs with steps and redact personal data.
Contributing and support
Please read CONTRIBUTING.md and SECURITY.md. Report bugs through GitHub Issues, but never post API keys, passwords, tracker tokens, private conversations, or personal database files. For suspected security vulnerabilities, follow SECURITY.md rather than posting exploit details publicly.
Release contents
- app/ — public app source and user documentation.
- release/ — portable app ZIP and checksum for the public app release.
- The personal tracker source, token, logs, and tracker ZIP are excluded from this public repository by design.
