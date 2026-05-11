Fractile Application Answers


Please tell us about a time you most successfully hacked some (non-computer) system to your advantage.

When I started contributing to Zed, I didn't have a Rust job or formal Rust credentials. So I picked the issues nobody wanted — obscure rendering bugs, platform-specific edge cases on Linux/X11, floating-point tolerance problems in terminal layout. Unglamorous stuff, but each one forced me to read deep into unfamiliar subsystems. After a few merged PRs the maintainers started recognizing my name, and now I have 30 merged across 15+ subsystems. I got in through the side door by doing the work nobody was competing for.


Please tell us in one or two sentences about the most impressive thing other than this startup that you have built or achieved.

I found and fixed a deadlock in Zed's GPUI rendering framework that was freezing the editor on macOS — traced it through the event loop and platform bindings to isolate a re-entrancy issue. Zed has 70k+ GitHub stars and I have 30 merged PRs with 6,800+ lines of Rust across 15+ subsystems.


Tell us about things you've built before. For example apps you've built, websites, open source contributions. Include URLs if possible.

Open source: 56 PRs (30 merged) to the Zed code editor in Rust — rendering, concurrency, terminal, debugger, platform layers. https://github.com/zed-industries/zed/pulls?q=author%3ADnreikronos

DarkPool-Exchange — ZK dark pool DEX. I built the Rust layer: halo2/arkworks proof circuits, client-side proof generation compiled to WASM and native CLI, proof batch aggregator. https://github.com/Dnreikronos/DarkPool-Exchange

zkSettle — ZK compliance infrastructure for Solana stablecoins. On-chain Rust program verifying Groth16 proofs in under 200K compute units, off-chain Rust workspace with axum API gateway. https://github.com/yuribodo/zksettle

Auto-Issue — Go backend that takes a GitHub issue, sends it to an AI agent, and produces a PR. Work queue, concurrency limiter, git worktree isolation, SSE streaming. https://github.com/yuribodo/auto-issue

Crypto-Tip — Solidity + Rust tipping platform for open-source funding (34 stars). https://github.com/Dnreikronos/crypto-tip

Zed OCaml extension — 5 merged PRs: Dune package management, MLX file support, LSP argument forwarding. https://github.com/zed-extensions/ocaml/pulls?q=author%3ADnreikronos


List any competitions/awards you have won, or papers you've published.

No awards or publications. I've participated in three hackathons (NearX & ZKVerify, Cypherpunk, HB02-2025) and shipped working projects at each, but didn't place.


List any entrepreneurship programs, clubs, or hacker houses you have participated in or are currently participating in.

Borderless Coding (Sep 2025 – present) — Web3 Technical Mentor & Ambassador. Mentoring 60+ professionals on Rust-based smart contracts and blockchain architecture, running 20+ live workshops.
