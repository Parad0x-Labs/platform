# Frequently Asked Questions

### 1. Is Parad0x Labs Open Source?
No. The core conduction engines (Liquefy and Nebula) are proprietary technologies. This repository provides public documentation, diagrams, and benchmark methodologies. We provide open-source SDKs for decompression to ensure customers always have access to their data.

### 2. Can I try the platform?
Yes. You can experience the latest Conductor live on our website. For full enterprise deployment or custom engine access, please request a demo via our contact page.

### 3. How does it compare to zstd or Splunk/Elasticsearch?
*   **vs. Generic Compression (zstd):** While we use zstd for block-level storage, our engines use specialized "conduction" heuristics that understand log structures (JSON, Apache, SQL, etc.), often doubling or tripling the ratios of raw zstd.
*   **vs. Traditional Indexing (Splunk/ELK):** We eliminate the "Indexing Tax." Instead of creating massive indices that take up more space than the logs, we search directly on the compressed blobs using metadata pruning.

### 4. Does it support encryption?
Yes. Every archive is optionally "sealed" using AES-256-GCM with keys derived via PBKDF2 (100k iterations). We support multi-tenant isolation, ensuring one customer's key cannot decrypt another's data.

### 5. Does it support anonymous payments?
The $NULL ecosystem is being designed with privacy in mind. While the core compression products are enterprise-focused, our roadmap includes integration with decentralized payment rails for "Pay-per-Conduction" access.

---
© 2026 Parad0x Labs. 🚀

