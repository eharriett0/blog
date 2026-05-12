---
title: "Hello"
date: 2026-05-12
draft: false
tags: ["meta"]
summary: "Bootstrapping the blog. First post is the deploy smoke test."
---

This is a placeholder post to validate the Hugo + GitHub Pages deploy
chain. Real content lands once `just blog-export` ([#363](https://github.com/eharriett0/awesome-o/issues/363))
is wired in to pull polished drafts out of the brain.

The platform mines blog topic candidates from two sources: brain
chunks (Claude Code + ChatGPT exports) and incident-class doc sections
([#367](https://github.com/eharriett0/awesome-o/issues/367)). A scoring
agent ranks them, with a saturation clamp that demotes commodity topics
([#368](https://github.com/eharriett0/awesome-o/issues/368)). The
calendar agent picks one per week. The polish step happens in ChatGPT,
because the platform's principle is **the system should not replace
editorial judgment** — only reduce the effort to produce a credible,
grounded draft.

Maintenance is part of publishing. The
[`ContentMaintenanceAgent`](https://github.com/eharriett0/awesome-o/blob/main/agents/blogging/src/blogging/maintenance.py)
audits every URL in `blog_published_posts` monthly for decay (broken
links, deprecated commands, stale version pins). Tickets go to ntfy.

That's the loop.
