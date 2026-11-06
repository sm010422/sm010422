# 박상민 | SangMin Park

> **백엔드 엔지니어 — Java/Spring 기반 분산 서비스를 설계하고 배포까지 직접 운영합니다**

Kafka 이벤트 파이프라인, MSA, K3s + GitOps 배포까지 백엔드 시스템을 처음부터 끝까지 만들어 봅니다.
동시성 · 실시간 처리 같은 까다로운 문제를 좋아하고, AI를 개발 라이프사이클 전체의 파트너로 활용합니다.

<div align="center">

[![wakatime](https://wakatime.com/badge/user/583a8256-10d0-4e1e-b350-cb9e4234e3b3.svg)](https://wakatime.com/@583a8256-10d0-4e1e-b350-cb9e4234e3b3)
<a href="https://www.linkedin.com/in/%EC%83%81%EB%AF%BC-%EB%B0%95-985026297/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white"/></a>

<a href="https://sm010422.notion.site/Study-56a666da01334f43ac9e2b33e6c08886"><img src="./assets/study-banner.svg" width="100%" alt="Study Log"/></a>

</div>

---

## 🚀 Featured Projects

### C4I System — [Target Tracking](https://github.com/sm010422/target-tracking-service) · [API Gateway](https://github.com/sm010422/defense-api-gateway) · [Threat Intel AI](https://github.com/sm010422/threat-intel-ai-service)
> **실시간 객체 추적 + AI 위협 분석 폴리글랏 MSA — 맥북 2대 + VM 3개 K3s 클러스터, GitOps 자동 배포**

`Java 21` `Spring Boot` `Kafka` `Python` `FastAPI` `K3s` `ArgoCD` `WebSocket`

- 드론 시뮬레이터 + 실제 공개 ADS-B 피드(adsb.fi)를 **Kafka → WebSocket** 파이프라인으로 실시간 대시보드에 전송
- 성격이 다른 AI 서비스 2개(pgvector + Gemini RAG / LangGraph + Qdrant)가 **같은 토픽을 독립 consumer group으로** 구독
- GitHub Actions → Docker Hub → **ArgoCD Image Updater write-back**으로 클러스터 반영까지 무개입 배포를 실측 검증
- VMware → Multipass 마이그레이션으로 반복되던 노드 OOM/NotReady 장애 해소

### [Sofly](https://github.com/Nagaja2world/Sofly_Back)
> **AI 기반 그룹 여행 플래닝 서비스 — Gradle 멀티모듈 MSA 백엔드**

`Java 21` `Spring Boot 3` `Spring AI` `Kafka` `PostgreSQL` `Redis` `Grafana`

- 레이어드(`travel-core`) + 헥사고날(`travel-supply`) 두 서비스를 독립 배포하는 모노레포
- Gemini 2.5 Flash(Spring AI) + Redis 대화 메모리로 3단계 여행 추천, Kafka로 항공편 저장 → 정복 지도 자동 갱신
- Prometheus · Grafana · Zipkin 관측성, Nginx Blue-Green 무중단 배포

### [Snowpeak Game](https://github.com/sm010422/snowpeak_game)
> **실시간 협동 카페 운영 시뮬레이션 — Race Condition & 동시성 제어**

`Java 17` `Spring Boot 3` `WebSocket(STOMP)` `Redis`

- 두 플레이어가 같은 주문을 동시에 집는 Race Condition을 **Redis Lua Script**로 원천 차단
- Redis List 기반 Producer-Consumer 주문 대기열, SETNX로 테이블 중복 배정 방지, Pub/Sub 상태 전파

<details>
<summary><b>📁 More Projects</b></summary>

<br>

| Project | 한 줄 소개 | Key |
|---|---|---|
| [Connecteamed](https://github.com/Connecteamed/Connecteamed-BE) | 팀 프로젝트 시작부터 회고까지 관리하는 협업 플랫폼 (UMC 9기) | QueryDSL · JWT/OAuth2 · AWS Lightsail |
| [SikjajaeDeal](https://github.com/sikjajaeDeal) | 위치 기반 B2B 식자재 거래 & 검색 플랫폼 | Elasticsearch · KakaoMap API |
| [LikeLion-RealTalk](https://github.com/LikeLion-RealTalk) | Claude AI 팩트체크 기반 실시간 토론 플랫폼 | WebSocket Pub/Sub · Redis |
| [memory-viz](https://github.com/sm010422/memory-viz) | macOS 물리/가상 메모리 구조 실시간 시각화 | Python · vm_stat · vmmap |

</details>

---

## 🛠 Tech Stack

**Backend** &nbsp; <img src="https://skillicons.dev/icons?i=java,spring,gradle,hibernate,mysql,postgresql,mongodb,redis,kafka,elasticsearch" height="32" />

**Infra** &nbsp; <img src="https://skillicons.dev/icons?i=docker,kubernetes,terraform,aws,nginx,githubactions,grafana,prometheus,linux" height="32" />

**Tools** &nbsp; <img src="https://skillicons.dev/icons?i=py,git,neovim,idea,notion,postman" height="32" />

**Dev Environment** — Ghostty · Zsh · tmux · [Neovim(LazyVim)](https://github.com/sm010422/nvim) · Hammerspoon, 전부 [dotfiles](https://github.com/sm010422/terminal_backup)로 형상 관리

---

## 📊 Activity

<div align="center">
  <img height="170" src="https://github-readme-stats-sm010422.vercel.app/api?username=sm010422&theme=dark&hide_border=true&count_private=true&include_all_commits=true" />
</div>

<details>
<summary><b>⏱ WakaTime 상세 지표 (매일 자동 갱신)</b></summary>

<br>

> 💡 **Other** 는 WakaTime이 집계한 터미널 사용 시간(tmux, zsh 등)입니다.

<!--START_SECTION:waka-->
![AI Code Time](http://img.shields.io/badge/AI%20Code%20Time-159%20hrs%2042%20mins-blue?style=flat)

**🐱 My GitHub Data** 

> 📦 275.6 kB Used in GitHub's Storage 
 > 
> 🏆 1,851 Contributions in the Year 2026
 > 
> 🚫 Not Opted to Hire
 > 
> 📜 34 Public Repositories 
 > 
> 🔑 3 Private Repositories 
 > 
**I'm a Night 🦉** 

```text
🌞 Morning                1225 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   08.15 % 
🌆 Daytime                5621 commits        █████████░░░░░░░░░░░░░░░░   37.38 % 
🌃 Evening                4682 commits        ████████░░░░░░░░░░░░░░░░░   31.14 % 
🌙 Night                  3509 commits        ██████░░░░░░░░░░░░░░░░░░░   23.34 % 
```
📅 **I'm Most Productive on Friday** 

```text
Monday                   1920 commits        ███░░░░░░░░░░░░░░░░░░░░░░   12.77 % 
Tuesday                  2310 commits        ████░░░░░░░░░░░░░░░░░░░░░   15.36 % 
Wednesday                2495 commits        ████░░░░░░░░░░░░░░░░░░░░░   16.59 % 
Thursday                 2001 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.31 % 
Friday                   3146 commits        █████░░░░░░░░░░░░░░░░░░░░   20.92 % 
Saturday                 1989 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.23 % 
Sunday                   1176 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   07.82 % 
```


📊 **This Week I Spent My Time On** 

```text
💬 Programming Languages: 
Other                    10 hrs 11 mins      ████████████████░░░░░░░░░   65.33 % 
Markdown                 1 hr 57 mins        ███░░░░░░░░░░░░░░░░░░░░░░   12.58 % 
Python                   1 hr 27 mins        ██░░░░░░░░░░░░░░░░░░░░░░░   09.30 % 
Bash                     45 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   04.89 % 
JSON                     22 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   02.42 % 

🔥 Editors: 
Ghostty                  9 hrs 37 mins       ███████████████░░░░░░░░░░   61.64 % 
Claude Code              4 hrs 53 mins       ████████░░░░░░░░░░░░░░░░░   31.31 % 
Neovim                   1 hr 6 mins         ██░░░░░░░░░░░░░░░░░░░░░░░   07.05 % 

🐱‍💻 Projects: 
personal-knowledge-graph-6 hrs 30 mins       ██████████░░░░░░░░░░░░░░░   41.69 % 
portfolio                2 hrs 42 mins       ████░░░░░░░░░░░░░░░░░░░░░   17.29 % 
terminal_backup          2 hrs 41 mins       ████░░░░░░░░░░░░░░░░░░░░░   17.21 % 
Unknown Project          57 mins             ██░░░░░░░░░░░░░░░░░░░░░░░   06.10 % 
k3s-msa-infrastructure   39 mins             █░░░░░░░░░░░░░░░░░░░░░░░░   04.18 % 

💻 Operating System: 
Mac                      15 hrs 36 mins      █████████████████████████   100.00 % 
```

🤖 **AI Coding This Week** 

```text
⏱ AI Coding Time: 7 hrs 38 mins (48.96%)

✍️ 2,588 lines written by AI, 46 lines written by hand (98.25% AI-written)

🔤 2,715,321 Input Tokens, 593,905 Output Tokens

💵 $37.37 Estimated AI Cost This Week

🧠 23 AI Sessions, 160 AI Prompts

Opus                     2,690 lines         █████████████████████████   100.00 % 

🔎 AI Coding Insights:
🤖 AI-Driven — 98.25% of written lines came from AI
📝 Concise Prompter — average 464 characters per prompt
🔁 Iterative Prompter — average 7 prompts per session
🚀 High AI Trust — 2.07% of changed lines were hand-edited
```

**I Mostly Code in Java** 

```text
TypeScript               6 repos             ████░░░░░░░░░░░░░░░░░░░░░   15.00 % 
Python                   3 repos             ██░░░░░░░░░░░░░░░░░░░░░░░   07.50 % 
Go                       2 repos             █░░░░░░░░░░░░░░░░░░░░░░░░   05.00 % 
Ruby                     1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.50 % 
Dockerfile               1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.50 % 
```




 Last Updated on 04/11/2026 23:57:12 UTC
<!--END_SECTION:waka-->

</details>

<br>

<div align="center">
<a href="https://www.gitanimals.org/en_US?utm_medium=image&utm_source=sm010422&utm_content=farm">
<img src="https://render.gitanimals.org/farms/sm010422" width="600" height="300" />
</a>
</div>
