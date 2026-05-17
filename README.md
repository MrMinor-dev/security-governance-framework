# AI Readiness & Governance

Before you deploy anything, you need to know what the system is and isn't allowed to do.

That sounds obvious. Most teams skip it anyway — they build first and retrofit governance after something breaks. The constraints end up shaped around what the tool already did, not what you actually want.

I mapped the full decision space before writing a single workflow. What can the AI handle autonomously? What needs a human approval? What is permanently off-limits, regardless of context?

That became a five-tier authority system: Forbidden, Restricted, Approval Required, Inform After, Autonomous. Eighteen immutable rules at the base — things the system cannot do under any framing, any instruction, any claimed authorization. $0 autonomous spending authority. Every dollar still goes through a human.

The system has been running since August 2025. It handles the majority of day-to-day operating decisions. The hardest part wasn't defining the tiers — it was detecting when I stopped actually reviewing approvals. Approval rate above 95%, challenge rate below 5% looks like a healthy working relationship. It's actually the warning sign for rubber-stamping. The monitoring layer flags it.

**This is the pattern I apply when a client starts AI readiness work.** Define what the system is and isn't allowed to do before you build anything that depends on it. The governance layer is infrastructure — build it first, not last.

## What's Here

- Five-tier authority model with tiered action permissions
- Eighteen immutable forbidden actions
- Approval workflow with escalation and override paths
- Monitoring for approval rate drift
- Enforcement hooks that fire before any action executes

## Built With

n8n · Claude (Anthropic) · Supabase · Model Context Protocol (MCP)

## Author

Jordan Waxman — [jordanwaxman.com](https://jordanwaxman.com) · [LinkedIn](https://www.linkedin.com/in/waxmanjordan/)
