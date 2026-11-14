# James Gibson

**I make claims checkable.**

Every system I have observed appears as if it fails the same way: one part goes missing, the
output stays plausible, and nobody notices. Energy reporting, deployment
pipelines, brokerage accounting, compliance limits, agent-facing services.
More than a decade, one failure shape.

Self-taught, community-raised. I care about four things and I can show my work
on all four: **user ease, software correctness, client joy, and environmental
sustainability.**

---

## Disciplines

No project attached to these. This is simply what I have done, repeatedly, for
a long time.

**Legacy rescue.** Six-thousand-line bootstrap files, a non-cascading stylesheet
retrofitted into a large Flex application, twelve production databases
collapsed into one. I take the thing nobody wants to touch and I do not break
it.

**Version control and provenance.** Moved teams from SVN to Git, and years
later ran source-of-truth-in-git deployments for a packaged application across
customer orgs — committed metadata, scripted deploy, and a fixture repo whose
only job was to test the build step itself. That was early 2016. The platform
announced the same idea as its own product that August.

**Dependency surgery.** Hundreds of nested git-in-git-in-git npm packages,
untangled. Then taught a junior to do it in weeks, and she is still surprised
about it years later.

**Federated GraphQL cluster design.** A federated graph is a set of contracts
pretending to be a schema. I design the seams: each service owns a subgraph and
declares what it claims — resolvers, routes, streams, RPC methods, crons,
transports — and what it presupposes, addressed so drift in the presupposed
surface breaks the build instead of the customer. The port is part of a
deployment's identity, not a deployment detail. I built this shape for a
multi-app NestJS cluster — main, admin, and auth apps mounting subsets of one
GraphQL surface over a shared Prisma schema, with a token guard that answers 423
rather than a plausible empty result — and I have watched what happens when the
seam is left to convention. See *the lint rule*, below.

**Language migration with an afterlife.** Rewrote a lending platform's backend
from Java to Node. Developers were still reading that codebase three to five
years later — which is the only code review that counts.

**Onboarding as engineering.** Took a team from about nine regular members to
twenty-one. Ramp-up is a system, not a vibe.

**Concurrent delivery inside a rigid process.** Six-week sprints with a new one
starting every four, several in flight, releasing into secure environments.
Overlap, not sequence. Continuous delivery with a waterfall wrapper, in 2012.

**Financial semantics.** GAAP → XBRL → IFRS taxonomy mappings, as an
undergraduate. A mapping error is not a bug, it is a misstatement.

---

## Values

**User ease is a correctness property.** NSGEM's stated end goal was to
"increase data credibility" and to be "easy to use"
([navy.mil](https://www.navy.mil/Press-Office/News-Stories/display-news/Article/2265327/from-the-shore-navy-installations-take-energy-initiatives-to-the-next-level/)).
The Energy Biggest Loser competition was scored on it, and a culinary
specialist was turning off monitors because the tool made the stakes legible to
him. If the person doing the work will not use it, the number does not matter.

**Correctness means the ledger closes.** I spent six hours walking an engineer
through commission-split tests, because thirds of a cent do not divide and
someone has to own the remainder. Today I write harnesses where reverting only
the bound arithmetic makes six of thirteen checks fail on purpose.

**Client joy.** Adoption is the deliverable. I have watched a tool with all the
right features sit at 23% and a humbler one reach 90% because someone did the
change management. I build for the second number.

**Environmental sustainability.** 62,000 billing statements mapped to
facility-level usage across every Navy installation, in multiple time zones,
feeding a competition that reduced actual kilowatt-hours. Today: 1,188 days of
solar production against weather, with snow separated from soiling, published
alongside what was excluded and what still narrows the population.

---

## Where it has been tested

**2012 — NSGEM, U.S. Navy (CNIC, worldwide installations).** Created by
Sandrine Schultz, energy program manager at Commander, Navy Installations
Command — the project I'm proudest of. Comprising over 62,000
facility billing statements to 30+ utility-level usage across multiple time zones, and
shipped the Data Quality Score that told the reader how much of each number to
believe. The Energy Biggest Loser competition was scored on it; the program won
the International Special Achievement Award, and the Navy credited CNIC for
standing out among more than 100,000 organizations.

**2014–2015 — `agrig8.in`**
Genomic sorting applied to warehouse pick routing: inspired in college by a
traveling salesman weighted by product density. Abandoned on purpose, because
I realized did not know enough discrete math to do it honestly. That reason is the artifact.

**2014–2016 — Geometri (acquired by Acuity Brands).** Built the prototype servers. The lead wanted data in RAM because it beat DynamoDB on reads. It did.
It also removed durability, which was the only axis that mattered.

**2016–2017 — Apto.** Source-driven deployment for a Salesforce managed
package, 2016. Also the year I learned that a commission engine can be
arithmetically perfect and still be wrong, because the hard part is not
computing the residue — it is assigning it.

**2017 — Flowhub.** Proposed the fix for purchase-limit looping before the
Sweet Leaf raid: hash the license details, verify the limit against a public
ledger. Enforcement without identification. Sweet Leaf lost 26 licenses and
three owners went to prison; their implicit defense was not that they did not know where
the flower went, it was that no-one from METRC had told them they were liable for treating sales like alcohol purchasing
looking. Also consolidated about a dozen production databases into one and
began the move off managed hosting onto Kubernetes.

**2016–2019 — infrastructure.** DesignOps by 2019; the chat-native deploy and
incident habits earlier than the vocabulary for them. Watched an etcd cluster
lose quorum to an expired certificate, where the monitoring lived inside the
thing it monitored and could not report its own death.  a rebuild
nobody had documented because the builder quit same-day — twelve hundred to
two thousand prototype deploys, brought back one at a time, while pre-scheduled
user testing slipped and 8 a.m. emergency calls with vendors like Rancher
became routine. The cost of undocumented systems is measured in the wages of
the people rebuilding them: repairs, delays, and the lost window, at a FortuneX
— an approximate seven to eleven million.

**2025–now — the lab.** Six Go services sharing one trust protocol: advertise
over mDNS, verify capability before granting a rung, refuse to display a peer
you cannot attest.

---

## 2019–2021 — The lint rule

At a company I joined in October 2019, a concession on one lint rule — a style
preference granted to one team because it was cheaper than the argument — became
the boundary case that split a division.

The rule was never about the rule. A shared lint config is the cheapest
federalism test a company ever runs: one file, every team's code, no product
surface to hide behind. If it cannot survive one concession, the schema will not
survive one either. The split did not happen because of a semicolon; it happened
because nobody could say where the rule stopped being style and started being a
contract, so the next argument was about who owned the seam.

Two teams left with two conventions, then two roadmaps, then two org charts. A
VP told a room of engineers it was fine, because I was going to fix it. I handed
in my notice that week and was gone by June 2021. I was not going to be the
person who absorbed the cost of an undecided boundary and called it a fix.

I was granted at $33 on 14 October 2019. The last time I looked, the share price
was $2 — a sixteenth of the grant. Marked honestly, with the option stack
counted, it was closer to a fiftieth. The market did not punish a lint rule. It
priced a company that could not decide who owned a seam.

---

## The last five years

Most of what I know about systems at scale I learned by trying to make one
generator honest. The working notes are public:
[lemon-x-files](https://github.com/gibsunas/lemon-x-files) is the
multi-transport generator corpus,
[lemon-extract](https://github.com/gibsunas/lemon-extract) is the cross-repo
introspection that came out of it. Neither is a portfolio piece; both are the
record of what broke.

- **A transport is a dimension, not a rewrite.** One surface spec, seven
  transports — REST, GraphQL, SSE, JSON-RPC, UDP, Socket.IO, OTLP — declared as
  modules in the same surface rather than forks. A generator that only writes a
  demo feature is hollow, and hollow is a state you can see.
- **Decomposition ends when every surface has exactly one owner.** A controller
  mounted on two apps with no routes is not a REST surface; a
  registered-but-inert service is not a service. Writing them down as out of
  scope is what makes the decomposition complete.
- **Identity is an address, not a name.** Specs presuppose each other by pinned
  address, so a rename is free and drift is loud.
- **A port is part of the identity.** The same note surface mounted on 3001 and
  3002 is a straddle. Treating the port as a family value makes it two frames of
  one signature instead of a fork.
- **Composition order is load-bearing.** The introspection plugins bootstrap
  sequentially because the init step creates the project list every later plugin
  reads. Concurrency there is a silent data-loss bug, not a speedup.
- **Read-only is the default, including when you cannot tell.** An unknown
  credential is a read-only credential. A stale ambient `GITHUB_TOKEN` turns a
  valid request into a 401 that reads like "not found," so the tool reads exactly
  one variable and never the ambient one.
- **The MCP surface is the security boundary.** Three read-only tools, no shell,
  no arbitrary path reader; scan, npm, and git are withheld because they mutate
  or execute. A smaller tool list is the entitlement.
- **Snapshot the schema like a lockfile.** A GraphQL schema, a
  `package-lock.json`, and a `yarn.lock` are all strings that describe what a
  deploy believed. Store them as extracts against a commit, and "what changed?"
  stops being an archaeology project.

---

## The rest of it

Not a portfolio. **Seeds** — bodies of knowledge with a stated audience, a
stated assumption, and one entrance. Take the door you came for.

- **[le.gume-energy](https://james-gibson.github.io/le.gume-energy/)** — solar
  production against weather, residuals separating snow from soiling.
- **[local-time](https://github.com/james-gibson/local-time)** — Cretaceous to
  now, in nanoseconds, two clocks per record, because local time lies once a
  year and does it quietly.
- **[lab-safety](https://github.com/james-gibson/lab-safety)** — safety data
  sheets for agent-facing surfaces; a priced call that cannot go unbilled.
- **[smoke-alarm](https://github.com/james-gibson/smoke-alarm)** — monitoring
  that lives outside the thing it watches.
- **[lezz.go](https://github.com/james-gibson/lezz.go)** — "42 is a coordinate,
  not a credential; trust is what you pinned."
- **[that-train-dashboard](https://github.com/james-gibson/that-train-dashboard)** —
  a child that cannot silently inherit its parent's rules.
- **[freematics-prototype](https://github.com/james-gibson/freematics-prototype)** —
  my car writes blog posts. Trusting the narrator is the hard part.
- **[lemon-x-files](https://github.com/gibsunas/lemon-x-files)** — one surface
  spec, seven transports, every gap written down.
- **[lemon-extract](https://github.com/gibsunas/lemon-extract)** — projects,
  commits, scans, and deployments across repos; a read-only MCP surface on top.
- **Old and load-bearing:**
  [lightning-bower-example](https://github.com/james-gibson/lightning-bower-example) ·
  [forceTooling](https://github.com/james-gibson/forceTooling) ·
  [resumeAPI](https://github.com/james-gibson/resumeAPI) ·
  [agrig8](https://github.com/james-gibson/agrig8)
