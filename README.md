# 박상민 | SangMin Park

> **방산 임베디드 & 백엔드 엔지니어 — 실시간 전술 시스템부터 분산 서비스까지**

C/Java 기반의 시스템 프로그래밍을 기반으로, RTOS · 전술 통신 프로토콜 · MSA 아키텍처를 직접 설계하고 구현합니다.
방산 도메인의 핵심 표준(MIL-STD-1553, DO-178C, MISRA-C)을 학습하며 신뢰성 높은 임베디드 소프트웨어 개발 역량을 쌓고 있습니다.
AI를 개발 라이프사이클 전체의 파트너로 활용하여, 더 많은 고부가가치 문제에 집중합니다.

<div align="center">

  [![wakatime](https://wakatime.com/badge/user/583a8256-10d0-4e1e-b350-cb9e4234e3b3.svg)](https://wakatime.com/@583a8256-10d0-4e1e-b350-cb9e4234e3b3)
  <a href="https://www.linkedin.com/in/%EC%83%81%EB%AF%BC-%EB%B0%95-985026297/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white"/></a>
  <a href="https://marmalade-lemming-3ae.notion.site/Study-56a666da01334f43ac9e2b33e6c08886"><img src="https://img.shields.io/badge/Study-Notion-000000?style=flat-square&logo=notion&logoColor=white"/></a>

</div>

<br>

<div align="center">

<a href="https://www.gitanimals.org/en_US?utm_medium=image&utm_source=sm010422&utm_content=farm">
<img
src="https://render.gitanimals.org/farms/sm010422"
width="600"
height="300"
/>
</a>

</div>

<br>

---

## 🛡️ Defense & Embedded Systems

### [sentinel-stack](https://github.com/sm010422/sentinel-stack)
> **전술 통신 미들웨어 스택 — RTOS · 소켓 통신 · 패킷 분석기 3-Layer 구조**

![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat-square&logo=qemu&logoColor=white)

방산 임베디드 시스템에서 요구하는 **설계 → 구현 → 검증 → 문서화** 전 과정을 포함한 포트폴리오입니다.

| Layer | 구성 | 적용 표준 |
|---|---|---|
| Layer 3 | Packet Analyzer — 실시간 캡처 · 프로토콜 파싱 · 이상 탐지 | Link-16 메시지 포맷 참고 |
| Layer 2 | Socket Communication — TCP/UDP 이중화 · Pub/Sub · AES 암호화 | MIL-STD-1553 이중화 참고 |
| Layer 1 | RTOS Scheduler — 선점형 · RMS/EDF · Jitter 측정 | ARINC 653, DO-178C 참고 |

- MISRA-C 2012 코딩 컨벤션 준수, QEMU(ARM) 환경에서 교차 검증
- clang-tidy 정적 분석 파이프라인 통합

<br>

### C4I System — [Target Tracking Service](https://github.com/sm010422/target-tracking-service) · [Defense API Gateway](https://github.com/sm010422/defense-api-gateway)
> **실시간 전술 객체 추적 시스템 (맥북 2대 + VM 3개 K3s 클러스터)**

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![K3s](https://img.shields.io/badge/K3s-FFC61C?style=flat-square&logo=kubernetes&logoColor=black)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square)

드론/레이더 센서 데이터를 초당 다량 수집하여 지휘통제실 대시보드로 실시간 전송하는 MSA 시스템입니다.

- **Target Tracking**: Kafka 비동기 파이프라인 → WebSocket 실시간 전송 → PostgreSQL 이력 저장
- **API Gateway**: Spring Cloud Gateway + JWT 글로벌 인증 필터 → 내부 서비스 단일 진입점 통제
- K3s 다중 Pod 복제 + 자동 Failover로 노드 장애 시 무중단 운영

<br>

### [OrbitTracer](https://github.com/sm010422/OrbitTracer)
> **위성 궤도 추적 & 지상국 패스 예측 시뮬레이터**

![C++](https://img.shields.io/badge/C++17-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)

- **SGP4/SDP4** 궤도 계산 엔진(C++)과 WPF 실시간 모니터링 GUI(C#)를 연동한 데스크탑 앱
- TLE 데이터 기반 위성 위치 계산 · AOS/LOS 패스 예측 · Elevation/Azimuth 가시성 분석
- CelesTrak 공개 데이터 연동, 이상 상태 임계값 알림

<br>

---

## 🚀 Backend & Application Projects

### [Sofly](https://github.com/Nagaja2world/Sofly_Back)
> **AI 기반 그룹 여행 플래닝 서비스 — 멀티모듈 MSA 백엔드**

![Java](https://img.shields.io/badge/Java_21-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.x-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Spring AI](https://img.shields.io/badge/Spring_AI-6DB33F?style=flat-square&logo=spring&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

두 서비스를 독립 배포하는 **Gradle 멀티모듈 모노레포** 구조입니다.

| 서비스 | 아키텍처 | 담당 도메인 |
|---|---|---|
| `travel-core-service` | 레이어드 아키텍처 | 인증·워크스페이스·AI 채팅·일정·앨범·정복 지도 |
| `travel-supply-service` | 헥사고날 아키텍처 | 항공권·호텔·장소 외부 공급사 연동 |

- **인증**: JWT + OAuth2(Google·Kakao·Naver), Refresh Token Redis 저장 / Stateless 세션
- **AI 채팅**: Google Gemini 2.5 Flash(Spring AI) + Redis 메모리 캐시(24h TTL) 기반 3단계 여행 추천
- **이벤트 파이프라인**: Kafka — 항공편 저장 → 정복 지도 자동 업데이트
- **외부 연동**: Booking.com RapidAPI(항공권·호텔), Google Places API, Google Calendar API
- **스토리지**: AWS S3 + Cloudflare R2 앨범 사진 업로드
- **관측성**: Prometheus + Grafana + Zipkin(분산 트레이싱) + cAdvisor + Dozzle
- **배포**: Nginx Blue-Green 무중단 배포, GitHub Actions 서비스별 독립 CI/CD
- Spring AOP — `@RequireWorkspaceMember` 커스텀 어노테이션으로 워크스페이스 권한 체크

<br>

### [Connecteamed](https://github.com/Connecteamed/Connecteamed-BE)
> **팀 프로젝트 시작부터 회고까지 흐름을 관리하는 협업 플랫폼 — UMC 9기**

![Java](https://img.shields.io/badge/Java_17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.x-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-07ADEE?style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_Lightsail-FF9900?style=flat-square&logo=amazonaws&logoColor=white)

- 복잡한 초기 설정을 최소화하여 팀 프로젝트를 즉시 시작할 수 있는 워크스페이스 제공
- 업무 과정 데이터를 기반으로 기여도 측정, 문서 공유, 초대 흐름 관리 기능 구현
- QueryDSL 동적 쿼리, JWT + OAuth2 인증, Docker + AWS Lightsail + Nginx 배포

<br>

### [SikjajaeDeal (식자재딜)](https://github.com/sikjajaeDeal)
> **위치 기반 B2B 식자재 거래 & 검색 최적화 플랫폼**

![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Elasticsearch](https://img.shields.io/badge/Elasticsearch-005571?style=flat-square&logo=elasticsearch&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

- **Elasticsearch** 기반 대용량 식자재 데이터 검색 엔진 구축 및 성능 최적화
- **KakaoMap Open API**를 활용한 사용자 위치 기반 매물 매칭 시스템

<br>

### [Snowpeak Game](https://github.com/sm010422/snowpeak_game)
> **실시간 협동 카페 운영 시뮬레이션 게임 — Race Condition & 동시성 제어**

![Java](https://img.shields.io/badge/Java_17-ED8B00?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot_3.x-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket_STOMP-010101?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

실제 아르바이트 경험을 바탕으로 만든 멀티플레이 협동 타이쿤 게임. 홀·바 역할 분담으로 손님을 응대하는 구조이며, 핵심 목표는 **동시성 문제 해결**입니다.

- **Lua Script 원자성 보장** — 두 플레이어가 동일 주문을 동시에 집는 Race Condition을 Redis Lua Script로 원천 차단
- **Producer-Consumer 패턴** — 주문 대기열을 Redis List로 구현, 주방·홀 간 비동기 처리
- **Redis SETNX** — 테이블 중복 배정 방지 / **Pub/Sub** — 주문 상태 변경을 전 직원에게 실시간 전파
- WebSocket(STOMP)으로 매장 전체 상태(주문·테이블) 실시간 동기화

<br>

### [LikeLion-RealTalk](https://github.com/LikeLion-RealTalk)
> **Claude AI 팩트체크 기반 실시간 토론 플랫폼**

![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![WebSocket](https://img.shields.io/badge/WebSocket-010101?style=flat-square)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Claude](https://img.shields.io/badge/Claude_API-D97757?style=flat-square)

- **WebSocket Pub/Sub** 패턴으로 실시간 토론방 입장 및 채팅 동기화 구현
- 참여자 찬/반 진영 정보를 Redis에 캐싱하여 DB 부하 최소화 및 조회 속도 개선
- 실시간 여론(찬반 퍼센트) 및 참여자 수 집계 로직 구현

### [memory-viz](https://github.com/sm010422/memory-viz)
> **macOS 메모리 구조 실시간 시각화 도구**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![macOS](https://img.shields.io/badge/macOS-000000?style=flat-square&logo=apple&logoColor=white)

- `vm_stat` · `ps aux` · `vmmap` 세 시스템 명령어를 주기적으로 실행해 macOS 메모리 구조를 브라우저에서 실시간 시각화
- 물리 메모리를 wired·active·inactive·compressed·free 5구역으로 분류하여 표시
- 프로세스 클릭 시 `vmmap --wide <PID>` 로 **가상 주소 공간(Stack·Heap·\_\_TEXT·\_\_DATA)** 레이아웃 시각화
- OS 페이지 관리 메커니즘을 직접 파고든 시스템 레벨 프로젝트

<br>

---

## ⌨️ Dev Environment

> 터미널 환경 전체를 직접 구성하고 형상 관리합니다.

<table>
<tr>
<td align="center" width="160"><b>Terminal</b><br><a href="https://github.com/sm010422/terminal_backup">terminal_backup</a></td>
<td>Ghostty · iTerm2 · Zsh + Oh-My-Zsh · Powerlevel10k · Hammerspoon(macOS 자동화)</td>
</tr>
<tr>
<td align="center"><b>Multiplexer</b></td>
<td>tmux — 세션/윈도우/페인 커스텀 키바인딩, 지속 개발 환경 구성</td>
</tr>
<tr>
<td align="center"><b>Editor</b><br><a href="https://github.com/sm010422/nvim">nvim</a></td>
<td>Neovim + <a href="https://lazyvim.org">LazyVim</a> — tokyonight-night 테마, LSP · Telescope · 커스텀 플러그인 구성</td>
</tr>
<tr>
<td align="center"><b>Dotfiles</b></td>
<td>.zshrc · .tmux.conf · .gitconfig · Homebrew 패키지 목록 백업 및 동기화</td>
</tr>
</table>

<br>

---

## 🛠 Tech Stack

**Backend**
<br>
<img src="https://skillicons.dev/icons?i=java,spring,gradle,hibernate,mysql,mongodb,postgresql,redis,kafka,elasticsearch" />

**DevOps & Infrastructure**
<br>
<img src="https://skillicons.dev/icons?i=docker,kubernetes,terraform,aws,nginx,jenkins,githubactions,grafana,prometheus,linux,ubuntu,bash" />

**Languages & Tools**
<br>
<img src="https://skillicons.dev/icons?i=py,apple,git,github,postman,notion,md,vim,neovim,idea" />

<br>

---

## 📊 Github Stats

<div align="center">
  <div style="display: flex; justify-content: center; gap: 10px;">
    <img height="200em" src="https://github-readme-stats-sm010422.vercel.app/api/top-langs/?username=sm010422&layout=compact&theme=dark&hide_border=true&langs_count=6&hide=javascript,html,css" />
    <img height="200em" src="https://github-readme-stats-sm010422.vercel.app/api?username=sm010422&theme=dark&hide_border=true&count_private=true&include_all_commits=true" />
  </div>
</div>

<br>
<!--START_SECTION:waka-->
**🐱 My GitHub Data** 

> 📦 269.4 kB Used in GitHub's Storage 
 > 
> 🏆 1,438 Contributions in the Year 2026
 > 
> 🚫 Not Opted to Hire
 > 
> 📜 26 Public Repositories 
 > 
> 🔑 3 Private Repositories 
 > 
**I'm a Night 🦉** 

```text
🌞 Morning                1163 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   07.95 % 
🌆 Daytime                5447 commits        █████████░░░░░░░░░░░░░░░░   37.26 % 
🌃 Evening                4558 commits        ████████░░░░░░░░░░░░░░░░░   31.18 % 
🌙 Night                  3452 commits        ██████░░░░░░░░░░░░░░░░░░░   23.61 % 
```
📅 **I'm Most Productive on Friday** 

```text
Monday                   1761 commits        ███░░░░░░░░░░░░░░░░░░░░░░   12.05 % 
Tuesday                  2231 commits        ████░░░░░░░░░░░░░░░░░░░░░   15.26 % 
Wednesday                2397 commits        ████░░░░░░░░░░░░░░░░░░░░░   16.40 % 
Thursday                 1979 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.54 % 
Friday                   3124 commits        █████░░░░░░░░░░░░░░░░░░░░   21.37 % 
Saturday                 1979 commits        ███░░░░░░░░░░░░░░░░░░░░░░   13.54 % 
Sunday                   1149 commits        ██░░░░░░░░░░░░░░░░░░░░░░░   07.86 % 
```


📊 **This Week I Spent My Time On** 

```text
💬 Programming Languages: 
Other                    4 hrs 45 mins       ███████████░░░░░░░░░░░░░░   42.39 % 
Markdown                 2 hrs 1 min         █████░░░░░░░░░░░░░░░░░░░░   18.04 % 
dbout                    1 hr 1 min          ██░░░░░░░░░░░░░░░░░░░░░░░   09.07 % 
C                        50 mins             ██░░░░░░░░░░░░░░░░░░░░░░░   07.53 % 
Bash                     40 mins             ██░░░░░░░░░░░░░░░░░░░░░░░   06.00 % 

🔥 Editors: 
iTerm2                   3 hrs 33 mins       ████████░░░░░░░░░░░░░░░░░   31.75 % 
Claude Code              3 hrs 13 mins       ███████░░░░░░░░░░░░░░░░░░   28.81 % 
Neovim                   3 hrs 1 min         ███████░░░░░░░░░░░░░░░░░░   27.02 % 
Ghostty                  1 hr 23 mins        ███░░░░░░░░░░░░░░░░░░░░░░   12.42 % 

🐱‍💻 Projects: 
sentinel-stack           3 hrs 28 mins       ████████░░░░░░░░░░░░░░░░░   30.91 % 
Unknown Project          2 hrs 18 mins       █████░░░░░░░░░░░░░░░░░░░░   20.53 % 
wagu_BE                  1 hr 45 mins        ████░░░░░░░░░░░░░░░░░░░░░   15.62 % 
Oliveyoung_Pipeline      1 hr 3 mins         ██░░░░░░░░░░░░░░░░░░░░░░░   09.37 % 
terminal_backup_file     1 hr                ██░░░░░░░░░░░░░░░░░░░░░░░   08.91 % 

💻 Operating System: 
Mac                      11 hrs 13 mins      █████████████████████████   100.00 % 
```

**I Mostly Code in Java** 

```text
Java                     15 repos            ███████████░░░░░░░░░░░░░░   44.12 % 
C                        2 repos             █░░░░░░░░░░░░░░░░░░░░░░░░   05.88 % 
JavaScript               2 repos             █░░░░░░░░░░░░░░░░░░░░░░░░   05.88 % 
Python                   1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.94 % 
C#                       1 repo              █░░░░░░░░░░░░░░░░░░░░░░░░   02.94 % 
```




 Last Updated on 10/06/2026 21:11:54 UTC
<!--END_SECTION:waka-->

## 📊 WakaTime Stats

<!-- <div align="center">
  <img src="https://wakatime.com/share/@583a8256-10d0-4e1e-b350-cb9e4234e3b3/0dc9da9c-8d19-481b-a00e-fc373a40bce2.svg" height="500" />
</div> -->
> 💡 **Other** includes terminal usage time tracked by WakaTime (tmux, zsh, etc.)
<div align="center">
  <img
    src="https://github-readme-stats-sm010422.vercel.app/api/wakatime?username=sm010422&layout=compact&icon_color=2d77dc&title_color=2d77dc&text_color=ffffff&bg_color=0d1117&hide_border=true&custom_title=WakaTime%20Stats&disable_animations=true&v=1"
    alt="WakaTime Stats"
  />
</div>

## 🧩 LeetCode
<div align="center">
  <img height="200em" src="https://leetcard.jacoblin.cool/sm010422?border=0&radius=20&theme=dark" width="98%" />
</div>

<br>
<br>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=auto&height=200&section=footer" />
</div>
