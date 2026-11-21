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
![AI Code Time](http://img.shields.io/badge/AI%20Code%20Time-183%20hrs%2011%20mins-blue?style=flat)

**🐱 My GitHub Data** 

> 📦 275.9 kB Used in GitHub's Storage 
 > 
> 🏆 1,897 Contributions in the Year 2026
 > 
> 🚫 Not Opted to Hire
 > 
> 📜 36 Public Repositories 
 > 
> 🔑 4 Private Repositories 
 > 
**I'm a Night 🦉** 

```text
🌞 Morning                1226 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   08.13 % 
🌆 Daytime                5640 commits        █████████░░░░░░░░░░░░░░░░   37.41 % 
🌃 Evening                4697 commits        ████████░░░░░░░░░░░░░░░░░   31.16 % 
🌙 Night                  3513 commits        ██████░░░░░░░░░░░░░░░░░░░   23.30 % 
```
📅 **I'm Most Productive on Friday** 

```text
Monday                   1936 commits        ███░░░░░░░░░░░░░░░░░░░░░░   12.84 % 
Tuesday                  2310 commits        ████░░░░░░░░░░░░░░░░░░░░░   15.32 % 
Wednesday                2496 commits        ████░░░░░░░░░░░░░░░░░░░░░   16.56 % 
Thursday                 2004 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.29 % 
Friday                   3156 commits        █████░░░░░░░░░░░░░░░░░░░░   20.93 % 
Saturday                 1995 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.23 % 
Sunday                   1179 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   07.82 % 
```


📊 **This Week I Spent My Time On** 

```text
💬 Programming Languages: 
Other                    15 hrs 52 mins      ████████████████░░░░░░░░░   62.77 % 
Markdown                 5 hrs 40 mins       ██████░░░░░░░░░░░░░░░░░░░   22.44 % 
C++                      1 hr 58 mins        ██░░░░░░░░░░░░░░░░░░░░░░░   07.84 % 
Zig                      34 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   02.25 % 
YAML                     20 mins             ░░░░░░░░░░░░░░░░░░░░░░░░░   01.35 % 

🔥 Editors: 
Ghostty                  14 hrs 35 mins      ██████████████░░░░░░░░░░░   57.74 % 
Claude Code              7 hrs 57 mins       ████████░░░░░░░░░░░░░░░░░   31.47 % 
Neovim                   2 hrs 42 mins       ███░░░░░░░░░░░░░░░░░░░░░░   10.72 % 
Terminal                 0 secs              ░░░░░░░░░░░░░░░░░░░░░░░░░   00.05 % 
iTerm2                   0 secs              ░░░░░░░░░░░░░░░░░░░░░░░░░   00.03 % 

🐱‍💻 Projects: 
ghostty                  11 hrs 14 mins      ███████████░░░░░░░░░░░░░░   44.46 % 
ghostty-contrib          4 hrs 24 mins       ████░░░░░░░░░░░░░░░░░░░░░   17.41 % 
frontend-platform-assignm3 hrs 16 mins       ███░░░░░░░░░░░░░░░░░░░░░░   12.95 % 
Unknown Project          2 hrs 4 mins        ██░░░░░░░░░░░░░░░░░░░░░░░   08.20 % 
ime-notes                1 hr 25 mins        █░░░░░░░░░░░░░░░░░░░░░░░░   05.65 % 

💻 Operating System: 
Mac                      25 hrs 17 mins      █████████████████████████   100.00 % 
```

🤖 **AI Coding This Week** 

```text
⏱ AI Coding Time: 12 hrs 7 mins (47.92%)

✍️ 9,718 lines written by AI, 488 lines written by hand (95.22% AI-written)

🔤 3,053,088 Input Tokens, 885,329 Output Tokens

💵 $67.45 Estimated AI Cost This Week

🧠 19 AI Sessions, 180 AI Prompts

Opus                     9,828 lines         █████████████████████████   100.00 % 

🔎 AI Coding Insights:
🤖 AI-Driven — 95.22% of written lines came from AI
📄 Detailed Prompter — average 590 characters per prompt
🔁 Iterative Prompter — average 9 prompts per session
🚀 High AI Trust — 5.13% of changed lines were hand-edited
```

**I Mostly Code in Java** 

```text
Java                     16 repos            ██████████░░░░░░░░░░░░░░░   38.10 % 
TypeScript               6 repos             ████░░░░░░░░░░░░░░░░░░░░░   14.29 % 
JavaScript               3 repos             ██░░░░░░░░░░░░░░░░░░░░░░░   07.14 % 
Python                   3 repos             ██░░░░░░░░░░░░░░░░░░░░░░░   07.14 % 
Ruby                     1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.38 % 
```




 Last Updated on 21/11/2026 23:36:47 UTC
<!--END_SECTION:waka-->

</details>

<br>

<div align="center">
<a href="https://www.gitanimals.org/en_US?utm_medium=image&utm_source=sm010422&utm_content=farm">
<img src="https://render.gitanimals.org/farms/sm010422" width="600" height="300" />
</a>
</div>
