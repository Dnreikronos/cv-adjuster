# Tempo Application Answers

## Why Tempo?

I've been writing Rust in open source (Zed editor, 53 PRs, 6,800+ lines) and building on Ethereum on the side for the past couple of years. Both are things I do because I want to, not because someone's paying me. Tempo is where those two things become the actual job.

What got my attention specifically: the focus on performance and benchmarking in Rust, close to the Execution Layer. I built a dark pool DEX where ZK proofs settle on-chain through a Solidity verifier on the EVM, and a compliance layer that verifies Groth16 proofs on BN254 curves, the same curve behind Ethereum's precompiles. Every time I work on these projects I end up reading reth source code or EVM specs to understand what's happening on the other side of the transaction. I'd rather work on that side directly.

I also like that this role expects you to figure things out without a clear spec handed to you. Most of my Zed contributions started with a vague bug report and zero obvious path forward. That's where I do my best work.

## Provide (2) examples of your exceptional engineering abilities

1. Concurrency bug in an invoicing pipeline, 140M+ monthly transactions

At Platform Builders (RD Saúde, Brazil's largest pharmaceutical retailer), invoices were intermittently failing fiscal compliance checks. The failures were sporadic and hard to reproduce, which is why they'd been open for a while before I picked them up. It turned out to be a race condition in the Kafka consumer pipeline: multiple goroutines were reading and writing shared invoice state without synchronization. Under load, two consumers could process the same invoice concurrently and produce conflicting fiscal data.

I added mutex-based locking to the critical section and reworked the consumers to enforce idempotency at the message level. Result: 99.99% idempotency, zero duplicate invoices, no downtime during the rollout. The system processes 140M+ transactions a month. The finance team had been correcting compliance failures by hand every week, so the fix also saved them several hours of that.

2. macOS deadlock in Zed's GPUI rendering framework (Rust)

Zed is a code editor written in Rust (70k+ GitHub stars). Users were reporting full freezes on macOS with certain keyboard input sequences. I dug into the GPUI rendering framework and found that a key status change handler was being called re-entrantly: a key event triggered a status update, which triggered another key event, which deadlocked the main thread. The tricky part was that it only happened with specific macOS input method configurations (CJK keyboards, third-party input tools), so most developers on the team couldn't reproduce it. I had to set up the exact input method and step through the event loop to actually see the re-entrancy happen.

Fixed it by restructuring how key status changes propagate, deferring status updates instead of processing them inline. PR #51035, merged. Eliminated the freeze for macOS users on non-standard input methods.
