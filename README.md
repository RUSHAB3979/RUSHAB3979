<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a2980,100:26d0ce&height=200&section=header&text=Rushab%20Patil&fontSize=58&fontColor=ffffff&fontAlignY=36&desc=Backend%20%C2%B7%20Distributed%20Systems%20%C2%B7%20Pune,%20India&descAlignY=58&descSize=18" width="100%" alt="Rushab Patil" />

<p align="center">
  <a href="https://git.io/typing-svg">
    <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=22&duration=3200&pause=900&color=26D0CE&center=true&vCenter=true&width=620&lines=Building+a+P2P+marketplace+for+idle+GPUs;FastAPI+%C2%B7+Postgres+%C2%B7+Windows+desktop+agents;I+design+for+the+failure+that+doesn't+throw" alt="What I do" />
  </a>
</p>

<p align="center">
  <!-- Paste your real URLs into the two lines below and uncomment them.
       They are held back on purpose: a badge pointing at a placeholder is a
       live 404 on the front page of your profile.
  <a href="https://linkedin.com/in/YOUR-HANDLE"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" /></a>
  <a href="mailto:YOU@example.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" /></a>
  -->
  <a href="https://github.com/RUSHAB3979?tab=repositories"><img src="https://img.shields.io/badge/My%20Repositories-181717?style=for-the-badge&logo=github&logoColor=white" alt="Repositories" /></a>
</p>

---

## 🛰️ What I'm building right now

> **A peer-to-peer marketplace for idle consumer GPUs.**
> Rent out the card in your gaming PC while you sleep. Rent someone else's when you need one.

A FastAPI control plane, a Windows tray application that supervises a local
inference runtime, Postgres, and a five-person team shipping through CI with
secret scanning, vulnerability gates and SBOM generation.

<table>
<tr><td width="50%" valign="top">

**Control plane**
`FastAPI` · `Pydantic v2` · `Postgres`

Node registry, heartbeat contract, TTL liveness, live fleet API.

</td><td width="50%" valign="top">

**Provider agent**
`Python` · `WebView2` · `Ollama`

System tray app, supervised inference server, real hardware telemetry, outbound-only.

</td></tr>
</table>

---

## 🧠 Four decisions I had to defend in writing

<table>
<tr><td>

**Liveness is derived, never stored.**
An `is_online` column plus a background sweeper means that the day the sweeper dies, every row reads *online* forever — and nothing raises. A `last_heartbeat_at` timestamp compared at read time cannot fail that way.

</td></tr>
<tr><td>

**Register upserts. Heartbeat returns 404.**
So a restored database backup heals itself: a node that gets a 404 re-registers with its full hardware profile, instead of the table quietly refilling with rows whose hardware fields are permanently null.

</td></tr>
<tr><td>

**A benchmark overstated capacity by 4.3×.**
It summed per-request throughput and excluded queue time — describing a parallel server that did not exist. Pricing built on that number inherits the error. Capacity is now measured as total tokens ÷ wall-clock time, under real concurrency.

</td></tr>
<tr><td>

**The agent's dependency list is a security boundary.**
It installs on a stranger's gaming PC. Every line in it is software shipped onto hardware I don't control. No database driver, ever — HTTP to the control plane and nothing else.

</td></tr>
</table>

<p align="center"><i>The pattern in all four: the dangerous bug isn't the one that crashes.<br/>It's the one that keeps reporting success.</i></p>

---

## 🔧 Tech

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,java,cpp,c,js,ts&theme=dark" alt="Languages" /><br/>
  <img src="https://skillicons.dev/icons?i=fastapi,django,spring,nodejs,react,tailwind&theme=dark" alt="Frameworks" /><br/>
  <img src="https://skillicons.dev/icons?i=postgres,mysql,docker,aws,git,githubactions&theme=dark" alt="Infra" /><br/>
  <img src="https://skillicons.dev/icons?i=pytorch,tensorflow,linux,arduino,raspberrypi&theme=dark" alt="ML and hardware" />
</p>

<p align="center">
  <sub>Depth is in <b>Python</b> and <b>FastAPI</b>. The rest is working familiarity — I'd rather say so than let a wall of logos imply otherwise.</sub>
</p>

---

## 📦 Selected work

| Project | What it is | Stack |
|---|---|---|
| **Decentralised GPU Marketplace** <sub>private</sub> | Control plane + Windows provider agent for renting idle consumer GPUs | `FastAPI` `Postgres` `React` |
| [**Smart India Hackathon**](https://github.com/RUSHAB3979/Smart-India-Hackathon) | SIH submission | `Python` |
| [**Secure Attendance**](https://github.com/RUSHAB3979/Secure-Attendance) | Attendance system built so proxy sign-ins *fail*, rather than go unnoticed | `Python` |
| [**Stock Market Prediction**](https://github.com/RUSHAB3979/Stock-Market-Prediction-Model) | Time-series modelling on market data | `Python` |
| [**AutoStream Logger**](https://github.com/RUSHAB3979/AutoStream-Logger) | Discord bot verifying streamer activity into Sheets, DM-only by design | `Python` |
| [**Discord Moderation Bot**](https://github.com/RUSHAB3979/Discord-Moderation-Bot) | Server moderation and automation | `Python` |
| [**NeetCode Submissions**](https://github.com/RUSHAB3979/neetcode-submissions-5qiqhw3o) | DSA practice, tracked in the open | `C++` |

---

## 📈 Activity

<p align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=RUSHAB3979&theme=tokyonight&hide_border=true&background=0D1117&ring=26D0CE&fire=26D0CE&currStreakLabel=26D0CE" alt="GitHub streak" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=RUSHAB3979&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=26D0CE&line=26D0CE&point=ffffff&area=true" alt="Contribution activity" width="100%" />
</p>

<div align="center">
  <img src="https://raw.githubusercontent.com/RUSHAB3979/RUSHAB3979/output/github-contribution-grid-snake.svg" alt="Contribution snake" />
</div>

---

<p align="center">
  <b>Open to backend and distributed-systems roles.</b><br/>
  <sub>Chess, the gym, and systems that fail loudly rather than quietly.</sub>
</p>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:26d0ce,100:1a2980&height=120&section=footer" width="100%" alt="" />
