# Quantova

Quantova is a post quantum Layer 1 blockchain. Its cryptography, virtual machine, contract language, and consensus are built on the NIST post quantum standards, so the keys, signatures, finality, and randomness that secure the network are designed to withstand both classical and quantum attack.

The stack is written to its own specification. The sections below describe the parts a developer works with directly.

## Q-Crypto, the cryptographic core

Q-Crypto is Quantova's implementation of the NIST post quantum standards, written from scratch against the published FIPS documents. It provides ML-DSA-65 for signatures under FIPS 204, ML-KEM-768 for key encapsulation under FIPS 203, SLH-DSA for a conservative hash based signature under FIPS 205, and SHA-3 with SHAKE for hashing under FIPS 202. Every algorithm is validated against the official NIST known answer vectors, and it is the single cryptographic dependency for the entire stack.

## QVM, the virtual machine

The QVM executes smart contracts as compiled containers on a deterministic register machine. Post quantum signature verification, hashing, and Merkle proof checking are native instructions, so a contract verifies a signature or a proof directly rather than reimplementing cryptography in bytecode. Arithmetic is checked, and a faulting execution reverts with no change to state.

## Quanta, the contract language

Quanta is the language contracts are written in, and it compiles to QVM containers. Assets are modeled as linear resources and authority as a capability, so a contract declares the operations it is permitted to perform and the compiler holds it to that declaration. The language is designed so that whole classes of common vulnerability, among them reentrancy, unchecked arithmetic, and value created or destroyed without accounting, are caught at compile time rather than left to runtime.

## QORUS, consensus and finality

QORUS is Quantova's consensus protocol. A committee is sampled for each round to attest to a proposed block, and finality is reached and recorded as a single aggregated certificate rather than a set of individual votes. The committee is bounded, so the work required to finalize a block does not grow with the size of the validator set.

## QVRF, verifiable randomness

QVRF is Quantova's verifiable random function, composed entirely from post quantum primitives. It supplies the randomness that samples the consensus committee, producing output that any party can verify and none can predict in advance.

## Q-Oracle, the bridge boundary

Q-Oracle is where a foreign chain is verified off the network and reduced to a post quantum attestation with a proof, so no foreign signature, key, or header ever reaches the post quantum stack. Assets bridged in are tagged by their origin and are never valid as validator stake, so only the native asset secures consensus.

## QCore, the client SDKs

QCore is the client library that derives keys, builds and signs transactions, and communicates with a node over its gateway. A single Rust core provides the JavaScript and Python bindings, so every language derives identical addresses and produces identical signatures. The JavaScript package is published on npm as @quantovainc/qcore.

Quantova is currently on testnet.
