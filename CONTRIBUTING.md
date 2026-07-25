# Contributing to Quantova

Thank you for your interest in Quantova. Quantova is a sovereign post quantum Layer 1 built from scratch. This guide explains how to propose changes, report problems, and get your work reviewed.

## Before you start

Quantova is at the testnet and pre audit stage. Interfaces can still change while the network matures toward mainnet. Please keep that in mind when you build on top of the current release.

## Ways to contribute

* Report a bug or a gap by opening an issue on the relevant repository
* Ask and answer questions in the developer forum under the Q and A category
* Propose a protocol change through the QIP process in the improvement proposal repositories
* Improve documentation and worked examples in the developer content
* Send a pull request that fixes a defect or adds a well scoped feature

## Pull requests

1. Fork the repository and create a branch with a short descriptive name
2. Keep each pull request focused on one change so it is easy to review
3. Write a clear description that states what changed and why
4. Add or update tests where the change affects behavior
5. Make sure the existing checks pass before you request review

## Coding standards

Everything in Quantova uses Quantova vocabulary rather than names borrowed from other chains. Prefer clear names over clever ones. Match the style already present in the file you are editing. Do not introduce cryptography that a quantum computer running Shor could break, because the whole point of the stack is that it does not depend on such cryptography.

## Reporting security issues

Do not open a public issue for a security problem. Follow the process in SECURITY.md so that we can address it responsibly.

## Code of conduct

By taking part you agree to follow the CODE_OF_CONDUCT.md. Be respectful and keep the discussion focused on the work.
