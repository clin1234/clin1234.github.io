<base href="https://clin1234.github.io/">
<nav>
      <a href="index.html">Home</a>
      <a href="projects/index.html">Projects</a>
      <a href="aboutme.html">About Me</a>
      <a href="blog/index.html">Blog</a>
      <a href="resources.html">Helpful Resources</a>
      <a href="https://github.com/clin1234/">Github</a>
</nav>

# Utterances of a Cynic

## AGNTCon + MCPCon 2026: a plugin, too many booths, and one Lego set

Posted on October 24, 2026.

I spent October 22–23 in San Jose at [AGNTCon + MCPCon North America](https://events.linuxfoundation.org/agntcon-mcpcon-north-america/). I came to learn more about agentic development, present my experience building a Claude Code plugin, and see what people were making with MCP. Judging by how I actually spent the two days, I also came to inspect nearly every sponsor booth.

The [schedule](https://events.linuxfoundation.org/agntcon-mcpcon-north-america/program/schedule/) was full of talks I wanted to attend. My ability to leave an interesting conversation in time for one needs work.

### Before the conference

The festivities started on October 21 at the [AI Community Bash, featuring De La Soul](https://events.linuxfoundation.org/agntcon-mcpcon-north-america/program/schedule/?id=1292533). I got to chat with PyTorch attendees on their conference's last day before starting my own two-day excursion.

As I admitted in [my first update](https://lnkd.in/p/eZcuucXP), I probably could have exercised more restraint around the drinks. A sensible observation to make after the fact.

### Day 1: MCP updates, then straight to the booths

Keynotes can test my patience, but a couple of things caught my attention. One was [David Soria Parra's “MCP and the Era of Connectivity”](https://events.linuxfoundation.org/agntcon-mcpcon-north-america/program/schedule/?id=1288844). Soria Parra, from Anthropic, is a co-creator of the Model Context Protocol. His updates on Tasks and skills over MCP gave me something concrete to look into afterward.

The [Tasks extension](https://tasks.extensions.modelcontextprotocol.io/) supports work that takes too long to finish in a single immediate response. A client can receive a task handle, poll for its status, and retrieve the result when it is ready. This was already part of MCP's development before the conference; the keynote put it on my radar. For someone still learning how these systems fit together, having an explicit way to track unfinished work makes sense.

The [Skills extension](https://modelcontextprotocol.io/extensions/skills/overview) interested me for a more personal reason. MCP servers can expose reusable workflow instructions and supporting files, which clients discover and read through MCP. Having spent time putting instructions into a Claude Code plugin, I wanted to understand how that work could travel between tools. The specification exists, though SDK and host support are still being implemented, so I would check a client's support before assuming it all works together.

I also enjoyed the live demo of [Buzz](https://github.com/block/buzz), Block's open-source workspace for humans and agents to collaborate. The program included Bradley Axen's keynote, [“Building the Human-Agent Workplace”](https://events.linuxfoundation.org/agntcon-mcpcon-north-america/program/schedule/?id=1288826), along with dedicated Buzz sessions. Seeing a working application helped ground a morning otherwise heavy on discussion about agents.

Then I entered the Solutions Showcase and more or less surrendered the rest of my available time to it. The sponsor area felt larger than the one I remembered from Open Source Summit North America in Minneapolis. That is a personal impression, not a floor-plan measurement, but it certainly contained enough booths to derail my plans.

I talked with almost every sponsor and neglected the other talks and poster sessions I had meant to attend. There was always another demo to inspect or another conversation to finish. Useful conversations, admittedly, but the sessions continued without me.

### Turning myself in

Somewhere amid the booth visits, I entered PointFive's [AI's Most Wanted contest](https://events.linuxfoundation.org/agntcon-mcpcon-north-america/program/schedule/?id=1361453). My [confession](https://lnkd.in/p/eyDCKmTr) concerned a request to add compiler sanitizer support in CI. The agent produced large patches touching more than 30 crate dependencies for instrumentation and rebuilt Rust's standard library from source.

That is quite a diff to receive from a request that fits in one sentence. It also gave me a suitable confession for a conference about agents. I still have plenty to learn about setting scope and reviewing what comes back, especially when the work reaches into dependencies and build infrastructure.

### My turn to present

I did manage to leave the booths for my own talk: [“Anatomy of a Claude Code Plugin, and Lessons Learned on Creating One”](https://events.linuxfoundation.org/agntcon-mcpcon-north-america/program/schedule/?id=1246201).

The subject was the [Rust Extension Review Toolkit](https://github.com/clin1234/rust-ext-review-toolkit), a Claude Code plugin I co-developed for reviewing Rust-based Python extensions using PyO3. I started without prior experience building Claude Code plugins, which gave me plenty of material for the “lessons learned” part of the title.

The project combines review instructions, specialized agents, scripts, and reference material. Its checks can help identify areas worth investigating, but a candidate finding still needs judgment. A parser cannot tell the whole story about a Rust program, particularly when macros and type information matter. Documentation and testing against actual extensions matter too; an impressive-looking review is of limited use if its recommendations do not hold up against the code.

Presenting this work gave me a way to contribute while still being new to much of the surrounding ecosystem. I could talk about a specific thing I had helped build, including its limits, and leave the grand predictions about the future of agents to somebody else.

Afterward, I returned to the booths for the raffles and won precisely nothing. The evening continued at Poppy & Claro with more conversation and indulgence. My [first-day notes](https://lnkd.in/p/eQqPu5aK) capture the mixture of technical curiosity and questionable time management fairly well.

### Day 2: I apparently learned nothing about scheduling

On Friday, the Solutions Showcase drew me back in. I spent the most time visiting TrueFoundry, Arm, Block, CData Software, Okta, Fly.io, and Runlayer. Between established companies and startups, there was enough to examine that I again missed the technical sessions I had been looking forward to.

I regret that part. Governance, orchestration, agentic workflows, and further MCP work were all on my list, and I cannot give an account of talks I did not attend. Next time, I need to pick a few sessions in advance and actually leave the booths when they start.

Still, I enjoyed asking questions and seeing what each company had built. I am early enough in this area that even figuring out what to ask takes some effort. The conversations left me with plenty to investigate after the conference.

My raffle fortunes also improved: I won a Lego set. After Thursday's results, I will take it. By the time I wrote [my second-day update](https://lnkd.in/p/egZqNdjx), I was still a little bedazzled by how much there had been to see.

### Until next time

I left AGNTCon + MCPCon excited to keep building, with a clearer sense of how much I still need to learn. As a newcomer, I hope I can help make this ecosystem easier for the next person to approach, whether through a useful plugin, better documentation, or an honest account of what did and did not work. I would like to return with better questions, a more disciplined conference schedule, and another piece of agentic development worth presenting. Thanks to The Linux Foundation, the Agentic AI Foundation, and everyone who organized the event or took the time to talk with me. There is a lot here I want to understand, and I am looking forward to getting my hands back into the code.

## My first BazelCon: build graphs, bad Wi-Fi, and stolen cards

I arrived in Amsterdam for [BazelCon 2026](https://events.linuxfoundation.org/bazelcon/) with plenty to learn about Bazel. Then I got robbed on the metro the day before the conference. Without my cards, I couldn't pay for my reservation at Bastion Amstel, so I ended up using a virtual card to book a night in a hostel. Not the introduction to Amsterdam I'd hoped for.

Fortunately, the next three days gave me much better things to think about.

### Day 1: learning by breaking things

The training day began with a change of plan. The instructor for [Build Without the Bytes: High-Velocity Image Composition at Scale](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1292480) didn't arrive, and our session became a series of breakout discussions about using Bazel. It was an improvised start to a day that would include quite a bit of improvisation.

Antonio Di Stefano and Yannic Bonenberger's [Advanced Bazel: Rules Authoring, Performance Tuning and Remote Execution](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1293066) gave me plenty to work through. The [workshop repository](https://github.com/EngFlow-Academy/bazelcon-2026-advanced-bazel-workshop) includes exercises on test sharding, validation actions, and tree artifacts. We also had an unscheduled exercise in patience: downloading Bazel over congested conference Wi-Fi. Occasional differences between the live presentation and the repository kept us on our toes, too. The presenters stayed cheerful even as time ran out.

The mutation-testing example helped several ideas click for me. Putting every mutation into one test action means running them sequentially on one worker, with coarse caching. Splitting the work into separate actions gives Bazel more opportunities to parallelize and reuse results. The special `\_validation` output group makes those checks part of the build without requiring users to request a custom output group explicitly. The [workshop slides](https://github.com/EngFlow-Academy/bazelcon-2026-advanced-bazel-workshop/blob/main/slides/build_deck.py) walk through that progression.

Tree artifacts were another useful discovery: directory outputs whose contents may only become known during execution. [`ctx.actions.map\_directory`](https://bazel.build/rules/lib/builtins/actions#map_directory) lets a rule create actions based on the files in those directories once they are available. In this exercise, that meant generating separate patching and checking actions for the discovered mutations. I could finally see how a build graph could accommodate work whose exact shape wasn't known upfront.

Jason Bedard's afternoon workshop changed, too. The [schedule](https://events.linuxfoundation.org/bazelcon/program/schedule/) lists [Build File Generation Using AXL](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1361063) as the replacement for [Extending Bazel with Starlark: Custom Commands and Code Generation](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1293142). We explored [Aspect Gazelle](https://github.com/aspect-build/aspect-gazelle), including its prebuilt runner. Avoiding a local build of Gazelle and its transitive toolchains sounded especially appealing after the morning's downloads.

The Jest example made BUILD-file generation feel approachable: an extension could add or remove test targets as the source tree changed. Lazy indexing and restricting regeneration to selected directories also caught my attention. These may be familiar ideas to experienced Gazelle users, but I was seeing them for the first time.

[Orion](https://github.com/aspect-build/aspect-gazelle/tree/main/language/orion) lets you write those generator extensions in Starlark through AXL, instead of implementing them in Go. Its callbacks divide the work into stages: `prepare` identifies sources and queries, while `declare` uses the results to define targets. That's a distinction I had to straighten out in my notes: we're writing the generator in Starlark, not inventing a replacement language for BUILD files. The session eventually became a group brainstorming discussion, which suited the improvised format.

Jorge Acosta and Ricard Sole Casas closed my training day with [How Fast Should/Can My Build Be? A Journey to Understand Build Optimization](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1293145). Their [maze project](https://github.com/Giorgiux/bazelcon-maze) uses a small browser game and its build graph as an optimization exercise. It made the limits of throwing more compute at a problem quite tangible. A long chain of dependent actions still has to run in order; adding workers won't shorten that chain. Local development and CI also have different starting conditions, so the same optimization won't necessarily help both.

We looked at whether execution or overhead dominated a build, and at tools for finding where the time went. The presenters' enthusiasm for [`--disk\_cache`](https://bazel.build/remote/caching#disk-cache) was infectious. Reusing action outputs across local builds sounds rather magical when you're new to it. I also discovered that Bazel's [JSON trace profiles](https://bazel.build/advanced/performance/json-trace-profile) can be opened in [Perfetto](https://ui.perfetto.dev/). Meanwhile, the Wi-Fi was still making its own contribution to our wall-clock measurements.

### Day 2: more acronyms, fewer possessions

Some good news: I filed a police report and received a written response to help with replacing my stolen ID and cards. A small consolation, but a useful one.

The main conference brought community updates, sponsor booths, and discussion of agentic development workflows. Bazel 10 was also on the agenda, with [10.0.0rc1 already released before the conference](https://github.com/bazelbuild/bazel/releases). Between the talks and conversations, my list of unfamiliar projects kept growing.

Mattias Jansson's [One Content-Addressed Store, Zero Full Clones: Backing Bazel's Cache and Remote Execution with Lore](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1270075) introduced me to [Lore](https://github.com/EpicGames/lore), Epic Games' content-addressed version-control system. The talk explored using one store for source data and build artifacts, with workers fetching inputs as needed. I'd initially scribbled down something like "Git plus a build cache," but Lore is its own version-control system. Sharing storage across those uses was the idea that interested me.

Tyler French and Benjamin Ingberg's [Content-Defined Chunking for Bazel](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1224147) approached reuse at a smaller scale. [Content-defined chunking](https://www.buildbuddy.io/blog/content-defined-chunking/) splits large files into chunks whose boundaries depend on their contents. Matching chunks can be reused, so a slightly changed binary needn't be uploaded or downloaded in full. This is chunk reuse, rather than storing a byte-by-byte diff against an earlier object file. The potential reduction in network traffic made immediate sense, especially after the previous day's downloads.

Tamir Duberstein's [Type-checking Starlark without waiting for Bazel](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1263217) answered a question I'd been wondering about: if Starlark looks so much like Python, why can't we simply point a Python type checker at it? Starlark has its own semantics, and Bazel adds constructs that Python tooling doesn't understand out of the box. His experimental checker, [`sty`](https://github.com/tamird/sty), builds on Starpls and uses `ty` for type analysis. I liked the prospect of getting feedback in an editor while the wider ecosystem works through annotation support and compatibility.

[Persistent Test Runners](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1266475), by John Cater and Antonio Di Stefano, covered the repeated attempts to avoid paying test-process startup costs for every run. Keeping a JVM or other expensive test environment alive sounds straightforward until different test rules and lifecycle requirements enter the picture. My notes include a preview provider and proposed Java lifecycle hooks; I came away treating those as work in progress, rather than APIs I could assume were available everywhere.

By evening, I'd reached my limit for dense technical explanations. I had more drinks than planned, along with some small bites, then headed to Social Impact Factory for impromptu karaoke and giant Parcheesi. More conversation followed at Venturo Skylounge. My notes from that part of the day are considerably less technical.

### Day 3: toolchains, packages, and configurations

The final morning went straight into technical talks. David Zbarsky's subjects seemed particularly well matched to my interests in C and toolchains.

He and Corentin Kerisit presented [Lessons learned building a zero-sysroot fully hermetic LLVM toolchain for Bazel](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1261770). Their [Hermetic LLVM project](https://github.com/hermeticbuild/hermetic-llvm) builds target-specific runtime components from source and makes them explicit parts of the build. That includes components normally supplied through a target sysroot, such as C libraries and compiler runtimes. Seeing cross-compilation and linking modeled this way gave me a much more concrete understanding of hermetic toolchains.

Zbarsky followed with [rules\_rs: {Fast, Hermetic, Ergonomic} - Pick 3](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1245581). [`rules\_rs`](https://github.com/hermeticbuild/rules_rs) builds on `rules\_rust`, with Cargo integration and toolchains for cross-platform builds. Its use of Cargo's lockfile directly, without another Bazel-specific Cargo lockfile, appealed to me. Keeping two build systems synchronized already sounds like enough work.

Armando Montanez and Ulf Adams' [Proving Equivalence in any2bazel Build System Migrations](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1268437) caught my attention as soon as the CMake File API appeared. [any2bazel](https://github.com/EngFlow/any2bazel) compares what the original build and the Bazel build actually compile and link. An LLM can generate or revise BUILD files, while a deterministic comparison exposes differences and guides the next attempt. The documented paths include CMake and Maven. Its checks have a defined scope, so I wouldn't read "equivalence" as proof that every possible build behavior is identical, but it gives a migration something concrete to test against.

[No bytes left untracked - Bazel Supply Chain Security](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1254769), by Antonio Di Stefano and Yannic Bonenberger, introduced work on collecting dependency metadata and producing software bills of materials. The [`package\_metadata` framework](https://github.com/bazel-contrib/supply-chain) supports gathering package information and applying organization-specific checks. I was glad to see people working on making that information available from the build itself. An SBOM won't prevent every supply-chain attack, but knowing what went into an artifact is a useful starting point.

Reid McKenzie's [Let the Package Manager Decide](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1272892) brought us into Python packaging. The walkthrough of installation behavior and wheel filenames helped me follow the discussion of [`rules\_py`](https://github.com/aspect-build/rules_py) and its `uv` integration. Using lockfile information to configure dependencies, while representing source builds as Bazel actions, offers more control over how third-party packages are built. It also made me appreciate how much work is hidden behind a seemingly simple package installation.

Scott Cao's [One Build, Many Configurations: Comparing Configuration Features in Bazel and Buck2](https://events.linuxfoundation.org/bazelcon/program/schedule/?id=1272973) addressed another problem I could easily imagine growing out of hand: building the same code for different platforms, optimization levels, and sanitizers without multiplying unnecessary work. Bazel's flagsets and Buck2's configuration modifiers offer ways to make those choices easier to manage. The [Buck2 modifier design](https://buck2.build/docs/rfcs/implemented/modifiers/) also clarified a detail in my notes: it recommends modifiers for library defaults; it doesn't establish a blanket ban on transitions for libraries. Modifiers can set or replace a constraint when constructing a top-level target's configuration, letting a choice such as ASan compose with other settings.

### What I'm taking home

Hermeticity was the theme I kept hearing: make the build's inputs explicit, control the environment, and give other people a fair chance of reproducing the result. I'm still a Bazel newcomer, and plenty of these talks left me with questions I'll need to answer by trying things myself. That's part of why I'm excited to keep going. The workshops gave me repositories to revisit, and the conversations made contributing feel less intimidating. I hope I can help improve Bazel's ecosystem as I learn, perhaps by documenting a confusing setup step or turning a toolchain problem into a small, reproducible bug report and eventually a patch. I'd love to return to a future BazelCon with something useful to share, even if it's a modest fix that saves the next newcomer an afternoon.


## CppCon 2026: Tying Up Loose Threads

My 1st time attending CppCon.

That sentence still feels a bit strange to write.

I had watched CppCon talks, illuminating talks whose names also authored in-depth blog posts, and nurtured and taught a generation on YouTube. All C++ projects, prominent and hobbyist, that somehow end up teaching you more than you realized.

And then, suddenly, I was in Denver.

Not watching CppCon.

Actually attending it.

And, slightly more surreal still, I was also there to give a talk.

### There Are Too Many C++ Talks

My first discovery was that attending CppCon's main talks is not quite the same thing as watching them on YouTube.

You look at the schedule and see a talk about branch prediction. Another about memory. Another about benchmarking. Another about C++26. Another about reflection. Another that sounds so interesting that you immediately want to clone yourself.

Marco Barbone joked about the obvious solution: `fork()` yourself and attend all the parallel tracks. He did not, in fact, recommend this particular conference optimization.

Funnily enough, Matt Godbolt described spending more time than ever in the "hallway track": the unofficial track where instead of sitting down for a presentation, you end up standing around talking to interesting people. His reasoning was difficult to argue with: the talks will eventually appear online, but the experience of conversing within the hallway is much harder to reproduce later.

I quickly discovered why.

There is something wonderful about seeing a name you've previously encountered only on a screen and then realizing that the person is just... there.

Walking around.

Getting coffee.

Talking about C++.

Being a person, instead of being imagined as an "iterant sage" (I'll explain the term in due time).

That was one of the strangest and nicest parts of the week.

### The Hallway Track Is Real

James Lim described CppCon as being densely populated with talent, passion, and warmth. He also mentioned an elevator ride that turned into a conversation about one of his projects and new ideas for it.

That sounds almost too convenient until you experience it yourself.

There's no need to induce networking opportunities at a conference like this. People already have something they want to talk about.

A talk just finished? Talk about it.

Someone has a project you recognize? Ask about it.

You're both standing in the same hallway? Apparently that's enough.

Vishnu Gopinath had a similar observation: CppCon is much more than its talks. It is the people, the random hallway discussions, the ideas you pick up from someone you have just met, and the slightly unreasonable amount of C++ that everyone seems perfectly happy to discuss.

I think that last part may be the official theme of the conference: there is simply an extraordinary amount of C++.

### And Then There Was the Mountain

The conference was held at Gaylord Rockies, with the Rocky Mountains providing a slightly unreasonable backdrop for a conference about compilers, caches, allocators, and undefined behavior.

Sandor Dargo's trip report captured some of that contrast nicely: spacious surroundings, the mountains outside, and the opportunity to explore Denver between conference activities. He visited the Forney Museum of Transportation and the Clyfford Still Museum, despite not usually being particularly interested in modern art.

It made the whole thing feel slightly unreal.

In the best possible way.

### The Moment CppCon Stopped Being a List of Talks

At some point, the conference stopped being a schedule.

It became a collection of questions (and I did ask plenty), such as:

* How much does an abstraction really cost?
* What does the CPU actually do?
* Where is the data?
* How do you benchmark something without disturbing the thing you're measuring?
* What happens when you want to update a running binary?
* What does C++26 make possible?
* How far can reflection go?
* What happens when AI writes the code?
* Can the language continue to thrive within WG21?

And, for me:

**What happens when Python no longer has the GIL?**

### Tying Up Loose Threads

My talk was [Tying Up Loose Threads: Making Your Project No-GIL Ready](https://cppcon2026.sched.com/event/2RT6m/tying-up-loose-threads-making-your-project-no-gil-ready).

The basic idea was that removing the GIL is not simply ripping out one giant lock: CPython's free-threaded build changes the allocator, reference counting, container synchronization, and C API, exposing assumptions that extension code may previously have relied on implicitly.

The deeper I looked, the more surprising those changes became. The free-threaded build uses mimalloc with delayed reclamation and quiescent-state mechanisms, while reference counting gains separate local and shared state so that different threads can participate safely. Containers and borrowed references bring another set of concurrency concerns: operations that once looked harmless can require explicit synchronization, and a borrowed reference no longer carries the same implicit protection when another thread can modify its container.

Fortunately, the ecosystem already provides practical migration paths. `pybind11` and PyO3 can declare GIL-independent modules; global state can move toward thread-local storage; Cython and module initialization have free-threading support; and CI can build against Python 3.14t, disable the GIL, and use ThreadSanitizer and AddressSanitizer to uncover the bugs hidden by the old assumptions.

Slides: https://github.com/CppCon/CppCon2026/blob/main/Presentations/Tying_Up_Loose_Threads.pptx

### Meanwhile, C++ Was Busy Being C++

Of course, I did not come to CppCon only to talk about Python's interop capabilities with C++. There were talks about branch prediction, object residency, benchmarking, practical algorithms, memory systems, and C++26.

Roman Bansal highlighted another cluster of ideas particularly well: memory as performance, increasingly explicit control over caches and RAM, measuring performance without distorting the measurement, and techniques for updating running binaries without restarting them.

As I continued to listen on his talk, I found myself repeatedly coming back to the same thought: 

> Higher-level abstractions can improve clarity and maintainability, but some abstraction techniques really do introduce runtime costs. The important thing is not to reject abstraction reflexively, but to understand where the costs matter and where they do not.

That felt surprisingly connected to the no-GIL work, as in both cases, the interesting engineering questions start when you stop accepting the surface-level justifications.

Oh, and during one [particular keynote session](https://youtu.be/41USGJaGsAo), the Q&A session got spicy 🌶️. John Lakos grilled Stroustrup on why [contracts](https://en.cppreference.com/cpp/language/contracts) and profiles could not be merged together in C++26, claiming that they can coexist. He also compared this watershed moment to C++11's formalization of the memory model and barring copy-on-write strings, and subsequent ABI breakages. His Qs touched on the following:

1. Difference between erroneous behavior (defined in standard) and profiles defining UB: Stroustrup stated that erroneous behavior removes a major source of UB, but also error-prone and implementation-defined, so can be sidestepped with the initialization profile
2. How Profiles handle integer overflow, comparison to prior approaches (saturation add and wrap around), and frustrating breakages and incompatbilties due to redefining UB as intended behavior: Stroustrup made a cop-out, claiming he authored a paper touching on this issue, but needed another year to elaborate.

BTW, my remark on MSVC not supporting profiles, with him implying absolute focus on AI above C++26 features elicited much laughter. 😁

### Then Someone Made a Duck

One of the most delightful moments of the conference was Ryan Keane's work with C++26 reflection. Sidenote: I'll still affectionately call him "the Renassler whiz kid with the yee-ass haircut".

His `rjk::duck` library explores how unrelated types can participate in a common interface using reflection, and his talk on synthesizing VTables with C++26 reflection earned a standing ovation. He also won Best Poster for the project.

I love moments like that at conferences.

You see something as marvelous and ingenious as thus, and your first reaction shifts from:

> "I should probably read the paper."

to:

> "Wait. You can do that?"

That happened more than once during the week.

Sometimes the exciting thing was a language feature.

Sometimes it was a memory-management technique.

Sometimes it was an absurdly fast emulator.

Sometimes it was a clever benchmark.

And sometimes it was simply watching someone explain a problem they had clearly spent a ridiculous amount of time thinking about. Seriously, check out [his write-up](https://ryanjk5.github.io/posts/rjk-duck/).

### Dozens of Talks. One Me.

Another maxim that afflicts every technical conference attendee: you won't see and hear everything.

There were talks about benchmarking, memory hierarchies from caches through NUMA and CXL, Python JITs, language panels, and lightning talks: all the while the hallway track was humming along.

A 6000 FPS Game Boy emulator, a closing systems-engineering talk, posters, sponsor events, and countless conversations were all competing for the same finite amount of time.

And that brought me back to one of the strangest feelings of being there for the first time.

### The Slightly Terrifying Part: Giving the Talk

Preparing the slides was one thing.

Seeing the talk on the actual conference schedule was another.

Suddenly the title was no longer something in my presentation file.

The dread was real: the room that I presented could seat roughly 40 peeps at best, and it was only slightly over half-full.

They could ask probing questions, disagree, or could have already studied the CPython implementation much more than I had.

Admittedly, I wasn't able to answer all of the attendees' questions in a satisfactory way. However, the payoff of enlightening the avidly-curious listeners was still worth the jitters.

### Tying Up Loose Threads

The no-GIL project currently has plenty of momentum. The slides I presented noted that 61% of the most popular PyPI wheels were reported as free-threaded compatible, alongside the growing collection of Python documentation and tooling for supporting free-threaded extensions.

But the most useful lesson for me was not a percentage.

It was a way of thinking. I think these maxims encapsulate the gist of all the wonderful talks presented at this year's CppCon:

* When an old assumption disappears, find everything that depended on it.
* When an abstraction hides something important, learn what is underneath.
* When a benchmark says something surprising, investigate the measurement.
* When an AI gives you code, ask it questions.
* When a conference presents six fascinating talks at once, accept that you are only one human being.
* When you meet someone whose work you've admired from afar, say hello.

You never know where the conversation will go.

### Just Before Leaving Denver

Normally, I would have spent my last night at Gaylord Rockies lounging around its numerous (and expensive) restaurants and finishing my other projects. However, an auspicious moment arrived when Jon Kalb, the convenor of the entire conference, permitted me to attend Fidor Pikus' 2-day class on C++'s parallel execution policies, thread safetiness, atomics, C++ memory ordering, how to prevent false sharing, and designing lock-free concurrent data structures. Normally attending required paying a very huge registration free, so I am still grateful for being able to hear from the greybeard himself for free!

PS: "iterant sage"

> During lightning talks, among their attendees were none other than Jason Turner (C++ Weekly) and  Matt Godbolt (Compiler Explorer). I could contain my excitement of meeting these two luminaries (among many others) of the C++ community. The former brought up wanting to pack up and move elsewhere; I joked that doing so befits calling them "iterant sages," who dispense invaluable C++ techniques across cities in exchange for room and board.

Last modified 9/29/2026

## 1st week of using Claude Pro

Thanks to the generosity of the organizers of PyTexas 2026, I won a 3-month Claude Pro subscription as a prize!

![Proof](https://github.com/user-attachments/assets/a689768f-24d0-4f1c-836a-568ed3f6cdbd)

After I installed the Claude Code CLI and began prompting, I realized that the 5-hour and weekly limits were
(compared to my previous usage of Claude solely within its web UI) basically unlimited.

[1st attempt here.](https://claude.ai/share/783b6ec3-0fb8-4a1f-a2c1-6fac6597074d)

As one can see by the above conversation, my first experience with Claude was adding no-GIL support for 
[`pywin32`](https://github.com/mhammond/pywin32/pull/2757), which went nowhere. (How I finally resolved it
will be mentioned later.)

So like any developer when given basically-unlimited LLM credits, I embraced ~~vibecoding~~ AI-assisted development
with human review. And boy, was my producitivty supercharged when paired with some awesome plugins.

### My environment with Claude

With Claude Code, I have these plugins installed:

* [devdanzin/cpython-review-toolkit](https://github.com/devdanzin/cpython-review-toolkit): CPython C code exploration and analysis agents
* [devdanzin/cext-review-toolkit](https://github.com/devdanzin/cext-review-toolkit): CPython C/C++ extension analysis agents
* [devdanzin/cpython-review-toolkit](https://github.com/devdanzin/cpython-review-toolkit): Code exploration and analysis agents for C code with the Python repo
* [devdanzin/ft-review-toolkit](https://github.com/devdanzin/ft-review-toolkit): Free-threading migration toolkit for CPython C extensions
* [clin1234/rust-ext-review-toolkit](https://github.com/clin1234/rust-ext-review-toolkit): Analysis agents for Python extensions written in Rust with PyO3 ***MAINTAINED BY YOURS TRULY***
* [devdanzin/code-review-toolkit](https://github.com/devdanzin/code-review-toolkit): General purpose codebase exploration and analysis agents
* [Gentleman-Programming/engram](https://github.com/Gentleman-Programming/engram): Persistent memory for AI coding agents
* [getlantern/circumvention-corpus](https://getlantern/circumvention-corpus): MCP for structured-metadata corpus of censorship-circumvention research
* [context7](https://github.com/upstash/context7): MCP for fetching up-to-date programming documentation

### What I contributed

#### pywin32

Within a month, Claude turned my request for free-threaded Python interpreter support
[made all the way back in June 2024](https://github.com/mhammond/pywin32/issues/2303) and
my [list](https://github.com/mhammond/pywin32/pull/2683)
[of](https://github.com/mhammond/pywin32/pull/2686)
[PRs](https://github.com/mhammond/pywin32/pull/2687)
[starting](https://github.com/mhammond/pywin32/pull/2737)
[in](https://github.com/mhammond/pywin32/pull/2757)
[November](https://github.com/mhammond/pywin32/pull/2765)
[last](https://github.com/mhammond/pywin32/pull/2766)
[year](https://github.com/mhammond/pywin32/pull/2767).

Finally, merging [this PR](https://github.com/mhammond/pywin32/pull/2767) officially makes `pywin32` free-threaded compatible,
though only with experimental support. With Claude, it converted my stumbling block (with a 4-month hiatus within) into quite
an excellent rubber duck; by feeding in CI logs from failed runs, I was surprised on how Claude Code correctly provided
approaches in resolving the stumbling block. Artifacts generated by the CLI tool are available
[here](https://gist.github.com/clin1234/4e5a82de185ef5efff8f5770b33a5702).

An example:
<script src="https://gist.github.com/clin1234/4e5a82de185ef5efff8f5770b33a5702.js?file=ci-failure.md"></script>

#### Analyses on Python projects with native extensions

The main culprits of me burning through the 5-hour limit within the 1st hour: generating reports on popular Python projects
containing C, C++, Cython, or Rust code, including compatbility with the free-threaded interpreter

* [pyo3/Rust](https://gist.github.com/clin1234/abec57c6caee33942c76f5eb986c6dba)
* [C/C++/Cython](https://gist.github.com/clin1234/2469758160721f4f991110167017e4d3)
* [Free-threaded](https://gist.github.com/clin1234/6cdb5150ba3298576ca54fa07c017517)

An example:
<script src="https://gist.github.com/clin1234/6cdb5150ba3298576ca54fa07c017517.js?file=aiohttp.md"></script>

#### msgpack-python

In an interesting twist, posting Claude-generated analyses [as an issue](https://github.com/msgpack/msgpack-python/issues/683)
actually helped to automate bug fixes (see [here](https://github.com/msgpack/msgpack-python/pull/687) and 
[here](https://github.com/msgpack/msgpack-python/pull/686)).

#### veles-ng

My crown jewel and epitome of LLMs facilitating more managable rewrites of old codebases. For those unfamiliar,
[veles-ng](https://github.com/clin1234/veles) is my continuation of a very pretty-looking visualization tools
for structured binary files. With Claude Code, I was able to acccomplish the following in mere weeks:

* Increase the number of supported file formats from 8 to roughly double
* Fix occasional crashes inherited from the original codebase

### TLDR

Claude Code is a productivity supercharger, but don't blindly trust its output, even with Opus as the Advisor model
set to maximum thinking effort. Manual guiding is definitely needed, as LLM-generated commits don't always compile
the first time, and may get confused when running a command containing multiple subagents and when they suddenly
pause due to hitting the limits too often.

## My experience in the Linux Embedded Conference NA

Last modified 5/22/2026

Right after the Open Source Summit NA 2026, here's two more days of networking,
and interesting talks on a more focused field about Linux's security stack, BPF,
AppArmor, and more.
(no interesting swag from exhibitors, sorry :-(...  ). Again, best expressed through a series
of photographs that I took:

* [Day 1](https://postimg.cc/gallery/gxrdt2J)
* [Day 2](https://postimg.cc/gallery/XNFSkTk)

## My experience in the Open Source Summit NA and Embedded Linux Conference NA

Laat modified 5/20/2026

To summarize three days of networking, and interesting talks, and zany exhibitors, it's best 
to present them as a series of photographs:

* [Day 1](https://postimg.cc/gallery/XJfb44z)
* [Day 2](https://postimg.cc/gallery/C0S9x0H)
* [Day 3](https://postimg.cc/gallery/JHY3bvf)

(Of course I have the longest ribbon chain. Pretty sure I'm the only one that exhibits such behavior)

## My contributions to Python and its ecosystem
Posted 4/20/2026

Since 2024, I've contributed profusely to both the CPython interpreter and popular packages, mainly low-level building blocks of other popular packages.

By commits:

* [CPython](https://github.com/python/cpython/commits/main/?author=clin1234)
* [pyo3](https://github.com/PyO3/pyo3/commits/main/?author=clin1234)
* [python-zstandard](https://github.com/indygreg/python-zstandard/commits/main/?author=clin1234)
* [pywin32](https://github.com/mhammond/pywin32/commits/main/?author=clin1234)
* [greenlet](https://github.com/python-greenlet/greenlet/commits/master/?author=clin1234)
* [tach](https://github.com/tach-org/tach/commits/main/?author=clin1234)
* [macchina](https://github.com/Macchina-CLI/macchina/commits/main/?author=clin1234)

Taking together my contributions, they strengthen Python’s ecosystem in multiple layers: improving the interpreter itself, enhancing cross‑language integration via Rust, and improving
usefulness of key platform‑specific and concurrency libraries. That shows my focus on low‑level performance, systems integration, and developer tooling—areas that have broad impact across Python applications and libraries. In particular, free-threading is becoming popular among popular packages: as of this post, [over HALF of the 360 most downloaded packages](https://hugovk.dev/free-threaded-wheels/) support it!

TLDR for the very unfortunate souls not enlightened by my wonderful talk:

* Changes to the runtime: a garbage collector that doesn’t rely on linked lists, fine-grained internal locks on built-in `dict` / `set` / `list`, modified reference counting to reduce contention, and critical sections (PyBeginCriticalSection / PyEndCriticalSection) for per-object locking, useful for custom objects to be exposed via the C API. `PyDict_Next` is not thread-safe and must be wrapped in a critical section.

* Module initialization:
  - Single-phase: call `PyUnstable_Module_SetGIL` in the extension module’s entry point `PyInit_<module name>`:
```c
#ifdef Py_GIL_DISABLED
    PyUnstable_Module_SetGIL(m, Py_MOD_GIL_NOT_USED);
#endif
```
  - Multi-phase: add a `PyModuleDef_Slot` with `Py_mod_gil` set to `Py_MOD_GIL_NOT_USED`.
* Language and tool support: [Cython](https://cython.readthedocs.io/en/latest/src/userguide/freethreading.html) (type annotations for efficient, compatible code), PyBind11 ([free-threading support](https://pybind11.readthedocs.io/en/stable/advanced/misc.html#free-threading-support) , `PYBIND11_MODULE(..., m, py::mod_gil_not_used())`), PyO3 /Rust (since 0.28, [assumes Rust code is thread-safe](https://pyo3.rs/v0.28.3/free-threading.html?highlight=gil_used#supporting-free-threaded-python-with-pyo3) ; opt out with `#[pyo3::pymodule(gil_used = true)]`).

* Testing: environment variable `PYTHONMALLOC=debug` and `PYTHON_GIL=0`, [AddressSanitizer](https://clang.llvm.org/docs/AddressSanitizer.html) and [ThreadSanitizer](https://clang.llvm.org/docs/ThreadSanitizer.html). The [cpython-sanity](https://github.com/nascheme/cpython_sanity) project provides pre-built Docker images of CPython with ASan and TSan enabled. Build wheels targeting free-threaded Python using versions ending in T (e.g., 3.13.0T).

Additionally, I presented a [very informative talk at PyTexas 2026 on porting Python packages with compiled-extensions to be compatible without the GIL.](https://www.pytexas.org/2026/schedule/talks/#tying-up-loose-threads-making-your-project-no-gil-ready)

Inspired by [Bernat Gabor's writeup](https://bernat.tech/posts/pytexas-2026-recap/), with additional details. ~~(please notice me and my greatness)~~

I've met a great variety of storied attendees: corporate and freelance, seasoned and newly-graduated, conversing about a wide range of topics: technical and social, quotidian and eccentric, informative and argumentative. Special shoutout to [Bernat Gabor](https://bernat.tech), [Moshe Zadka](https://cobordism.com/), [Scott Irwin](https://fosstodon.org/@Nekokawaigari), [Al Sweigart](https://alsweigart.com/), [Tristan Lee](https://tristanl.ee/), [Jacob Coffee](https://scriptr.dev/), and [Mason Egger](https://mason.dev/).

## Another long overdue update
Posted 3/7/2024

Not much has changed, except I run Canary builds of Windows Insider (very few crashes, surprisingly) and fetch (stripped) debug symbols of MS projects (binaries included with Canary builds, Office, Visual Studio, etc). Currently, my cache is ~450GB.

One topic that piqued my interest over the last few months is related to symbol fetching. Specifically, I was fascinated by the following two articles (see [here](https://www.emergetools.com/blog/posts/symbolicating-swiftui-and-any-apple-framework-part-2) and [here](https://www.emergetools.com/blog/posts/symbolicating-swiftui-and-any-apple-framework)) on automatically fetching debug symbols matching all Apple frameworks from Apple's servers, not just frameworks that come bundled with symbol names. If I have some way to get developer access to a Mac computer, the [ETSymbolication repo](https://github.com/EmergeTools/ETSymbolication) would greatly aid debugging macOS and iOS apps and their crash logs.

Also, deploying GH Pages have become more painful. For some reason, changes on my pages do NOT automatically trigger a rebuild, so I am forced to write a GH Actions file to do this for me:
```
# File: .github/workflows/refresh.yml
name: Refresh

on: push

jobs:
  # Build job
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
      - name: Setup Pages
        id: pages
        uses: actions/configure-pages@v3
      - name: Build with Jekyll
        uses: actions/jekyll-build-pages@v1
        with:
          source: ./
          destination: ./_site
      - name: Upload artifact
        uses: actions/upload-pages-artifact@v2

  # Deployment job
  deploy:
    env:
      GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
    permissions:
      id-token: write
      pages: write
    environment:
      name: github-pages
      url: ${{steps.deployment.outputs.page_url}}
    runs-on: ubuntu-latest
    needs: build
    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v2
            
```

## Long overdue update
Posted on 6/26/2023

In the time since my last post, I replaced my main laptop from an Acer Aspire 5 with a Ryzen 4700U and integrated graphics with a Razer Blade 17
 containing a Core i7 12800H and discrete Nvidia RTX 3060 GPU.

 Other than that, I spent my copious amounts of time lurking (too often) blogs that piqued my interest. I'm generous enough to release my list
  here: https://ufile.io/1fqpnqsx. All you need is to import this OPML file into a supported news aggregator. This'll expire in 30 days.

## Making the Steam Linux client use system libs on (OpenSUSE)
Posted on 4/09/2023.

Work in progress...

By invoking

`pushd ~/.steam/root/ubuntu12_32; file * | grep ELF | cut -d: -f1 | LD_LIBRARY_PATH=. xargs ldd  | grep  "=>"|awk -F "=>" '{print $1}'|sort | uniq; popd`
, the following libraries from my system that correspond to those from the Steam runtime are [here](stear32.txt). First-party libraries are `lib`

(Abbreviated) output of `rpm -q --requires steam`, which is the installer, **NOT** the Steam runtime used for the games themselves:
```
...
dbus-1-glib-32bit
fontconfig-32bit
glibc-32bit
glibc-locale-base-32bit
gtk2-engine-oxygen-32bit
libICE6-32bit
libSDL-1_2-0-32bit
libSM6-32bit
libX11-6-32bit
libXdmcp6-32bit
libXext6-32bit
libXfixes3-32bit
libXi6-32bit
libXrandr2-32bit
libXrender1-32bit
libXtst6-32bit
libatk-1_0-0-32bit
libcairo2-32bit
libcrypt1-32bit
libcups2-32bit
libcurl4-32bit
libdbus-1-3-32bit
libdrm2-32bit
libfreetype6-32bit
libgcc_s1-32bit
libgcrypt20-32bit
libgdk_pixbuf-2_0-0-32bit
libglib-2_0-0-32bit
libgmodule-2_0-0-32bit
libgobject-2_0-0-32bit
libgtk-2_0-0-32bit
libogg0-32bit
libopenal1-32bit
libopenssl1_0_0-steam
libopenssl1_0_0-steam-32bit
libpango-1_0-0-32bit
libpipewire-0_3-0-32bit
libpixman-1-0-32bit
libpng12-0-32bit
libpulse0-32bit
libstdc++6-32bit
libtheora0-32bit
libudev1-32bit
libusb-1_0-0-32bit
libva-drm2-32bit
libva-glx2-32bit
libva-x11-2-32bit
libva2-32bit
libvdpau1-32bit
libvorbis0-32bit
libvulkan1-32bit
libxcb-dri2-0-32bit
libxcb-glx0-32bit
...
```

Now, onto to writing a spec file.

The latest

Anywhere, here's the link: https://software.opensuse.org/package/steam.

## My experience at Vanderbilt
Posted on 8/08/2022.

### TODO:
For some reason I can't scale down images yet to fit with this article. Mainly because
the images I took were in the HEIC format (see [here](https://en.wikipedia.org/wiki/High_Efficiency_Image_File_Format#Support)),
and current web browsers don't support it natively, at least on Linux.

## The impact of my internship experience

To sum up in one word: *Wonderous*. Not only did I relish in collaborating with a graduate student who have published numerous papers on the field of computer-enhanced vision, but also indulged in engaging with both the academic and social summer-time atmosphere found within the university, including gazing at the Central Library, shown below:

## Would I have pursued this internship without external funding?

Without the funding, I would have not pursued it, or any other internship not within
driving distance from Central Florida. One major disincentive that the Gateway Fellows program
dispeled was my transportation and lodging costs, both to arrive at Nashville, and the
quotidian driving in the city.

And before you ask, I chose to lodge at a hotel some distance away from the city center,
mainly because of (perhaps apocryphal) concerns about abnormally high rowdiness during
nights. That choice was not cheap: the total price for my nearly 2 month stay totaled close
to ~$3,200.

## Lessons learned

* Unity's AR/VR plug-in is rather fickle to manage, at least initially. Hopefully later
Unity releases improve this
* Ethical considerations for testing volunteers on virtual environments don't surprisingly
differ too significantly from studies in the hard sciences
* Internet speeds provided by anywhere else, including fast-food restaurants, public libraries,
and the university, feel relieving compared to both the hotel's Wi-Fi and my "ultrafast"
5G mobile Internet.

## Examples of growth

* Learned how to create and test AR environments in Unity
* With the supervisor's encouragement, I went through Google Scholars to read on not
only her papers, but also those published by other eminent researchers on both augmented
reality and computer-enhanced vision.

## Future plans

After graduation in December, I intend to pursue full-time employment at niche, yet
intriguing tech companies in specialized fields. Possible candidates include fintech (JPMorgan & Chase, Bloomberg), and quant-based (Two Sigma).
