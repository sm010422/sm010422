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
![AI Code Time](http://img.shields.io/badge/AI%20Code%20Time-170%20hrs%2053%20mins-blue?style=flat)

**🐱 My GitHub Data** 

> 📦 275.8 kB Used in GitHub's Storage 
 > 
> 🏆 1,873 Contributions in the Year 2026
 > 
> 🚫 Not Opted to Hire
 > 
> 📜 35 Public Repositories 
 > 
> 🔑 3 Private Repositories 
 > 
**I'm a Night 🦉** 

```text
🌞 Morning                1225 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   08.14 % 
🌆 Daytime                5631 commits        █████████░░░░░░░░░░░░░░░░   37.40 % 
🌃 Evening                4688 commits        ████████░░░░░░░░░░░░░░░░░   31.14 % 
🌙 Night                  3513 commits        ██████░░░░░░░░░░░░░░░░░░░   23.33 % 
```
📅 **I'm Most Productive on Friday** 

```text
Monday                   1920 commits        ███░░░░░░░░░░░░░░░░░░░░░░   12.75 % 
Tuesday                  2310 commits        ████░░░░░░░░░░░░░░░░░░░░░   15.34 % 
Wednesday                2495 commits        ████░░░░░░░░░░░░░░░░░░░░░   16.57 % 
Thursday                 2004 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.31 % 
Friday                   3155 commits        █████░░░░░░░░░░░░░░░░░░░░   20.95 % 
Saturday                 1995 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.25 % 
Sunday                   1178 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   07.82 % 
```


📊 **This Week I Spent My Time On** 

```text
💬 Programming Languages: 
Other                    7 hrs 25 mins       ███████████████░░░░░░░░░░   61.08 % 
Markdown                 3 hrs 46 mins       ████████░░░░░░░░░░░░░░░░░   31.07 % 
Bash                     23 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   03.27 % 
Swift                    19 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   02.73 % 
tmux                     13 mins             ░░░░░░░░░░░░░░░░░░░░░░░░░   01.85 % 

🔥 Editors: 
Ghostty                  7 hrs 21 mins       ███████████████░░░░░░░░░░   60.58 % 
Claude Code              4 hrs 25 mins       █████████░░░░░░░░░░░░░░░░   36.41 % 
Neovim                   16 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   02.31 % 
iTerm2                   4 mins              ░░░░░░░░░░░░░░░░░░░░░░░░░   00.62 % 
Terminal                 0 secs              ░░░░░░░░░░░░░░░░░░░░░░░░░   00.05 % 

🐱‍💻 Projects: 
ghostty                  6 hrs 18 mins       █████████████░░░░░░░░░░░░   51.93 % 
terminal_backup          2 hrs 40 mins       ██████░░░░░░░░░░░░░░░░░░░   22.00 % 
sm010422                 1 hr 46 mins        ████░░░░░░░░░░░░░░░░░░░░░   14.56 % 
ime-notes                21 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   02.92 % 
ghostty-contrib          19 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   02.67 % 

💻 Operating System: 
Mac                      12 hrs 9 mins       █████████████████████████   100.00 % 
```

🤖 **AI Coding This Week** 

```text
⏱ AI Coding Time: 6 hrs 55 mins (56.96%)

✍️ 711 lines written by AI, 193 lines written by hand (78.65% AI-written)

🔤 1,396,376 Input Tokens, 348,616 Output Tokens

💵 $30.74 Estimated AI Cost This Week

🧠 11 AI Sessions, 151 AI Prompts

Opus                     711 lines           █████████████████████████   100.00 % 

🔎 AI Coding Insights:
🤖 AI-Driven — 78.65% of written lines came from AI
📝 Concise Prompter — average 390 characters per prompt
🔁 Iterative Prompter — average 14 prompts per session
🚀 High AI Trust — 21.35% of changed lines were hand-edited
```

**I Mostly Code in Java** 

```text
TypeScript               6 repos             ████░░░░░░░░░░░░░░░░░░░░░   15.00 % 
Python                   3 repos             ██░░░░░░░░░░░░░░░░░░░░░░░   07.50 % 
Go                       2 repos             █░░░░░░░░░░░░░░░░░░░░░░░░   05.00 % 
Ruby                     1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.50 % 
Dockerfile               1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.50 % 
```




 Last Updated on 13/11/2026 23:52:24 UTC
<!--END_SECTION:waka-->

</details>

<br>

<div align="center">
<a href="https://www.gitanimals.org/en_US?utm_medium=image&utm_source=sm010422&utm_content=farm">
<img src="https://render.gitanimals.org/farms/sm010422" width="600" height="300" />
</a>
</div>
