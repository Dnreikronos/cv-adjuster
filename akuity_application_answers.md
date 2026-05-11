# Akuity - Application Questions

## Do you have experience in start-up environments building from 0-1? If so, please explain.

I haven't worked at a startup, but I've done a lot of 0-1 building on my own projects.

Auto-Issue started as an empty repo -- I built the full Go backend myself: orchestrator, work queue, concurrency limiter, git worktree isolation, SSE streaming, REST API with 15+ endpoints, PostgreSQL persistence. Every architecture decision was mine.

Same with DarkPool-Exchange and zkSettle -- greenfield projects where I designed the system, wrote smart contracts, and built the off-chain Rust services and API gateways from scratch. I've gone through the "nothing exists, figure it out" cycle enough times that I'm comfortable with it.

At Docile Alimentos (not a startup, but the situation was similar), I led a monolith-to-microservices migration where nobody had done it before. I picked the service boundaries, set up Docker deployments, wrote the first Go services, and onboarded the team as we went.

## Briefly describe your hands-on experience building or operating Kubernetes infrastructure in production, including any controllers/operators, multi-cluster environments, or GitOps workflows you've worked with.

At Platform Builders (contracted to RD Saúde), I work with containerized Go microservices on Kubernetes and Docker, deployed on Oracle Cloud Infrastructure. The system handles 140M+ monthly transactions. Most of my time goes into managing deployments across environments, debugging containerized services when things break, and maintaining the CI/CD pipelines that push to our clusters.

I haven't built custom Kubernetes controllers or operators. What I have done is operate production K8s workloads day to day -- pod failures, resource limits, release coordination, the operational side. I also work with AWS (EC2, S3, RDS, Lambda, EKS) and use Docker constantly.

For infrastructure changes and deployments, I use Git-driven workflows -- config lives in Git, changes go through PRs. I haven't used Argo CD or Kargo directly, but the patterns are familiar. And I learn new tooling quickly: I went from never having seen the Zed codebase to 56 PRs (30 merged) across 15+ subsystems in about 2.5 months, so ramping up on your stack isn't something I'm worried about.

## What makes you uniquely qualified for this role? (can be short bullet points!)

- 6+ years backend, 3+ in Go. It's my main language -- not something I picked up for a side project.
- Fixed a concurrency bug in a Kafka pipeline processing 140M+ monthly transactions. I debug production systems, not just build them.
- Migrated Oracle to PostgreSQL, rewrote execution plans, cut worst-case query times by over a minute.
- 56 PRs (30 merged) to the Zed code editor (70k+ stars, Rust) in ~2.5 months. I get productive in large unfamiliar codebases fast.
- Spent real time working on a developer tool (Zed) used by thousands of people. That changes how you think about DX.
- Built multiple Go projects from zero: orchestrators, work queues, REST APIs, real-time streaming, PostgreSQL.
- Kubernetes, Docker, AWS, Prometheus, Grafana in production daily.
- BS in Computer Science. Remote since 2020. GMT-3, overlaps with US Eastern.
