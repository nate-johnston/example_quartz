---
title: "(24) AI's Two Bottlenecks and One Real Threat: Reflections from Red Hat Summit 2026"
source: "https://www.linkedin.com/pulse/ais-two-bottlenecks-one-real-threat-reflections-from-red-pablo-casal-k78uf/"
author:
  - "LinkedIn"
published: 2026-05-19
created: 2026-06-22
description:
tags:
  - "clippings"
  - "ai"
---
---

Back from Atlanta. Three buildings of the Georgia World Congress Center packed for four straight days, more than **6,500** people on the floor, and for the **first time** in Red Hat Summit history a company originally from LATAM had its own **booth**. That was us, **netlabs**. And that same week we became the **first AI Red Hat Specialized Partner worldwide**. Two firsts I will not forget.

> And that same week we became the **first AI Red Hat Specialized Partner worldwide**. Two firsts I will not forget.

But I did not fly to Atlanta to celebrate either of those milestones. I went looking for signals. Specifically, I went to test **three ideas** I have been carrying around for **months**. Three things I believe will define what kind of revolution AI actually becomes: two technical bottlenecks that determine **how much power** AI can really deliver inside a serious enterprise, and one **societal threat** that has more to do with timeframes than with technology itself.

The Summit either confirmed them or it did not. It mostly did, with some **interesting** wrinkles.

### The Industrial Revolution analogy is not hyperbole

I do not usually like dramatic framings. But I think it is fair to say AI is probably the **most consequential revolution since the Industrial Revolution**. Certainly the biggest **leap** in **emergent behavior** since we **connected** every **computer** on the planet through the **Internet**, an event that also reshaped society in ways no one fully predicted at the time.

We are seeing the tip of the iceberg. Red Hat's own **CTO Chris Wright** noted publicly at Summit that he has never seen technology *evolve at the current rate in his two decades* at the company, and that he expects the velocity to **keep accelerating**.

### A weekend of liberation

Let me anchor all of this with something I did yesterday. On a Sunday. In a few hours.

I built an iPhone app that transcribes any voice recording into text. Yes, plenty of apps already do this. The difference is that mine does it **using** the **idle capacity** of my **gamer PC** and its **4090**, sitting at home. Open source software end to end: WhisperX for transcription, Qwen for downstream processing. I benchmarked it against ElevenLabs Scribe, the current market leader for this task, and it performs at roughly **99% of Scribe's accuracy**.

The **thousand dollars** a year I will save is the least interesting part. What I really gained is the **privacy** of being able to transcribe any audio, personal or professional, with the **absolute peace of mind** that **nobody** else will **ever see** that data. If I wanted to, I could record and transcribe twenty-four hours of my day, for free, without ever **sending a byte** to anyone's **cloud**.

But here is the part that matters most. The whole thing runs on the same digital infrastructure Red Hat offers, which means I have **governance**, **control**, **support**, and a clear **path to scale**. If tomorrow I want to take this from personal use to "every netlabber uses it across the company," the **architecture** does **not change**. Same stack, same controls, just more nodes.

This is the kind of move that **liberates** and **empowers** us as a **society**. The alternative is to keep building our daily lives on closed systems run by a handful of companies more **powerful** than most **superpowers**. I know which path I want to be on.

And that is exactly why I went to Atlanta. To see whether the **foundation** that makes this kind of move **possible** is actually **maturing** into something every enterprise **can stand on**, not just engineers who happen to enjoy spending their Sundays compiling models.

### Two unlocks and one reckoning

Out of everything I saw and thought through at Summit, **three threads** stayed with me. Two of them are **bottlenecks** in the engineering sense: solve them and the **real power** of these models genuinely shows up in production environments, instead of being trapped in demos and proofs of concept. I prefer to call them **unlocks**, because that is exactly what they do. They open the door from "AI is impressive in a notebook" to " **AI runs the business.**"

The third one is different. It is not a bottleneck to be unblocked by engineers. It is a **reckoning** to be **navigated**, deliberately and with **eyes open**. It is what makes me uneasy when I read the headlines, not the technology itself but the **pace** at which we are being asked to **absorb** it. That is the **threat** I want to talk about.

Let me take them one at a time.

### Unlock #1: Privacy vs capability

The first unlock is the one most engineers feel the moment they try to build something **serious**.

I can run a **powerful** **open source** model on my own GPU. I keep every **sensitive** piece of context inside my **perimeter**. Beautiful for **sovereignty**. But the frontier models running in the public clouds, the Opuses and the GPTs and the Geminis of the world, are **simply more capable**. So today every team faces a binary: **privacy or power.**

What I have been calling **Hybrid AI** is the obvious shape of the answer. A **local**, **private** model handles **sensitive context**. When it needs more **horsepower**, it consults a frontier model. The catch is that we do not have a clean way to guarantee that the local model does not **leak private context into that consultation**. Put a **heuristic filter** in the middle and you trade off coverage. Put a **guard model** in the middle and you have to decide whether that guard runs local (and is **too weak** to catch sophisticated leakage) or in the cloud (and has already **seen the data** you were trying to protect).

This problem is genuinely **unsolved**. And it matters more than people realize, because as long as it is unsolved, every **regulated enterprise**, every **hospital**, every **government agency**, every **law firm**, every **bank** has a **hard ceiling** on how deeply they can **integrate AI** into their actual workflows.

What **encouraged** me at Summit is that **Red Hat** is now publicly **working** in this **direction**. Their own internal deep research agent, a system of roughly **two hundred** coordinated agents, now **routes 85%** of its calls to open weight models running on Red Hat's own infrastructure rather than to a frontier model. They started with frontier models, did the work to figure out what could be **replaced** with **smaller open models** running **locally**, and found that not only did **cost drop**, the results actually **got better.** That is the **Hybrid AI** thesis playing out at scale inside a serious enterprise.

The Summit announcements lean in further. Red Hat AI 3.4 ships a Model-as-a-Service layer that lets organizations expose models through a **governed**, OpenAI-compatible interface, with **consumption tracking** and **policy enforcement**, all running on infrastructure the **organization controls**. OpenShift AI 3.4 now includes on-premises telemetry and consumption tracking, together with Red Hat Lightspeed, so you can monitor and manage your AI workloads **without sending operational data out of your sovereign boundary**. Confidential containers on NVIDIA infrastructure protect models and data even from other workloads on the same cluster. And the sovereignty framing Red Hat formalized this year, **model sovereignty**, **data sovereignty**, and **outcome sovereignty**, names the problem cleanly: you need to **choose** your **models**, **control** your **data**, and **audit** every **decision**.

None of that fully closes the leakage tension. But it is the right kind of progress. It moves enterprises from " **you cannot have both** " to " **here is the architecture where you might.**"

### Unlock #2: Freedom vs control in agentic systems

The second unlock is the one that will dominate the next two years of AI engineering work.

OpenClaw is the perfect illustration. It became the **fastest** growing **open source project** in history by giving **agents radical freedom**: full **credentials**, full **tool access**, the ability to **rewrite themselves**, the ability to **do** almost **anything** in pursuit of a **goal**. And the results are genuinely **astonishing**. The emergent behavior is the kind of thing that makes you stop dead on your feet and ask yourself, *is this for real? Am I* ***really living this moment*** *in* ***history****?*

But the same radical freedom that produces this almost **human-like behavior** also produces astonishing **failure modes**. Agents **leaking credentials**. Agents **posting private keys** publicly. Agents **deleting mailboxes**. Agents making **purchases nobody approved**. The same property that enables **breakthrough** is the property that enables **disaster**.

Lock the agent down with too many **guardrails** and the **emergence vanishes**. You get predictable, **boring**, expensive automation that could have been more efficiently achieved with **bash scripting or Ansible**. Finding the exact **balance** where emergent **intelligence** survives but catastrophic **mistakes** do not is the other **unsolved problem**.

Red Hat made some of the most substantive announcements I have seen on this front. AgentOps in Red Hat AI 3.4 brings **end-to-end tracing**, **observability**, **cryptographic identity for agents**, lifecycle management, and **automated red-teaming** through tooling like Garak and Chatterbox Labs. Red Hat Desktop, now generally available, gives developers a sandboxed environment to build and iterate on agents **without** those agents **touching** **production** data or infrastructure. The partnership with NVIDIA on the OpenShell project brings that sandboxing all the way from the developer laptop to production clusters. Confidential containers protect agents from each other, so a compromised agent cannot cascade into a compromised platform.

This is **real progress**. It is not solved. But for the first time I can see the **shape** of what " **solved** " looks like: agents with cryptographic **identities**, every action **traced** and **auditable**, every credential **scoped**, every workload **sandboxed**, with red teams running continuously in the background. That is a defensible architecture. It is also a **long way** from where most enterprises are **today**.

### The reckoning: a revolution in years, not decades

The third thread on my list is different. It is not a technical **unlock**. It is a **reckoning**, and I want to be **careful** with how I frame it.

Do not get me wrong. I **love technology**. I love **innovation**. I have spent **my whole life pushing** the **envelope of the art of the possible**. I waited my **entire career** to see **AI actually materialize**, and I am **thrilled** to be living through this **moment**. The issue is not the moment. The issue is the **pace**.

The Industrial Revolution reshaped society. Everyone had to **adjust**. There was no opting out, and there is no opting out of **this one either**. But the Industrial Revolution gave people **decades** to absorb the change, generations even. AI is asking us to absorb a comparable shift in **years**, possibly less.

Look at the intervals. **Three** and a half years ago **ChatGPT shipped**. Less than a **year** later, Llama 2 made open **weights real**. Then DeepSeek shocked the **cost curve**. Then practical **agentic coding** showed up. Then **OpenClaw** became the fastest growing open source project in history. The gaps are **collapsing**.

The doubling time of AI capability is now **shorter** than the **planning cycle** of most enterprises. **CFOs** cannot **budget** against it. HR cannot retrain against it. **Boards** cannot **govern** against it. **Auditors** cannot **keep up**. **Schools** cannot rewrite **curriculum** fast enough.

I am not going to pretend I **know** how this **plays out**. Maybe the wave creates more opportunity than it destroys, the way previous technological transitions ultimately did. Maybe entire categories of work **disappear** and entire new categories **appear**. Honestly, **nobody** **really knows** yet. What I do know is that **everything** is going to **change**, probably more **deeply** than most people are **willing to admit**, and the speed of that change is the part **nobody is ready for**.

That is the **threat**. It is not "AI is bad." It is not "robots are taking the jobs." The threat is the **timeframe**. We are being asked to do in **years** what previous transitions did in **generations**, and there is no **historical precedent** for how a society handles that. Maybe it ends well. Maybe it ends roughly. Either way, the responsible move is to **take it seriously now**, prepare with intention, and stop assuming we will have time to figure it out as we go.

This is where Red Hat's **framing** actually **does help**, even though no platform vendor can **solve** a **societal challenge** by itself. The entire thesis behind " **the right foundation**," running any model on any accelerator in any cloud with consistent governance, is essentially an **absorption** layer. If your platform can keep pace with model evolution without rebuilding your stack every quarter, then your organization has a **fighting chance** to **absorb** the wave instead of being knocked over by it.

That is not a complete answer to the reckoning. But it is a **meaningful** one. It buys time, preserves optionality, and keeps the **adjustment** in the hands of the people who **run the organization** rather than the people who **sell the model**.

### What worries me most: the concentration

Step back from the two unlocks and the reckoning. What honestly worries me most about where AI sits today is not the technology. It is the **concentration of power**.

**Three or four** companies **own** the frontier models that everyone else is **paying to use**. As AI moves from helpful tool to constant assistant, that concentration matters more, not less. Going forward, almost anything we do we will **probably do with an assistant**, or at least consult one before deciding. That is true at the individual level, at the team level, and at the enterprise level. How we **see work**, how **we work**, how we **make decisions**, probably even the **business models** we build, will be **reshaped** by AI participation.

Leaving the rails of that future in the hands of three or four model providers should make every **CIO** and every **regulator** **uncomfortable**.

**Matt Hicks** (Red Hat's CEO) framed it well at Summit: *the companies that win this era will not be the ones who bet on a particular vendor, a particular cloud, or a particular model. They will be the ones who picked the right foundation to stand on, regardless of which model, cloud, or vendor leads the next twelve months*. I **agree completely**. And I would push it one **step further**. The **winners** will be the ones whose foundation lets them **solve these two unlocks** on their **own terms**, with their **own data**, their **own controls**, and their **own auditability**, and lets them absorb the **reckoning** at their **own pace**, not at **someone else's** rented permission.

This is exactly what an open source platform like Red Hat **enables**. Not because Red Hat solves these problems for you, but because it gives you the **rails** to **solve them yourself**, in production, with the governance and the enterprise support that the reality of regulated industries actually demands.

The market signal is loud. **Gartner** expects **sovereign** cloud **spending** to reach **$80B** in 2026, growing **36% year over year.** That is not a compliance footnote. That is a structural shift in how serious enterprises are choosing to build.

### Where this leaves netlabs

I want to close with a paragraph that is **honest** about my **position**. I run **netlabs**, a **boutique** open source **consultancy**. Our purpose is to empower people and companies to achieve **amazing feats**. Our strategy is, plainly, **engineers in command**: real engineers at the **center of the work**, not a layer of slideware between the customer and the system. Our brand promise is **Production, not PowerPoint**. We deliver **hands-on**, open source-powered **digital transformation** across DevOps, Cybersecurity, Data, and Gen-AI for **governments**, **telecom** leaders, **manufacturers**, and other large enterprises.

This year we became the **first AI Red Hat Specialized Partner worldwide**. That is not a marketing line. It reflects the **work** we have been doing for **years** in exactly the territory I described above: **helping enterprises** build **governed**, **sovereign**, **hybrid AI** architectures on Red Hat, with **real engineers** in the room, doing **real modernization** to actual **production**, not pilots that die on a conference stage.

If you are a **CIO**, a **VP of Infrastructure**, or a **head of platform** looking at **AI** and feeling the **tension** between what your **board** is asking for and what your **platform can actually deliver**, this is the **conversation** we **want to have with you**. Not a deck. A workshop. A migration. A **working** **hybrid AI architecture** where **your** data **stays** where it **should**, **your** **agents** are **governed**, and **your** platform **absorbs the pace of change** instead of **breaking** under it.

### Owning the rails

The two unlocks and the reckoning I went to Atlanta to test **are real**. The unlocks **are not** going to be fully **solved** this **year**. The **reckoning** is already **underway**. But the open source ecosystem, with **Red Hat** as its **enterprise flagship**, is building the infrastructure that **gives us a fighting chance to navigate all three on our own terms**, at our **own pace**, with **auditability** and **control** built in.

**Owning the rails matters more than ever.**

**AI** is about to **change everything**. Make sure the change happens on **rails you can see**.

More to come.

---

***Pablo Casal*** *is the* ***CEO*** *of* ***netlabs****, the* ***first AI Red Hat Specialized Partner worldwide****.* ***netlabs*** *delivers* ***open source-powered digital transformation*** *across* ***DevOps****,* ***Cybersecurity****,* ***Data****, and* ***Gen-AI*** *for* ***governments****,* ***telecom*** *leaders,* ***manufacturers****, and large enterprises.*

*#RedHatSummit2026 #OpenSource #HybridAI #AIGovernance #SovereignAI #netlabs*