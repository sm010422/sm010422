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
![AI Code Time](http://img.shields.io/badge/AI%20Code%20Time-184%20hrs%205%20mins-blue?style=flat)

**🐱 My GitHub Data** 

> 📦 276.1 kB Used in GitHub's Storage 
 > 
> 🏆 1,910 Contributions in the Year 2026
 > 
> 🚫 Not Opted to Hire
 > 
> 📜 36 Public Repositories 
 > 
> 🔑 4 Private Repositories 
 > 
**I'm a Night 🦉** 

```text
🌞 Morning                1226 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   08.12 % 
🌆 Daytime                5656 commits        █████████░░░░░░░░░░░░░░░░   37.46 % 
🌃 Evening                4705 commits        ████████░░░░░░░░░░░░░░░░░   31.16 % 
🌙 Night                  3513 commits        ██████░░░░░░░░░░░░░░░░░░░   23.26 % 
```
📅 **I'm Most Productive on Friday** 

```text
Monday                   1936 commits        ███░░░░░░░░░░░░░░░░░░░░░░   12.82 % 
Tuesday                  2310 commits        ████░░░░░░░░░░░░░░░░░░░░░   15.30 % 
Wednesday                2496 commits        ████░░░░░░░░░░░░░░░░░░░░░   16.53 % 
Thursday                 2004 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.27 % 
Friday                   3169 commits        █████░░░░░░░░░░░░░░░░░░░░   20.99 % 
Saturday                 1995 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.21 % 
Sunday                   1190 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   07.88 % 
```


📊 **This Week I Spent My Time On** 

```text
💬 Programming Languages: 
Other                    13 hrs 41 mins      ███████████████░░░░░░░░░░   61.14 % 
Markdown                 5 hrs 6 mins        ██████░░░░░░░░░░░░░░░░░░░   22.80 % 
C++                      1 hr 58 mins        ██░░░░░░░░░░░░░░░░░░░░░░░   08.86 % 
Zig                      34 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   02.55 % 
YAML                     20 mins             ░░░░░░░░░░░░░░░░░░░░░░░░░   01.53 % 

🔥 Editors: 
Ghostty                  12 hrs 29 mins      ██████████████░░░░░░░░░░░   55.80 % 
Claude Code              6 hrs 53 mins       ████████░░░░░░░░░░░░░░░░░   30.80 % 
Neovim                   2 hrs 58 mins       ███░░░░░░░░░░░░░░░░░░░░░░   13.31 % 
Terminal                 0 secs              ░░░░░░░░░░░░░░░░░░░░░░░░░   00.05 % 
iTerm2                   0 secs              ░░░░░░░░░░░░░░░░░░░░░░░░░   00.03 % 

🐱‍💻 Projects: 
ghostty                  7 hrs 41 mins       █████████░░░░░░░░░░░░░░░░   34.32 % 
frontend-platform-assignm4 hrs 39 mins       █████░░░░░░░░░░░░░░░░░░░░   20.83 % 
ghostty-contrib          4 hrs 21 mins       █████░░░░░░░░░░░░░░░░░░░░   19.46 % 
Unknown Project          2 hrs 4 mins        ██░░░░░░░░░░░░░░░░░░░░░░░   09.26 % 
bunpuri                  1 hr 8 mins         █░░░░░░░░░░░░░░░░░░░░░░░░   05.13 % 

💻 Operating System: 
Mac                      22 hrs 23 mins      █████████████████████████   100.00 % 
```

🤖 **AI Coding This Week** 

```text
⏱ AI Coding Time: 10 hrs 10 mins (45.45%)

✍️ 9,172 lines written by AI, 505 lines written by hand (94.78% AI-written)

🔤 3,008,743 Input Tokens, 798,958 Output Tokens

💵 $61.97 Estimated AI Cost This Week

🧠 18 AI Sessions, 141 AI Prompts

Opus                     9,305 lines         █████████████████████████   100.00 % 

🔎 AI Coding Insights:
🤖 AI-Driven — 94.78% of written lines came from AI
📄 Detailed Prompter — average 531 characters per prompt
🔁 Iterative Prompter — average 8 prompts per session
🚀 High AI Trust — 5.56% of changed lines were hand-edited
```

**I Mostly Code in Java** 

```text
Java                     16 repos            ██████████░░░░░░░░░░░░░░░   38.10 % 
TypeScript               7 repos             ████░░░░░░░░░░░░░░░░░░░░░   16.67 % 
Python                   3 repos             ██░░░░░░░░░░░░░░░░░░░░░░░   07.14 % 
Go                       2 repos             █░░░░░░░░░░░░░░░░░░░░░░░░   04.76 % 
Ruby                     1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.38 % 
```




 Last Updated on 22/11/2026 23:50:01 UTC
<!--END_SECTION:waka-->

</details>

<br>

<div align="center">
<a href="https://www.gitanimals.org/en_US?utm_medium=image&utm_source=sm010422&utm_content=farm">
<img src="https://render.gitanimals.org/farms/sm010422" width="600" height="300" />
</a>
</div>
