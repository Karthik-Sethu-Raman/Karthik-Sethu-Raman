# Karthik Sethuraman

Cybersecurity undergrad building systems close to the metal — encrypted storage, boot integrity, and AI-driven security tooling.

`I build security systems (filesystems, boot chains, crypto) and AI/RAG tooling for security operations, mostly in C/C++ and Python.`

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/karthik-sethuraman-1298bb320)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:karthiksethuraman6@gmail.com)

---

## Currently Building

- **Qwen-ATLAS** — RAG-based threat intelligence agent (team project, Model Architect role)


---

## Selected Work

### EVL — Encrypted Virtual Locker
`C` `OpenSSL` `libfuse3` `libargon2`

A block-level encrypted virtual filesystem built on FUSE, verified against 7 distinct attack classes (ciphertext tampering, cross-container block transplant, block reordering).

- Per-block AES-256-GCM encryption with CSPRNG nonces — concurrent `pread`/`pwrite` access without full-file lock contention
- Two-key derivation chain (Argon2id → HKDF-Expand, domain-separated labels) enforcing cryptographic isolation between containers
- Validated under simultaneous read/write access using GDB and Valgrind (zero leaks across ~1,000 allocations)

**Known limits:** no replay/rollback protection, no crash consistency (documented, not hidden — Phase 2 addresses this)

🔗 [Repo](https://github.com/Karthik-Sethu-Raman) · Tagged `v0.1.0`, MIT licensed

---

### Qwen-ATLAS — Threat Intelligence Agent
`Python` `ChromaDB` `HuggingFace` `LoRA`

Hybrid RAG pipeline over 915 MITRE ATT&CK STIX objects for cyber threat intelligence retrieval and attribution.

- Raised threat attribution accuracy from **43.75% → 83.75%** on a 40-query frozen benchmark
- Deterministic benchmark across 8 threat intel categories with a reproducible scoring rubric
- Adversarial evaluation: measured nation-state misattribution rate under poisoned inputs

🔗 [Repo](https://github.com/Karthik-Sethu-Raman)

---

### Preflight AI — Infrastructure Chaos Engine
`Python` `FastAPI` `React` `NetworkX` `Llama-3`

AI-driven DevSecOps platform that parses Terraform into DAGs and simulates cascading "blast radius" failures.

- BFS-based blast-radius simulation over infrastructure dependency graphs
- Chaos simulations offloaded to a self-hosted Llama-3-70B model on an AMD MI300X GPU (via AMD hackathon access), with Fireworks API fallback for logic synthesis
- Custom GitHub Action posting AI-synthesized SOC2 review comments and HCL patches directly on PRs

🔗 [Repo](https://github.com/Karthik-Sethu-Raman)

---

## Stack

| | |
|---|---|
| **Languages** | C, C++, Python, Java, JavaScript |
| **Systems** | Linux, FUSE, POSIX I/O, Concurrency, GDB, Valgrind |
| **Security & Crypto** | AES-256-GCM, Argon2id, HKDF, OpenSSL, Threat Modeling |
| **AI/ML** | RAG, LoRA fine-tuning, vLLM, ChromaDB |
| **Web/Infra** | FastAPI, React, Git, GitHub Actions |

---

## GitHub Stats

[![Anurag's GitHub stats](https://github-stats-extended.vercel.app/api?username=Karthik-Sethu-Raman)](https://github.com/stats-organization/github-stats-extended)

---

📫 Reach me at **karthiksethuraman6@gmail.com** or on [LinkedIn](https://www.linkedin.com/in/karthik-sethuraman-1298bb320)
