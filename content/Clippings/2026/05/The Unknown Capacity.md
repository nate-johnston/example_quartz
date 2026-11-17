---
title: "The Unknown Capacity"
source: "https://crossingtheedge.substack.com/p/the-unknown-capacity?triedRedirect=true"
author:
  - "[[Clément Verna]]"
published: 2026-03-17
created: 2026-03-17
description: "How AI Agents are lowering the \"entry fee\" for technical contribution and redefining the Engineering Manager's reach."
tags:
  - "clippings"
  - "ai"
  - "agile"
---
### How AI Agents are lowering the "entry fee" for technical contribution and redefining the Engineering Manager's reach.

![a bunch of television screens hanging from the ceiling](https://images.unsplash.com/photo-1642775196125-38a9eb496568?crop=entropy&cs=tinysrgb&fit=max&fm=jpg&ixid=M3wzMDAzMzh8MHwxfHNlYXJjaHwyM3x8Z2l0aHVifGVufDB8fHx8MTc3MzczNzM5Mnww&ixlib=rb-4.1.0&q=80&w=1080)

Photo by Leif Christoph Gottwald on Unsplash

At a recent All Hands meeting, a Director shared a sentiment that has been echoing in my head. Speaking on the impact of Agentic Development, he said: *“Because of these tools, I don’t even know what my capacity is anymore.”*

That resonated with me deeply. As a Senior Engineering Manager at Red Hat working on CoreOS my day is typically a “chaotic manager workflow”: a collection of Slack messages, JIRA tickets, emails and back-to-back meetings. Traditionally, the role of an EM (Engineering Manager) is to create the environment for the team to succeed by setting strategy, empowering decisions, and shielding the team from toil.

In the last few weeks, however, I’ve been experimenting with an AI coding agent using OpenCode. I gave my agent access to JIRA, GitHub, and Jenkins with a primary mission: monitor our build pipelines, fetch logs, investigate failures, and create JIRA cards to track them.

But the impact of this experiment went much further than simple automation.

### Breaking the Context-Switch Barrier

One of the biggest challenges to deep technical work is the “context-switch penalty.” Traditionally, making a meaningful contribution requires a significant block of focus, time to set up an environment, internalize an unfamiliar codebase, or regain fluency in a specific language. This “entry fee” is often so high that it prevents contributions entirely, especially when your day is fragmented by meetings and support requests.

Recently, I used the agent to investigate a support request from our Slack channel. In a 30-minute window between meetings, I gave enough context to the agent, for it to discover the repos, go through the codebases and propose a fix. I only reviewed the code, and I opened the PRs:

- [openshift/release-controller #739](https://github.com/openshift/release-controller/pull/739)
- [openshift/oc #2215](https://github.com/openshift/oc/pull/2215)

These were small fixes, but without the agent, they would have remained “someday” tasks. The agent handled the “toil” of environment setup and code discovery, allowing me to focus entirely on the **intent**.

### Investigating the “Under the Hood”

The most impressive example was an investigation into a failure in Fedora CoreOS triggered by a dracut update in Fedora Rawhide. While I understand the high-level architecture of initramfs and rpm-ostree, I am not the person you’d ask to explain the “under the hood” mechanics of dracut internals.

I spent about an hour on a Friday morning guiding the agent. It compared logs between working and failing builds, searched GitHub repos for commits between versions, and identified the exact change that broke the tests.

I didn’t propose the fix myself since I lacked the architectural depth to know where the fix belonged but I provided a [detailed root cause analysis](https://gist.github.com/cverna/cf9413bc639a00ace792bf34e9d91171) to the upstream maintainers. This is a “superpower”: the ability to provide deep technical value during a gap in a manager’s schedule that previously would have required a dedicated IC’s afternoon.

### If This is True for Me, What About the Team?

The “Unknown Capacity” I’ve discovered as a manager is a signal. If these tools allow me to bridge fluency gaps and contribute to unfamiliar codebases in 30 minutes, the impact on Individual Contributors (ICs), who have the dedicated focus and deep architectural knowledge I lack, will be exponential.

However, as we unlock this capacity, we must remain grounded. **Technology is the Means, Not the End**. We are entering a world where code is cheaper to write than ever, but it is not necessarily cheaper to review or maintain. Agents will write bugs just like humans do, and the ability to keep code simple and small remains a vital principle. As leaders, it is more important than ever to remember *why* we are building a solution. Our job isn’t just to produce more; it’s to ensure that what we produce is sustainable.

I don’t yet know what the “new norm” for productivity is, but I know the ceiling has moved. I am no longer just managing a team; I am exploring how we all, managers and engineers alike, redefine what we are capable of achieving.

---

1 Like