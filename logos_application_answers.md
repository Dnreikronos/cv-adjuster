# Logos - Decentralised Messaging Engineer (Rust) - Application Answers

## Link to publicly available projects

https://github.com/Dnreikronos | https://www.linkedin.com/in/blsoaresdev/

---

## What attracted you to this opening?

I've been writing Rust in open source (53 PRs to Zed, two ZK proof projects) and building on Ethereum and Solana for the past couple of years. This role sits at the intersection of those two things — Rust and cryptographic protocols — but applied to messaging, which is a problem I actually care about.

What got my attention specifically was MLS and the SDK focus. I've worked with cryptographic primitives directly (halo2, arkworks, Groth16 proof circuits), so I'm not new to reading specs and turning them into Rust code. But I haven't had the chance to work on messaging protocols at this level, and the idea of building a reference SDK that other developers use is the kind of work I want to be doing.

The small team, async-first setup also matters. Every role I've had has been remote, and I do my best work when I can think through problems without meetings breaking up the day.

---

## What is your favourite messaging app? - and why?

Signal. It does one thing well and doesn't try to be a platform. The protocol design is solid — Double Ratchet gives you forward secrecy and break-in recovery without the user having to think about it. No ads, no social graph mining, no feature bloat.

I also respect that the Sealed Sender work actively tries to minimize what the server can learn about who's talking to whom. Most messaging apps protect content but leak metadata freely. Signal at least takes that problem seriously, even if it's not fully solved.

The thing I'd change: it still depends on phone numbers for identity, which ties your account to a telecom provider. That's the kind of problem decentralised identity could actually fix.

---

## Why do you think you're a good match for this opening?

I write Rust and I'm used to working in large Rust codebases. 53 PRs to Zed across 15+ subsystems, including deadlock fixes in the rendering framework, state machine bugs, and platform-layer code. I can read unfamiliar Rust, understand the architecture, and ship changes that don't break things.

I've also worked directly with cryptographic primitives in Rust. DarkPool-Exchange uses halo2 and arkworks for ZK proof generation and aggregation. zkSettle verifies Groth16 proofs on BN254 curves on-chain. I'm comfortable with the math and the Rust libraries around it. MLS is a different domain, but reading a cryptographic spec and turning it into correct Rust is something I've done before.

On the decentralised side, I've been building smart contracts, mentoring 60+ developers on blockchain architecture, and participating in hackathons (NearX, ZKVerify, Cypherpunk) for years now. I'm not approaching decentralisation as an abstract idea; it's where I've been putting my time.

---

## Where do you learn about new technology / industry?

Mostly by reading source code and specs directly. When I started contributing to Zed I didn't read blog posts about GPUI — I read the framework code. Same approach with MLS: I'd go to RFC 9420, then look at OpenMLS's implementation to see how the spec maps to Rust.

Beyond that: GitHub trending for Rust projects, the Rust subreddit and This Week in Rust for ecosystem news, Hacker News for broader tech, and Twitter/X for the crypto and P2P space (following people like the Waku team, libp2p maintainers, and protocol researchers). I also follow the Ethereum and Solana research forums when something relevant comes up.

For deeper learning, I build things. That's how DarkPool-Exchange and zkSettle happened — I wanted to understand ZK proofs properly, so I wrote the circuits myself.

---

## Would you be willing to accept part of your payment in Crypto?

Yes. I've been in the Web3 space for years and hold crypto already. Happy to receive part of my compensation that way.

---

## What are your thoughts on decentralisation?

Decentralisation matters when it solves a real problem, not as an end in itself. Messaging is one of the clearest cases: right now, private conversations between two people go through servers controlled by a single company. Even with end-to-end encryption, the company still knows who talks to whom, when, and how often. That metadata alone is enough to map out someone's life.

A decentralised messaging layer removes that single point of control. No one entity can decide to shut down the service, hand over metadata to a government, or change the privacy guarantees. Users keep their conversations without trusting a company to keep its promises.

That said, decentralisation is hard to get right. It's slower, coordination is harder, and user experience usually suffers compared to centralised alternatives. The projects that actually get used are the ones where decentralisation is invisible — you get censorship resistance and data ownership without needing to understand the plumbing. That seems to be what Logos is going for with messaging, and I think it's the right call.

---

## What are your pay expectations?

$120,000 - $150,000 USD gross annually, depending on scope and crypto/fiat split.

---

## Are you an existing member of our community?

No, but I've been around the Ethereum, Solana, and NEAR ecosystems for a while — hackathons, open source, and mentoring Web3 developers at Borderless Coding.
