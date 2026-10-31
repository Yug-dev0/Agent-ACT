# Public build-story draft

> **Project:** Agent-ACT  
> **Maker & Author:** Yug Patel ([@yug-dev0](https://github.com/yug-dev0))

Use this as the basis for a LinkedIn/X post for the optional community prize. Replace the bracketed text with your
own voice and add a short screen recording or three screenshots: incident, TrueForge approval, recovery.

## Suggested LinkedIn post

> I built **Agent-ACT** for the moments when production fails at 2 a.m. and the on-call engineer needs evidence,
> not another dashboard tab.
>
> The job I handed to an agent: investigate a checkout outage, prove the cause from metrics/logs/database state,
> try the lowest-risk fix, and verify whether it actually worked.
>
> The interesting part was not getting an agent to restart a service. It was making sure it *noticed* that the
> restart did not solve the real defect: a new payment-service version exhausted its database connection pool.
>
> Agent-ACT runs on **TrueForge**. The agent reaches a real MCP server, writes and executes diagnostic Python in a
> sandbox, and gets stopped by TrueForge before it can roll back production. A human sees the evidence brief and
> must approve the exact `v2 → v1` rollback. The server independently attests that approval before switching traffic.
>
> After the rollback, recovery is not a claim: Agent-ACT requires readiness, 20 synthetic checkouts, error rate,
> latency and database usage to meet configured thresholds before it says `RECOVERED`.
>
> The hard lesson: a command returning success is not the same as an incident being resolved.
>
> [Add your demo link] · [Add your repository link: https://github.com/yug-dev0/Agent-ACT]
>
> #AgentACT #agentsthatact #TrueForge #TrueFoundry #SRE #AIAgents #YugPatel

## Suggested caption for the approval screenshot

> The model can recommend a rollback. It cannot authorise one. TrueForge holds the exact tool call until a person
> decides, and Agent-ACT refuses to execute without a matching, single-use attestation.

## Posting checklist

- State only results visible in your own recording.
- Tag `@truefoundry` and `@polariscodes` and use `#agentsthatact`.
- Do not show `.env`, API keys, browser profiles, or internal session URLs.
- Link the public repository and the short demo video.
