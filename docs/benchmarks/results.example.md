# Illustrative Performance Results (Example)

The following results represent a sample audit of the latest Conduction Engines. These numbers are illustrative and vary based on data entropy.

### 📊 Log Data Benchmarks

| Data Type | Raw Size | Ratio | Ingest Speed | Query Latency |
| :--- | :--- | :--- | :--- | :--- |
| Structured JSON | 1.0 GB | **35x - 49x** | 95 MB/s | < 150ms |
| Access Logs | 1.0 GB | **18x - 24x** | 80 MB/s | < 200ms |
| Syslog (RFC 5424) | 1.0 GB | **12x - 18x** | 110 MB/s | < 100ms |
| Mixed Text | 1.0 GB | **5x - 8x** | 150 MB/s | N/A |

### 📊 Media Optimization (Nebula)

| Media Type | Original (JPG/MP4) | Squeeze | Quality (SSIM) |
| :--- | :--- | :--- | :--- |
| Static Image (AVIF) | 5.0 MB | **0.8 MB** | 0.98 |
| 4K Video (AV1) | 500 MB | **45 MB** | 0.96 |

**Note:** Results labeled "Extreme" or "Enhanced" prioritize ratio over ingest speed. High-entropy payloads (encrypted or already compressed data) will yield poor ratios.

