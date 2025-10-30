# 🧰 Arc402 SDK Developer Toolkit for Solana Adaptive Intelligence

<div align="center">
  <img src="https://i.imgur.com/YTVZHOW.png" width="100" alt="Arc402 Logo"/>
</div>

---

### Overview

**Arc402 SDK** allows developers to connect DApps and services directly to the **Arc402 Adaptive Intelligence Layer** on Solana.

It provides an intuitive JavaScript/TypeScript interface for sending encrypted context signals, invoking adaptive policies, and fetching on-chain DecisionProofs.

> Designed for developers building privacy-first, intelligent applications on Solana.

---

## 🚀 Installation

```bash
# Using npm
npm install @arc402/sdk

# or yarn
yarn add @arc402/sdk

import { Arc402Client } from "@arc402/sdk";

const arc = new Arc402Client({
  endpoint: "https://console.arc402.org/api",
  programId: "<PROGRAM_ID>"
});

async function main() {
  const result = await arc.evaluatePolicy({
    user: "YourPublicKeyHere",
    intent: "privacy",
    hints: { latency: 40, fee: 0.0002 },
  });

  console.log("Decision Proof:", result);
}

main();
