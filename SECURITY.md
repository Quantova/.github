# Security Policy

Quantova is post quantum end to end by design. The network is live and its native asset is on testnet. Please do not place real value on the testnet asset.

## Supported versions

Security fixes target the latest release of each repository. Older releases are not maintained and their npm versions are deprecated.

## Reporting a vulnerability

Report vulnerabilities privately, never in a public issue, discussion or pull request. Use private vulnerability reporting under the Security tab of the affected repository. It opens a confidential advisory that only the maintainers can see. Include the affected component and version, the steps to reproduce, and the impact you observed.

## What to expect

We acknowledge every report, investigate it and keep you informed while we work on a fix. Please give us reasonable time to release a fix before any public disclosure. Do not attack the live network, do not degrade service for others, and do not access data that is not yours.

## Scope

The consensus engine QORUS, the QVM, the Q Crypto library, the gateway, the Quanta contract language and compiler, the QCore SDKs, QStamp and the application SDKs, QNS, and the token standards QAsset and QCollectible are all in scope.

## Cryptography

Q Crypto uses ML DSA 65, ML KEM 768, SLH DSA, SHA 3 and SHAKE. A weakness in how these algorithms are used is exactly the kind of report we want.
