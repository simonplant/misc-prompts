---
title: Super Synthesis Prompt – Modular Spec Sheet
version: 2.1.0
source_prompt: Super Synthesis Prompt v2.1.0
last_updated: 2025-07-22
author: AI Systems Architect
purpose: Configuration reference and modular execution guide for Super Synthesis workflows
---

## 🎛️ CONFIGURATION OPTIONS

### 🔍 Scoring Depth
| Key | Options | Default | Description |
|-----|---------|---------|-------------|
| `scoring_level` | `none`, `doc-level`, `section-level`, `phrase-level` | `section-level` | Controls granularity of comparative evaluation logic |

### ⚖️ Conflict Resolution Strategy
| Key | Options | Default | Description |
|-----|---------|---------|-------------|
| `conflict_resolution` | `consensus`, `strongest-claim`, `most-recent`, `user-tag` | `strongest-claim` | Determines how contradictory claims are resolved in synthesis |

### 🎯 Output Intent
| Key | Options | Default | Description |
|-----|---------|---------|-------------|
| `goal` | *free text* | "finalized executive summary" | Used to align final document tone and purpose |
| `output_format` | `summary`, `brief`, `full_doc`, `appendix+main` | `full_doc` | Controls final output structure and granularity |

### 🧑‍🏫 Audience Role Simulation
| Key | Options | Default | Description |
|-----|---------|---------|-------------|
| `audience_role` | `executive`, `developer`, `analyst`, `PM`, etc. | `executive` | Shapes tone, examples, and structure to reader persona |

### 📥 Preprocessing Mode
| Key | Options | Default | Description |
|-----|---------|---------|-------------|
| `preprocess_format` | `markdown`, `auto` | `markdown` | Input normalization strategy. If `auto`, attempts to convert `.docx`, `.txt`, etc. |

### 🧠 AI-Specific Checks
| Key | Type | Default | Description |
|-----|------|---------|-------------|
| `hallucination_check` | `boolean` | `true` | Flags confident but unsupported statements |
| `redundancy_penalty` | `boolean` | `true` | Penalizes repeated or unoriginal phrasing |

### 🗃️ Version Control Mode
| Key | Options | Default | Description |
|-----|---------|---------|-------------|
| `vcs_mode` | `checklist`, `git-stage`, `skip` | `checklist` | Determines how draft deletion is handled post-synthesis |

---

## 🧱 EXECUTION MODES

| Mode | Description | Use Case |
|------|-------------|----------|
| `two-phase` | Analysis → Synthesis with traceability | Full fidelity with mapping table and audit trail |
| `one-shot` | Fast synthesis, no tracking | Lightweight merge where traceability isn't required |
| `draft-comparison` | Collapses and rewrites from draft history | Version consolidation, WIP cleanup |

---

## 🧩 PLUGGABLE MODULES

| Module | Function |
|--------|----------|
| `section-aligner` | Aligns sections from multiple docs |
| `source-scoring-engine` | Scores contributions using config settings |
| `hallucination-detector` | Flags suspicious language using LLM self-audit |
| `trace-annotator` | Adds inline origin metadata tags |
| `cleanup-generator` | Produces deletion checklists or git-stage commands |

---

## 🔧 RECOMMENDED EXTENSIONS

- Obsidian automation wrapper
- Claude-optimized translation
- Shell-based `.docx` → `.md` converter pre-pass
- Git pre-commit hook for draft cleanup validation
- System health check (missing metadata, inconsistent headers, etc.)

---

Let me know if you’d like a JSON schema version of this config for API or tool integration.
