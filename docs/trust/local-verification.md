# Local Verification & Trust

At Parad0x Labs, we believe that **Trust is Verifiable**. Our "Zero-Persistence Policy" is not just a promise; it is a technical reality enforced by our architecture.

## The Principle of Local Verification

While data compression and orchestration may happen in our secure cloud environment or via managed services, the **power to restore and verify that data belongs solely to the customer.**

### The Sealed Decoder Appliance
To facilitate this, we provide the **Liquefy Sealed Decoder Appliance**—a hardened, "Blackbox" container image that allows you to:
- Decompress archives on your own infrastructure.
- Verify cryptographic hashes of original vs. restored data.
- Run in completely air-gapped environments (`--network=none`).

## Why We Use Sealed Binaries
We provide signed, versioned binaries rather than source code for two reasons:
1. **IP Protection:** To safeguard the proprietary "secret sauce" that allows for 10x–50x compression ratios on high-entropy data.
2. **Security:** A sealed appliance reduces the attack surface, eliminates dependencies, and ensures that the restoration logic has not been tampered with.

## How to Verify
Enterprise clients can follow our [Local Verification Guide](https://github.com/Parad0x-Labs/liquefy/blob/master/docs/enterprise-evaluation.md) to perform independent audits:

1. **Download Archive:** Retrieve your encrypted `.liq` or `.nulla` archive.
2. **Mount License:** Attach your offline `liquefy.lic`.
3. **Run Decoder:** Execute the restoration in a network-isolated container.
4. **Compare Hashes:** Verify that the restored data is a bit-perfect match to your original source.

## Data Sovereignty
By separating the **Encoder** (Optimized for ratio) from the **Decoder** (Optimized for trust), we ensure that you remain the sole owner of your data's "keys to the kingdom."

---
For more details on the decoder contract and licensing, visit the [Liquefy Repository](https://github.com/Parad0x-Labs/liquefy).

