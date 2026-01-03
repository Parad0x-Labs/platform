# Benchmark Methodology

To ensure fair and transparent results, Parad0x Labs follows a strict benchmarking protocol.

## 1. Datasets
We use a combination of:
*   **Public Datasets:** NASA HTTP logs, GitHub Event streams, and Enron email corpus.
*   **Synthetic Generators:** Custom scripts that simulate high-velocity JSON and Syslog traffic with varying entropy levels.
*   **Real-World Samples:** Anonymized logs provided by enterprise partners (Apache, Nginx, AWS CloudTrail).

## 2. Metrics
Every benchmark run must report:
*   **Compression Ratio:** `Raw Size / Compressed Size`.
*   **Ingest Throughput:** MB/s processed during compression.
*   **Query Latency:** Time to complete a specific search query on a 1GB+ archive.
*   **Resource Footprint:** Peak RAM and CPU usage during the run.

## 3. Environment
Benchmarks are typically run on:
*   **Generic Linux Nodes:** 4-8 vCPU, 16GB RAM.
*   **Storage:** NVMe SSD.
*   **OS:** Ubuntu 22.04 LTS (Docker-based).

## 4. Fairness Rules
*   **No Pre-Loading:** Every run starts with a cold cache.
*   **Deterministic:** All compression engines must use their production-grade "Safe" mode unless "Extreme" is specified.
*   **End-to-End:** Time includes ingest, encryption, and verification.

