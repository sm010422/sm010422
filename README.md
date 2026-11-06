# Hi, I'm SangMin Park 👋

> **Backend Engineer** — I design distributed services on Java/Spring and own them all the way through deployment and operations.

- 🔧 I build systems **end-to-end** — from Kafka event pipelines and MSA to K3s + GitOps deployment
- ⚡ I enjoy the tricky parts: concurrency, race conditions, and real-time processing
- 🤖 I work with AI as a pair across the whole development lifecycle

<div align="center">

[![wakatime](https://wakatime.com/badge/user/583a8256-10d0-4e1e-b350-cb9e4234e3b3.svg)](https://wakatime.com/@583a8256-10d0-4e1e-b350-cb9e4234e3b3)
<a href="https://www.linkedin.com/in/%EC%83%81%EB%AF%BC-%EB%B0%95-985026297/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white"/></a>

<a href="https://sm010422.notion.site/Study-56a666da01334f43ac9e2b33e6c08886"><img src="./assets/study-banner.svg" width="100%" alt="Study Log"/></a>

</div>

---

## 🚀 Featured Projects

### C4I System — [Target Tracking](https://github.com/sm010422/target-tracking-service) · [API Gateway](https://github.com/sm010422/defense-api-gateway) · [Threat Intel AI](https://github.com/sm010422/threat-intel-ai-service)
> **Real-time object tracking + AI threat analysis, polyglot MSA on a self-built K3s cluster**

`Java 21` `Spring Boot` `Kafka` `Python` `FastAPI` `K3s` `ArgoCD` `WebSocket`

- Streams a drone simulator and a live ADS-B feed (adsb.fi) to a real-time dashboard through a **Kafka → WebSocket** pipeline
- Two AI services with different approaches (pgvector + Gemini RAG / LangGraph + Qdrant) consume **the same topic as independent consumer groups**
- Verified zero-touch deployment end to end: GitHub Actions → Docker Hub → **ArgoCD Image Updater write-back**
- Migrated from VMware to Multipass to fix recurring node OOM / NotReady failures

### [Sofly](https://github.com/Nagaja2world/Sofly_Back)
> **AI-powered group travel planner — Gradle multi-module MSA backend**

`Java 21` `Spring Boot 3` `Spring AI` `Kafka` `PostgreSQL` `Redis` `Grafana`

- Monorepo with two independently deployed services: layered (`travel-core`) and hexagonal (`travel-supply`)
- Three-step trip recommendations with Gemini 2.5 Flash (Spring AI) and Redis-backed conversation memory; saving a flight updates the user's travel map via Kafka
- Observability with Prometheus · Grafana · Zipkin; zero-downtime Nginx blue-green deployment

### [Snowpeak Game](https://github.com/sm010422/snowpeak_game)
> **Real-time co-op café tycoon — solving race conditions in multiplayer state**

`Java 17` `Spring Boot 3` `WebSocket(STOMP)` `Redis`

- Eliminated the race condition where two players grab the same order at once, using an atomic **Redis Lua script**
- Producer-consumer order queue on Redis Lists, SETNX to prevent double-assigning tables, Pub/Sub to broadcast state changes

<details>
<summary><b>📁 More Projects</b></summary>

<br>

| Project | Description | Key |
|---|---|---|
| [Connecteamed](https://github.com/Connecteamed/Connecteamed-BE) | Team collaboration platform covering a project from kickoff to retrospective (UMC 9th) | QueryDSL · JWT/OAuth2 · AWS Lightsail |
| [SikjajaeDeal](https://github.com/sikjajaeDeal) | Location-based B2B marketplace and search platform for food ingredients | Elasticsearch · KakaoMap API |
| [LikeLion-RealTalk](https://github.com/LikeLion-RealTalk) | Real-time debate platform with Claude AI fact-checking | WebSocket Pub/Sub · Redis |
| [memory-viz](https://github.com/sm010422/memory-viz) | Real-time visualizer for macOS physical and virtual memory layout | Python · vm_stat · vmmap |

</details>

---

## 🛠 Tech Stack

**Backend** &nbsp; <img src="https://skillicons.dev/icons?i=java,spring,gradle,hibernate,mysql,postgresql,mongodb,redis,kafka" height="32" />

**Infra** &nbsp; <img src="https://skillicons.dev/icons?i=docker,kubernetes,terraform,aws,nginx,githubactions,grafana,prometheus,linux" height="32" />

**Tools** &nbsp; <img src="https://skillicons.dev/icons?i=py,git,neovim,idea,notion,postman" height="32" />

**Dev Environment** — Ghostty · Zsh · tmux · [Neovim(LazyVim)](https://github.com/sm010422/nvim) · Hammerspoon, all version-controlled in my [dotfiles](https://github.com/sm010422/terminal_backup)

---

## 📊 Activity

<div align="center">
  <img height="170" src="https://github-readme-stats-sm010422.vercel.app/api?username=sm010422&theme=dark&hide_border=true&count_private=true&include_all_commits=true" />
</div>

<details>
<summary><b>⏱ WakaTime Metrics (auto-updated daily)</b></summary>

<br>

> 💡 **Other** is terminal time tracked by WakaTime (tmux, zsh, etc.)

<!--START_SECTION:waka-->
![AI Code Time](http://img.shields.io/badge/AI%20Code%20Time-160%20hrs%2037%20mins-blue?style=flat)

**🐱 My GitHub Data** 

> 📦 275.7 kB Used in GitHub's Storage 
 > 
> 🏆 1,863 Contributions in the Year 2026
 > 
> 🚫 Not Opted to Hire
 > 
> 📜 34 Public Repositories 
 > 
> 🔑 3 Private Repositories 
 > 
**I'm a Night 🦉** 

```text
🌞 Morning                1225 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   08.14 % 
🌆 Daytime                5631 commits        █████████░░░░░░░░░░░░░░░░   37.42 % 
🌃 Evening                4682 commits        ████████░░░░░░░░░░░░░░░░░   31.11 % 
🌙 Night                  3511 commits        ██████░░░░░░░░░░░░░░░░░░░   23.33 % 
```
📅 **I'm Most Productive on Friday** 

```text
Monday                   1920 commits        ███░░░░░░░░░░░░░░░░░░░░░░   12.76 % 
Tuesday                  2310 commits        ████░░░░░░░░░░░░░░░░░░░░░   15.35 % 
Wednesday                2495 commits        ████░░░░░░░░░░░░░░░░░░░░░   16.58 % 
Thursday                 2004 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.32 % 
Friday                   3155 commits        █████░░░░░░░░░░░░░░░░░░░░   20.96 % 
Saturday                 1989 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.22 % 
Sunday                   1176 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   07.81 % 
```


📊 **This Week I Spent My Time On** 

```text
💬 Programming Languages: 
Other                    11 hrs 48 mins      █████████████████░░░░░░░░   67.65 % 
Markdown                 2 hrs 59 mins       ████░░░░░░░░░░░░░░░░░░░░░   17.15 % 
Python                   1 hr 41 mins        ██░░░░░░░░░░░░░░░░░░░░░░░   09.71 % 
Bash                     23 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   02.28 % 
conf                     10 mins             ░░░░░░░░░░░░░░░░░░░░░░░░░   01.03 % 

🔥 Editors: 
Ghostty                  10 hrs 5 mins       ██████████████░░░░░░░░░░░   57.77 % 
Claude Code              6 hrs 38 mins       ██████████░░░░░░░░░░░░░░░   38.06 % 
Neovim                   43 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   04.18 % 

🐱‍💻 Projects: 
portfolio                6 hrs 58 mins       ██████████░░░░░░░░░░░░░░░   39.92 % 
terminal_backup          2 hrs 29 mins       ████░░░░░░░░░░░░░░░░░░░░░   14.23 % 
personal-knowledge-graph-2 hrs 28 mins       ████░░░░░░░░░░░░░░░░░░░░░   14.17 % 
toss                     1 hr 30 mins        ██░░░░░░░░░░░░░░░░░░░░░░░   08.66 % 
ghostty                  1 hr 18 mins        ██░░░░░░░░░░░░░░░░░░░░░░░   07.49 % 

💻 Operating System: 
Mac                      17 hrs 27 mins      █████████████████████████   100.00 % 
```

🤖 **AI Coding This Week** 

```text
⏱ AI Coding Time: 9 hrs 54 mins (56.71%)

✍️ 4,702 lines written by AI, 27 lines written by hand (99.43% AI-written)

🔤 4,183,605 Input Tokens, 994,714 Output Tokens

💵 $68.38 Estimated AI Cost This Week

🧠 23 AI Sessions, 182 AI Prompts

Opus                     4,812 lines         █████████████████████████   100.00 % 

🔎 AI Coding Insights:
🤖 AI-Driven — 99.43% of written lines came from AI
📄 Detailed Prompter — average 680 characters per prompt
🔁 Iterative Prompter — average 8 prompts per session
🚀 High AI Trust — 0.89% of changed lines were hand-edited
```

**I Mostly Code in Java** 

```text
TypeScript               6 repos             ████░░░░░░░░░░░░░░░░░░░░░   15.00 % 
Python                   3 repos             ██░░░░░░░░░░░░░░░░░░░░░░░   07.50 % 
Go                       2 repos             █░░░░░░░░░░░░░░░░░░░░░░░░   05.00 % 
Ruby                     1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.50 % 
Dockerfile               1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.50 % 
```




 Last Updated on 06/11/2026 18:40:27 UTC
<!--END_SECTION:waka-->

</details>

<br>

<div align="center">
<a href="https://www.gitanimals.org/en_US?utm_medium=image&utm_source=sm010422&utm_content=farm">
<img src="https://render.gitanimals.org/farms/sm010422" width="600" height="300" />
</a>
</div>
