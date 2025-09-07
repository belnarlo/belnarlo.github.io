+++
title = 'Taming Homelab Chaos: How I Finally Got Organized'
date = 2025-09-17T16:00:00Z
draft = true
categories = ["personal", "learning", "infrastructure"]
tags = ["homelab", "organization", "productivity", "project-management"]
series = ["homelab-journey"]
description = "The story of how I went from having too many half-finished projects to a structured approach that actually works"
+++

## The Problem: Too Many Shiny Objects

Like many IT professionals, my homelab suffered from what I call "Shiny Object Syndrome." Every interesting technology became a new project, every problem spawned three more "quick fixes," and my todo list grew faster than my ability to complete tasks.

The breaking point came when I realized I had:

- Projects scattered across **Todoist**, **Obsidian**, and my brain
- Half-configured services that only worked via LAN *or* Tailscale (never both)
- A growing list of "I'll fix that later" issues
- Zero documentation for future me

Sound familiar?

## The Catalyst: Network Connectivity Chaos

The final straw was discovering that some of my services only worked when accessed via my local network, while others only worked through Tailscale. Simple things like SSL certificates weren't automated, and I was spending more time firefighting than building.

I needed a system. Not just for the technical problems, but for managing the **chaos of ideas** that is a modern homelab.

## The Solution: A Prioritization Matrix

Instead of trying to fix everything at once, I created a **tier-based prioritization system**:

### Tier 1: Critical Infrastructure

The blockers that prevent everything else from working:

- ✅ **Documentation workflow** (this blog!)
- 🔄 **Network connectivity fixes** (LAN vs Tailscale issues)
- ⏳ **SSL certificate automation**
- ⏳ **Vault productionization**

### Tier 2: Platform Extensions

Building on what already works:

- **Complete SaltStack management** of all systems
- **Comprehensive monitoring** with Zabbix and Grafana
- **NetBox deployment** for infrastructure documentation

### Tier 3: New Services

The fun stuff (once the foundation is solid):

- **ESP32 sensor network** for environmental monitoring
- **Jellyfin evaluation** (Plex replacement testing)
- **NextCloud deployment** for self-hosted productivity

### Tier 4: Learning Projects

Future skills development:

- **Talos Kubernetes cluster** for container orchestration learning
- **Advanced automation** experiments

### Tier 5: Personal Projects

Because burnout prevention is critical:

- **Guitar learning** (15 minutes daily before any IT work)
- **Electronics projects** (guitar pedal currently in progress)

## The Workflow: Obsidian + Claude

Here's where it gets interesting. Instead of fighting against my tendency to have ideas faster than I can implement them, I built a workflow that captures and processes them systematically:

**Daily Planning Template:**

```markdown
## Today's Focus
- [ ] Primary project: [ONE THING FROM TIER 1-2]
- [ ] Secondary task: [SMALL WIN]
- [ ] Guitar practice: 15 min ⏰

## Claude Consultation
Context: [Current homelab status and blockers]
Question: What should I prioritize today?
Response: [AI-assisted decision making]
```

*The Secret Sauce:* Using Claude AI for project consultation. By providing context about my current infrastructure and goals, I get objective prioritization advice that cuts through the noise of "but this would be really cool to try."

## Early Results

Three weeks in, the approach is working:

1. Focus Improved: One primary project at a time, with clear next steps
1. Documentation Happening: This blog post exists because I prioritized the writing workflow
1. Stress Reduced: Guitar practice before homelab work centers my mindset
1. Progress Visible: Clear metrics for what's actually getting done

## The Technical Stack

### My current homelab foundation

- Proxmox for virtualization
- SaltStack for configuration management
- Zabbix + Grafana for monitoring
- Tailscale for secure networking
- HashiCorp Vault for secrets (being productionized)
- Docker managed via Salt (no manual container deployment)

## Lessons Learned So Far

### What's Working

- Tier-based prioritization prevents scope creep
- Daily guitar practice genuinely improves technical focus
- AI consultation provides objective project advice
- Documentation-first approach is already paying dividends

### What's Still Hard

- Resisting new project temptation when the current work gets tedious
- Estimating effort accurately for complex infrastructure changes
- Balancing learning time with productive work

### Unexpected Benefits

- Writing clarifies thinking - explaining problems helps solve them
- Public documentation creates accountability for follow-through
- Systematic approach reduces decision fatigue

## What's Next

The immediate focus remains Tier 1 completion:

- Fix network connectivity issues (LAN vs Tailscale access)
- Automate SSL certificates for all services
- Productionize Vault with proper TLS and backup

Once the foundation is solid, I'm particularly excited about the E8SP32 sensor network project* - bridging physical and digital monitoring appeals to both my technical and maker instincts.

## For Fellow Homelab Enthusiasts

If you're drowning in half-finished projects and good intentions, consider:

- Audit your current chaos - list everything that's "in progress"
- Create dependency maps - what's blocking what?
- Ruthlessly prioritize - foundation before fun features
- Document the journey - future you will be grateful
- Include non-IT activities - burnout kills productivity

The goal isn't to eliminate all projects, but to approach them systematically. A well-organized homelab is more fun than a chaotic one, even if it takes longer to get there.

---

Next post: "When Networks Collide: Debugging LAN vs Tailscale Access Issues" - the technical deep-dive into my current Tier 1 priority.
*Series Navigation:*
← Previous: This is the first post
→ Next: Coming soon: Network connectivity debugging