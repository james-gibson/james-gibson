> James is looking for work that doesn't feel like work

- 🕸️ https://jamesgibson.co
- :octocat: https://github.com/james-gibson

## What is James up to lately?


- `local-time-system`
  | a comprehensive TypeScript library for managing temporal universes, cross-universe references, and temporal relationships. It provides a sophisticated framework for tracking time across fictional and real works, with support for zero-reference addressing, temporal paradoxes, and complex reference chains

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

### Creating a Historical Event Universe

```typescript
const universe = new UniverseBuilder()
  .historicalEvent('jfk_assassination', 1963)
  .withDateRange(1963, 11, 22, 1963, 11, 22, TimePrecision.SECOND)
  .withRealityRelation('documentary', 0.0)
  .withPublicDomain(['Warren Commission Report'])
  .addDateKeyframe(1963, 11, 22, 12, 30, 0, 'first_shot', 1.0, ['assassination'])
  .build();
```

### Querying Universes

```typescript
import { LocalTime } from '@local-time/temporal-system';

const localTime = new LocalTime();
await localTime.initialize();

// Find universes in 1964
const windowSearch = localTime.getWindowSearch();
const universes = await windowSearch.findUniversesInWindow('cal:1964');

// Get specific universe
const registry = localTime.getRegistry();
const maryPoppins = registry.getUniverse('disney:mary_poppins:1964');
```
</details>

- (mcp)
- Project, Art?
  - 
- (personal api)

## Work James tricked himself into doing:

- Converting his homelab onto low voltage hardware to maximize utilization of local solar production
- Created reverse proxies for my applications to minimize puncturing my home firewall and to centralize TLS management
- My homelab supports multiple federated react apps backed by a shared node.js api
  - While exploring CQRS patterns I load tested the system by live rendering random markdown content from my web-hook security updates table, achieving 300 - 1k req/s
  - <img width="1705" height="628" alt="image" src="https://github.com/user-attachments/assets/66cff645-a456-49dc-bee5-6b6921c61992" />
- I use the lab to explore things like
  - Personal Github application posts web-hook security updates that I convert into test content for my markdown exploration
  - `Project, Art?` started as an exploration in rendering MDX into JSX securely using nonce or sha CSPs)
  - Personal MCP server directly connected to `Project, Art?` via a simple SExpression pattern
    - LLM's speak markdown, this is intended to allow me to repeatably create prompts and artifacts
    - The native MDX support already baked in means custom webcomponents can be utilized by the LLM
    - Custom webcomponents in my understanding is the next natural evolution of model response
    - Advanced RAG indexing is currently being planned for future research and implementation 
  - Custom application protocols and advanced data management via service workers
  - OAuth 2.0 Dynamic Client Registration (RFC 7591) to support QR-code addressed view adoption, complete with privacy focused 
  - Combining HTTP status code 402 with 418 to create a intra-microservice based payment system middleware themed around cups of tea as units of measure 
- My car uses those api's to write diagnostic report for me
  - <img width="553" height="1057" alt="image" src="https://github.com/user-attachments/assets/a9dd2121-141c-44ad-b030-804ade7a95f4" />

## Things James has done:
- Inherited eleven mongodb instances and developed solution to collapse them into a single database instance / api
  - The system used the OpLog for its Meteor.js integration, due to the number of active clients they had scaled it horizontally first
  - 
- Successfully converted a traditional Salesforce (copy paste) deployment cycle into a fast paced (gitops) pipeline that enabled stronger developer experience
  - This enabled the business to focus on a mobile experience quickly while enabling custom services income at the same time
  - My work was directly compared to best practices advocated by Salesforce at the time, specifcially that my approach was much smoother. (this is before salesforce bought heroku)
  - Companies Denver presence grew from three devs to over eighty team members across all areas of the business during my tenure as the second dev the founder hired full time
- Worked on a data intensive dashboard supporting 60k individual building energy reports to support tracking progress against Congressional mandate
  - Data source ingested from 12+ timezones worth of energy bills for the US Navy
  - Data aggrigated via ETL down to monthly usage for every individual building
  - Data summarized from the individual into a regional => global command view pane
 

## Things James hasn't finished yet
- Automatic service healing with zero involvement via System swarm management configured by Magnet URL
- Writing a linux daemeon to support an offsite backup service of critical application data
- Distributed Hash Table ordinal/lexical search support
- Exporting live data from the solar panels
- Providing an auth token during the dynamic creation of an install script (daemeon => otel tracking)
<!--
**james-gibson/james-gibson** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
