# Security Policy

Quantova takes security seriously. The protocol is post quantum end to end by design, and it is at the testnet and pre audit stage. External security audits are planned and they come before mainnet. Please treat the test network as experimental and do not place real value on it.

## Supported versions

Security fixes target the current testnet release. Older snapshots are not maintained.

## Reporting a vulnerability

Please report vulnerabilities privately rather than in a public issue or discussion. Use the private vulnerability reporting feature on the affected repository under its Security tab, which opens a confidential advisory visible only to the maintainers. Include enough detail to reproduce the problem, the affected component, and the impact you observed.

## What to expect

We will acknowledge your report, investigate, and keep you informed as we work on a fix. We ask that you give us reasonable time to release a fix before any public disclosure, and that you avoid actions that damage the network or access data that is not yours.

## Scope

Reports about the consensus engine QORUS, the QVM, the Q-Crypto cryptography, the gateway, the Quanta contract language, the QCore SDKs, QNS, and the token standards QAsset and QCollectible are all in scope. Because the release is pre audit, we welcome findings even where behavior is already known to be incomplete.

## Cryptography note

Q-Crypto uses ML-DSA-65, ML-KEM-768, SLH-DSA, and SHA-3 and SHAKE. If you believe you have found a weakness in how these algorithms are used, that is exactly the kind of report we want.
