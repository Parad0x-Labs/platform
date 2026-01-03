# Reproduction Guide

This guide outlines how to use the benchmark harness to verify engine performance.

## 1. Prerequisites
*   A synthetic log generator (provided in `tools/gen_logs.py` in the enterprise SDK).
*   The `liquefy` binary (available under license).

## 2. Running a Test
To test the **JSON Columnar Gun** engine:

```bash
# 1. Generate 1GB of synthetic JSON logs
python gen_logs.py --size 1GB --format json --out test.json

# 2. Run compression benchmark
./liquefy compress test.json archive.null --engine json_columnar

# 3. Verify and measure search speed
time ./liquefy grep archive.null "error_code: 500"
```

## 3. Interpreting Results
The output will display:
*   `ratio`: The squeeze factor achieved.
*   `wall_time`: Total processing time.
*   `sha256`: Hash verification to prove bit-perfect restoration.

---
*Note: The actual `liquefy` binary is a proprietary "Black-box" component and is not included in this public documentation repository.*

