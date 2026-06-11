# Ledger trend — Radar AI
Ultimo aggiornamento: 2026-06-11

Legenda stadi: seed | emerging | accelerating | mainstreaming | saturated |
declining | dormiente (21 giorni senza evidenze; dopo 45 → ARCHIVE.md).
Confidenza: bassa | media | alta.
Regola: massimo 10 evidenze per trend, le più recenti.

## Trend attivi

### [id: mcp-standard-001] MCP come livello d'integrazione standard per agenti (core stateless, Apps, Tasks)
- alias: Model Context Protocol, MCP Apps, Tasks extension, spec 2026-07-28
- stadio: accelerating
- confidenza: media
- prima_osservazione: 2026-06-11
- ultima_evidenza: 2026-06-11
- evidenze:
  - 2026-05-21 — https://blog.modelcontextprotocol.io/posts/2026-07-28-release-candidate/ — release candidate della spec 2026-07-28 (finale il 28 luglio): core stateless scalabile su HTTP ordinario, MCP Apps (UI renderizzate dal server in iframe sandboxed), Tasks promossa a estensione ufficiale, sei SEP di hardening OAuth 2.0/OIDC
  - 2026-03-09 — https://blog.modelcontextprotocol.io/posts/2026-mcp-roadmap/ — roadmap 2026: scalabilità del transport, primitive Tasks (retry/expiry), governance a Working Group, enterprise readiness via estensioni
  - 2026-06-11 — https://openai.github.io/openai-agents-python/mcp/ — docs ufficiali OpenAI Agents SDK: cinque trasporti MCP supportati (hosted, streamable HTTP, SSE deprecato, stdio, server manager) con filtering e approvazioni (pagina senza data, consultata oggi)
  - 2026-06-11 — https://adk.dev/tools-custom/mcp-tools/ — docs ufficiali Google ADK: McpToolset come client e ADK come server MCP, in Python/TypeScript/Java/Kotlin (pagina senza data, consultata oggi)
- note: stadio "accelerating" già al bootstrap, in deroga alla regola del massimo "emerging": l'adozione è documentata nei framework ufficiali di almeno tre org (spec/SDK del progetto MCP, OpenAI Agents SDK, Google ADK). La direzione 2026 è chiara: da protocollo di tool-wiring locale a infrastruttura di produzione (stateless, OAuth, UI, task lunghi). Da seguire: pubblicazione della spec finale il 2026-07-28 e velocità di adozione nei Tier 1 SDK.

### [id: pd-disagg-002] Disaggregazione prefill/decode come architettura standard del serving LLM
- alias: PD disaggregation, disaggregated prefilling, disaggregated serving, KV transfer
- stadio: accelerating
- confidenza: media
- prima_osservazione: 2026-06-11
- ultima_evidenza: 2026-06-11
- evidenze:
  - 2026-06-02 — https://github.com/ai-dynamo/dynamo — NVIDIA Dynamo v1.2.0: layer di orchestrazione datacenter-scale con disaggregated serving come capability centrale, sopra vLLM/SGLang/TensorRT-LLM; 7.2k stelle
  - 2026-06-11 — https://docs.vllm.ai/en/latest/features/disagg_prefill.html — docs ufficiali vLLM: prefill e decode su istanze separate con ~9 connettori KV (NIXL, LMCache, Mooncake, FlexKV…); dichiarata sperimentale (consultata oggi)
  - 2026-06-11 — https://docs.sglang.io/advanced_features/pd_disaggregation.html — docs ufficiali SGLang: PD disaggregation con backend di trasferimento Mooncake, NIXL e Ascend, deployment single/multi-node (consultata oggi)
- note: stadio "accelerating" in deroga al massimo "emerging" da bootstrap: la feature è documentata ufficialmente in tutti i principali framework di serving (vLLM, SGLang) e NVIDIA ci ha costruito sopra un prodotto dedicato (Dynamo). Onestà sul controfattore: vLLM la marca ancora "experimental and subject to change". Da seguire: stabilizzazione in vLLM e convergenza sui transfer engine (NIXL vs Mooncake).

### [id: open-weight-003] Ondata open-weight: MoE di frontiera rilasciati a ritmo serrato dai lab cinesi
- alias: open-weight frontier, DeepSeek V4, Kimi K2.6, GLM-5.x, MiniMax M2.x
- stadio: emerging
- confidenza: media
- prima_osservazione: 2026-06-11
- ultima_evidenza: 2026-06-08
- evidenze:
  - 2026-06-08 — https://huggingface.co/deepseek-ai — DeepSeek-V4-Pro (862B) e DeepSeek-V4-Flash (158B) pubblicati/aggiornati ~3 giorni fa (data stimata da "updated 3 days ago" sull'org page)
  - 2026-05-19 — https://huggingface.co/moonshotai — Kimi-K2.6 (1.1T, image-text-to-text, quindi multimodale) aggiornato ~23 giorni fa; K2.5 il 30 aprile (date stimate dall'org page)
  - 2026-05-13 — https://huggingface.co/zai-org — GLM-5.1 (754B) aggiornato ~29 giorni fa; GLM-5 il 5 aprile (date stimate dall'org page)
  - 2026-04-20 — https://huggingface.co/MiniMaxAI — MiniMax-M2.7 (229B), 2.52M download: la famiglia M2.x itera a cadenza ~mensile (M2 dic 2025, M2.1 feb, M2.5 mar, M2.7 apr)
- note: quattro lab (DeepSeek, Moonshot, Z.ai, MiniMax) hanno rilasciato pesi di scala frontier tra aprile e giugno 2026, con cadenza che si misura in settimane. Stadio tenuto a "emerging" per la regola di bootstrap: la velocità andrà misurata nei prossimi run (qui non ho verificato l'adozione nei framework, solo le release). Licenze non verificate sulle singole model card — da fare in un run futuro. Attenzione ai numeri di parametri riportati dagli aggregatori: per V4 fa fede l'org page HF (862B/158B).

### [id: agent-security-004] Sicurezza degli agenti: limiti formali delle difese da prompt injection e svolta architetturale
- alias: prompt injection, indirect prompt injection, agent security, contextual integrity, defense wrappers
- stadio: emerging
- confidenza: media
- prima_osservazione: 2026-06-11
- ultima_evidenza: 2026-05-17
- evidenze:
  - 2026-05-17 — https://arxiv.org/abs/2605.17634 — Abdelnabi & Bagdasarian, "AI Agents May Always Fall for Prompt Injections": risultato di impossibilità — l'avversario può sempre costruire un contesto in cui un flusso bloccato appare legittimo; riletto via Contextual Integrity
  - 2026-04-07 — https://arxiv.org/abs/2604.06436 — Bhatt et al., "The Defense Trilemma": continuità, utility preservation e completeness non possono coesistere in una difesa wrapper; formalizzato in Lean 4 e validato su tre LLM
  - 2025-06-10 — https://arxiv.org/abs/2506.08837 — Beurer-Kellner, Tramèr et al. (gruppo multi-org), "Design Patterns for Securing LLM Agents against Prompt Injections": pattern progettuali con resistenza per costruzione, al costo di trade-off di utilità
- note: tre gruppi indipendenti convergono sulla stessa conclusione: i filtri/wrapper non bastano e la sicurezza va spostata a livello di architettura (least privilege, sandboxing, pattern di design). I risultati di impossibilità (maggio 2026) sono il segnale più recente e forte. Da seguire: reazione dei vendor (difese a livello piattaforma) e advisory su vulnerabilità reali di agenti in produzione.

### [id: rl-env-005] Ambienti RL verificabili come categoria infrastrutturale per l'addestramento di agenti
- alias: RL environments, environments hub, rollout-as-a-service, agentic RL
- stadio: emerging
- confidenza: media
- prima_osservazione: 2026-06-11
- ultima_evidenza: 2026-05-21
- evidenze:
  - 2026-05-21 — https://www.bugcrowd.com/press-release/bugcrowd-launches-reinforcement-learning-environments-to-help-ai-models-learn-real-world-security-skills/ — Bugcrowd lancia "RL Environments" come prodotto: centinaia di migliaia di ambienti da vulnerabilità open-source reali (tecnologia Mayhem), già usati da LLM provider
  - 2026-03-19 — https://arxiv.org/abs/2603.18815 — "ProRL Agent: Rollout-as-a-Service for RL Training of Multi-Turn LLM Agents" (gruppo NVIDIA): il rollout agentico come servizio API con sandbox rootless per HPC; open-source dentro NeMo Gym
  - 2026-04-30 — https://arxiv.org/abs/2604.27859 — Cui et al., "Rethinking Agentic Reinforcement Learning in LLMs": survey che sistematizza il paradigma (obiettivi autonomi, pianificazione lunga, ambienti incerti)
  - 2025-08-27 — https://www.primeintellect.ai/blog/environments — Environments Hub di Prime Intellect: piattaforma aperta per condividere ambienti RL + trainer prime-rl; 30+ contributori già in beta (Arcee, Hud.so, Groq…)
- note: gli ambienti con outcome verificabili stanno diventando un mercato/categoria a sé (chi li vende: Bugcrowd; chi li federa: Prime Intellect; chi li industrializza nel training: NVIDIA). Stadio "emerging": i pezzi sono reali ma l'adozione cross-lab non è ancora misurabile da qui. Da seguire: NeMo Gym, crescita dell'Environments Hub, eventuali standard di interfaccia tra ambienti e trainer.

## coda_osservazione
Segnali non ancora promossi a seed. Formato: data — descrizione — link se c'è.
- 2026-06-11 — "MiniMax M3" (coding frontier + 1M contesto + multimodalità nativa) citato da aggregatori come release di giugno 2026, ma NON presente sull'org page Hugging Face di MiniMaxAI a oggi — non verificato, controllare i canali ufficiali MiniMax
- 2026-06-11 — report vendor "Stacklok State of MCP in Software 2026" citerebbe 41–45% di uso MCP in produzione — non verificato (fonte non aperta), cercare il report originale
- 2026-06-11 — paper "Not All Prefills Are Equal: PPD Disaggregation for Multi-turn LLM Serving" (arXiv 2603.13358): disaggregazione spinta oltre il binomio prefill/decode per il multi-turn — non verificato (non aperto)
- 2026-06-11 — "GenEnv: Difficulty-Aligned Co-Evolution Between LLM Agents and Environment Simulators" (arXiv 2512.19682): la generazione degli ambienti diventa essa stessa oggetto di training — non verificato (non aperto)
- 2026-06-11 — serie di vulnerabilità reali di agenti divulgate in Q1 2026 (EchoLeak, GeminiJack, Reprompt…) citate solo da fonti secondarie — non verificato, risalire agli advisory originali

## rotazione_fonti
Registro di quali fonti sono state coperte in quali date.
- 2026-06-11 — blog.modelcontextprotocol.io; openai.github.io/openai-agents-python (docs OpenAI Agents SDK); adk.dev (docs Google ADK); docs.vllm.ai; docs.sglang.io; github.com/ai-dynamo/dynamo; huggingface.co (org: deepseek-ai, moonshotai, Qwen, MiniMaxAI, zai-org); arxiv.org (2605.17634, 2604.06436, 2506.08837, 2603.18815, 2604.27859); bugcrowd.com (press release); primeintellect.ai (blog). Tentata lmsys.org/blog: indice non leggibile via fetch (rendering JS) — per i post SGLang/LMSYS passare dagli URL diretti dei singoli post.

## note_strategia
Correzioni alla strategia delle fonti proposte dalla routine weekly.
