# The Ocean Pipeline 🌊 (GTM-as-a-Service)

The **Ocean Pipeline** is a state-aware, filesystem-based GTM extraction and enrichment framework built on the **Interpreted Context Methodology (ICM)** and powered by **Vertex AI**.

## 🔱 The Architect's Vision
This pipeline is designed for "Grease Monkey" GTM engineers who build hard-gated data flows. It replaces fragile Zapier/n8n workflows with a transparent, "glass-box" filesystem loop where every stage is an interpreted layer of context.

## 🎭 The Fleet & Personas
- **🔱 Neptune:** The Senior GTM Architect and primary conversational interface (The Webhook).
- **⚓ Ahab:** The Broad Search Grounding specialist (The Hunter).
- **🐦 Sparrow:** The Deep-Sourcing Google Dorking specialist (The Scout).
- **⛴️ Nemo:** The High-Reasoning Technical Auditor (The Signal Architect).
- **📜 Mariner:** The "Grease Monkey" Copywriter (The Storyteller).
- **🦑 Kraken:** The Logistics Engine managing file placement, auth, and git sync.

## 🏗️ The ICM Reiteration Loop
Instead of linear steps, the pipeline uses a **Folder = Stage** architecture. Each bot "wakes up" when data appears in its `in/` folder and writes its artifact to `out/`.

```text
/ocean-pipeline
  ├── /01-Ahab-Lead-Factory   (Broad Grounding)
  ├── /02-Sparrow-Sniper       (Deep Dorking)
  ├── /03-Nemo-Pre-Enrichment  (High-Reasoning Audit)
  ├── /04-Mariner-Copywriting  (Contextual Copy)
  ├── /05-Kraken-Orchestrator  (Logistics & Auth)
  └── /06-Outputs              (Final NocoDB CSVs)
```

## 🚀 Getting Started (CLI Orchestration)
1. **Initialize the Mission:** Write your objective to `ocean-pipeline/01-Ahab-Lead-Factory/in/mission.txt`.
2. **Summon Ahab:** Command Neptune to trigger the hunt. Ahab will "think out loud" ⚓ and produce `out/catch.json`.
3. **Move Data (Kraken):** Kraken 🦑 moves the catch to `03-Nemo/in/`.
4. **Audit (Nemo):** Nemo ⛴️ audits the catch and produces `out/perfect_record.json`.
5. **Storytell (Mariner):** Mariner 📜 drafts the outreach into `out/outreach_pkg.json`.

## 🔱 Vertex AI Deployment
Every bot folder contains a `PROMPT.yaml`. These are the **Production Blueprints** for deployment as Vertex AI Prompt Templates or Agents.

---
*Built with Interpreted Context Methodology (ICM)*
