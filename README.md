> James is looking for work that doesn't feel like work.

**🕸️ [jamesgibson.co](https://jamesgibson.co)** · **🐙 [github.com/james-gibson](https://github.com/james-gibson)** · **🌱 [le.gume](https://james-gibson.github.io/le.gume/)**

<p align="center">
  <a href="https://github.com/james-gibson/le.gume"><img alt="le.gume stars" src="https://shieldcn.dev/github/stars/james-gibson/le.gume.svg?variant=secondary&size=sm" /></a>
  <a href="https://github.com/james-gibson/local-time"><img alt="local-time stars" src="https://shieldcn.dev/github/stars/james-gibson/local-time.svg?variant=secondary&size=sm" /></a>
  <a href="https://github.com/james-gibson/le.gume/blob/main/LICENSE"><img alt="AGPL-3.0" src="https://shieldcn.dev/github/license/james-gibson/le.gume.svg?variant=secondary&size=sm" /></a>
  <a href="https://github.com/james-gibson/le.gume"><img alt="le.gume last commit" src="https://shieldcn.dev/github/last-commit/james-gibson/le.gume.svg?variant=secondary&size=sm" /></a>
  <a href="https://github.com/james-gibson/lab-safety"><img alt="lab-safety last commit" src="https://shieldcn.dev/github/last-commit/james-gibson/lab-safety.svg?variant=secondary&size=sm" /></a>
</p>

---

## What James is building

### le.gume — the self-documenting documentation site

[le.gume](https://james-gibson.github.io/le.gume/) is a documentation site that is its own
starter kit: plain Markdown plus flat frontmatter, navigation derived from the file tree (so it
cannot drift), a publish guard that fails the build loudly instead of shipping stale docs, and a
generated `llms.txt` so an agent can take the site and go. It is promotional, educational, and an
open-knowledge starter at once — and it documents the rules it follows. Source:
[james-gibson/le.gume](https://github.com/james-gibson/le.gume).

The site is organised into **seeds** — each one a body of knowledge with an audience, an
assumption, and an entrance, arranged on a readiness scale rather than a seniority scale.

#### The seeds

| Seed | Readiness | Written for | Start here |
| --- | --- | --- | --- |
| [No script](https://james-gibson.github.io/le.gume/seeds/no-script/) | −3 · No script | Someone who wants the words, JavaScript off on purpose | [The page, script removed](https://james-gibson.github.io/le.gume/nojs/) |
| [No stylesheet](https://james-gibson.github.io/le.gume/seeds/no-stylesheet/) | −2 · No stylesheet | Someone who wants to read without the page's opinions | [The bare page](https://james-gibson.github.io/le.gume/bare/) |
| [It's just a file](https://james-gibson.github.io/le.gume/seeds/just-a-file/) | −1 · Just a file | Someone who wants the source, not a presentation of it | [The file](https://james-gibson.github.io/le.gume/seeds/just-a-file/) |
| [The commercial case](https://james-gibson.github.io/le.gume/seeds/pitch/) | 0 · Just a website | Whoever approves the time or the invoice | [Why le.gume](https://james-gibson.github.io/le.gume/pitch/why-legume/) |
| [The twelve factors](https://james-gibson.github.io/le.gume/seeds/twelve-factors/) | 1 · Understand | Someone who has never deployed software | [Start here](https://james-gibson.github.io/le.gume/factors/start-here/) |
| [Scenario as contract](https://james-gibson.github.io/le.gume/seeds/scenario-as-contract/) | 1 · Understand | Someone with a design doc, a schema, and no definition of done | [From design doc to scenarios](https://james-gibson.github.io/le.gume/guides/from-design-doc-to-scenarios/) |
| [The starter](https://james-gibson.github.io/le.gume/seeds/starter/) | 2 · Learn | An engineer who needs docs they can still run in two years | [Quickstart](https://james-gibson.github.io/le.gume/docs/quickstart/) |
| [Agent operations](https://james-gibson.github.io/le.gume/seeds/agent-operations/) | 3 · Operate | An LLM agent, or whoever points one at a repo | [Docs for agents](https://james-gibson.github.io/le.gume/docs/for-agents/) |
| [Isotopes](https://james-gibson.github.io/le.gume/seeds/isotopes/) | 4 · Package | Anyone who keeps re-explaining a setup | [What an isotope is](https://james-gibson.github.io/le.gume/isotopes/what-is-an-isotope/) |
| [The voice](https://james-gibson.github.io/le.gume/seeds/voice/) | Register · lateral | Writers and editors on technical material | [The hard parts](https://james-gibson.github.io/le.gume/writing/the-hard-parts/) |

### lab-safety — the policy layer for the prototype lab

[lab-safety](https://github.com/james-gibson/lab-safety) is the guardrail layer for a local-first
Go lab: a cluster of tools — `lezz.go`, `smoke-alarm`, `adhd`, `tuner`, `isotope`,
`fire-marshall` — that discover each other over mDNS and verify trust before acting.

The question it answers is **trust after connection**: a caller can connect to an MCP service, and
whether it should be trusted after that is a separate question most transport specs never answer.
lab-safety measures a caller's **42i distance** from nominal and maps it to a capability rung that
limits what it may read.

Its policy object is written down before its checks: one **16-section safety data sheet per MCP
surface**, laid out as Gherkin under [`sheets/`](https://github.com/james-gibson/lab-safety/tree/main/sheets).
A surface is not permissible until it is declared — and a surface that does not match its own
documentation is a failing test rather than a stale sentence.

### Documentation that derives itself

Across le.gume, the lab, and the open-knowledge vault, the recurring bet is the same:
**documentation should be a derived artefact, not a promise someone has to remember to keep.**

Simulations and research projects land as plain Markdown with flat frontmatter; navigation,
indexes, `llms.txt`, and cross-references are generated from the tree; a publish guard refuses to
ship anything that has drifted. A source file is the record, and the presentation is derived from
it — never typed twice.

- [local-time](https://github.com/james-gibson/local-time) — a TypeScript library that models
  temporal universes (films, historical events, simulations, books, biographies, legal timelines)
  with zero-reference addressing and cross-universe references, so a fictional world and a research
  timeline live in the same queryable model.
- [le.gume](https://james-gibson.github.io/le.gume/docs/for-agents/) — the engine: plain-text
  source, derived navigation, generated `llms.txt`, and a publish guard as the gate.
- [The open-knowledge vault](https://github.com/james-gibson/kb) — the corpus, indexed for search
  rather than left as loose notes.

---

## What James is up to lately

- `local-time-system` — (wip) a TypeScript library for managing temporal universes,
  cross-universe references, and temporal relationships. It tracks time across fictional and real
  works, with support for zero-reference addressing, temporal paradoxes, and complex reference
  chains.

<details>

```typescript
import { UniverseBuilder } from '@local-time/temporal-system';

const universe = new UniverseBuilder()
  .film('disney', 'mary_poppins', 1964)
  .withRuntime(139) // minutes
  .withRealityRelation('pure_fiction', 1.0)
  .withCopyright(['Walt Disney Productions'], 1964, 'active')
  .withCulturalSignificance(0.98)
  .addRuntimeKeyframe(87, 15, 'umbrella_descent', 0.95, ['iconic', 'magical'])
  .build();
```

```typescript
const universe = new UniverseBuilder()
  .historicalEvent('jfk_assassination', 1963)
  .withDateRange(1963, 11, 22, 1963, 11, 22, TimePrecision.SECOND)
  .withRealityRelation('documentary', 0.0)
  .withPublicDomain(['Warren Commission Report'])
  .addDateKeyframe(1963, 11, 22, 12, 30, 0, 'first_shot', 1.0, ['assassination'])
  .build();
```

```typescript
import { LocalTime } from '@local-time/temporal-system';

const localTime = new LocalTime();
await localTime.initialize();

const windowSearch = localTime.getWindowSearch();
const universes = await windowSearch.findUniversesInWindow('cal:1964');

const registry = localTime.getRegistry();
const maryPoppins = registry.getUniverse('disney:mary_poppins:1964');
```

</details>

- (mcp)
- `Project, Art?`
- (personal api)

## Work James tricked himself into doing

- Converting his homelab onto low-voltage hardware to maximise utilisation of local solar
  production.
- Created reverse proxies for his applications to minimise puncturing the home firewall and to
  centralise TLS management.
- The homelab supports multiple federated React apps backed by a shared Node.js API.

<details>

  - My car uses those APIs to write a diagnostic report for me

      <img width="553" height="1057" alt="image" src="https://github.com/user-attachments/assets/a9dd2121-141c-44ad-b030-804ade7a95f4" />

  - While exploring CQRS patterns, I load-tested the system by live-rendering random Markdown
    content from my webhook security-updates table, achieving 300–1k req/s.

      <img width="1705" height="628" alt="image" src="https://github.com/user-attachments/assets/66cff645-a456-49dc-bee5-6b6921c61992" />

</details>

- I use the lab to explore things like:
  - A personal GitHub application posting webhook security updates that I convert into test content
    for my Markdown exploration.
  - `Project, Art?` started as an exploration in rendering MDX into JSX securely using nonce or sha
    CSPs.
  - A personal MCP server connected directly to `Project, Art?` via a simple S-expression pattern.
    - LLMs speak Markdown, so this lets me repeatably create prompts and artifacts.
    - The native MDX support means custom web components can be used by the LLM.
    - Custom web components, in my understanding, are the next natural evolution of model response.
    - Advanced RAG indexing is currently planned for future research and implementation.
  - Custom application protocols and advanced data management via service workers.
  - OAuth 2.0 Dynamic Client Registration (RFC 7591) to support QR-code-addressed view adoption,
    with privacy in mind.
  - Combining HTTP 402 with HTTP 418 to build an intra-microservice payment middleware themed
    around cups of tea as units of measure.

## Things James has done

- Designed and led multiple technical code migrations with zero unscheduled hours of developer
  downtime.
- Stabilised core website delivery pipelines for multiple Fortune 500 companies.
  - I've battled Googlebot and Kubernetes — both winning and losing.
  - Un-recursed 1.3m npm modules while maintaining production shipping ability.
  - The generalised statement: 7 minutes to build, lint, and test; 7 minutes to ship.
    - It's not always possible, but the intention adds up to hundreds of saved developer hours.
- Supported active design-system implementation and automation.
  - Created scripts that calculated whether downstream repos were falling out of design compliance
    (mandated by accessibility legal requirements).
- Inherited eleven MongoDB instances and developed a solution to collapse them into a single
  database/API.
  - The system used the oplog for its Meteor.js integration; the number of active clients had led
    them to scale horizontally first.
- Successfully converted a traditional Salesforce copy-paste deployment cycle into a fast-paced
  GitOps pipeline that enabled a stronger developer experience.
  - This let the business focus on a mobile experience quickly while enabling custom-services income
    at the same time.
  - My work was directly compared to the best practices Salesforce advocated at the time —
    specifically, that my approach was much smoother (this was before Salesforce bought Heroku).
  - The company's Denver presence grew from three developers to over eighty team members across all
    areas of the business during my tenure as the second developer the founder hired full-time.
- Worked on a data-intensive dashboard supporting 60k individual building-energy reports to track
  progress against a Congressional mandate.
  - Data source ingested energy bills for the US Navy across 12+ timezones.
  - Data aggregated via ETL down to monthly usage for every individual building.
  - Data summarised from the individual building into a regional → global command view pane.

## Things James hasn't finished yet

- Automatic service healing with zero involvement via System swarm management configured by Magnet
  URL.
- Writing a Linux daemon to support an offsite backup service for critical application data.
- Distributed Hash Table ordinal/lexical search support.
- Exporting live data from the solar panels.
- Providing an auth token during the dynamic creation of an install script (daemon → otel
  tracking).
