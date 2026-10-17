# Pustaka Terbuka — SWINMY (Swinburne University of Technology Sarawak Library)

> **Pustaka Terbuka: Katalog Induk Terbuka untuk Perpustakaan dan Sekolah Malaysia.**  
> *Official Swinburne University of Technology Sarawak Library (SWINMY) Bibliographic Dataset & Standalone Harvester.*

This repository contains the harvested open MARCXML collection and harvester pipeline for **Swinburne University of Technology Sarawak Library** (`SWINMY`), contributing to the national Malaysian union catalog at [pustaka-terbuka/opac](https://github.com/pustaka-terbuka/opac).

---

## Institutional Metadata

| Attribute | Value |
| :--- | :--- |
| **Institution Code** | `swinmy` |
| **Agency Code** | `SWINMY` |
| **Official Name** | Swinburne University of Technology Sarawak Library |
| **Institution Type** | `university` |
| **State / Territory** | Sarawak |
| **Target End Bib** | 120,000 |
| **OPAC Base URL** | [https://www.swinburne.edu.my/library](https://www.swinburne.edu.my/library) |
| **Subject Focus** | Software engineering, mechatronics, industrial design, and multimedia design |

---

## Directory Structure

```text
swinmy/
├── README.md                      # Institutional repository documentation
├── package.json                   # Node.js project specification & scripts
├── harvest/
│   └── inbox/swinmy/             # Sealed MARCXML batch chunks and manifests
│       └── <run-id>-chunk-001/
│           ├── manifest.json      # Chunk SHA-256 manifest & metadata
│           ├── provenance.jsonl   # Record-level attribution and fetch logs
│           └── records/           # Batched MARC21 slim XML files
├── tools/
│   ├── harvesters/swinmy/        # Automated OPAC crawler & XML converter
│   └── lib/                       # Supporting MARCXML and validation utilities
└── tests/
    └── harvester-swinmy.test.js  # Autonomous test suite
```

---

## Usage

```bash
# Install dependencies
npm install

# Test run harvester (10 sample records)
npm run harvest:sample

# Run full collection sweep
npm run harvest:full

# Validate dataset integrity
npm run validate-inbox harvest/inbox/swinmy/<chunk-directory>
```

---

## Attribution & License

Dataset harvested and preserved under open library metadata standards for educational, civic, and cooperative indexing. Attribution: **Swinburne University of Technology Sarawak Library (SWINMY)** & **Pustaka Terbuka**.
