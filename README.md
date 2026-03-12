<div align="center">

<svg width="1280" height="320" viewBox="0 0 1280 320" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <!-- Black background always -->
    <style>
      @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@700&amp;family=Rajdhani:wght@700&amp;display=swap');
    </style>

    <!-- Gradient for name text -->
    <linearGradient id="nameGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:#ffffff"/>
      <stop offset="50%" style="stop-color:#00d4ff"/>
      <stop offset="100%" style="stop-color:#7c3aed"/>
      <animateTransform attributeName="gradientTransform" type="translate" from="-1 0" to="1 0" dur="3s" repeatCount="indefinite"/>
    </linearGradient>

    <!-- Glow filter -->
    <filter id="glow" x="-20%" y="-20%" width="140%" height="140%">
      <feGaussianBlur stdDeviation="4" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Strong glow for name -->
    <filter id="nameGlow" x="-10%" y="-30%" width="120%" height="160%">
      <feGaussianBlur stdDeviation="8" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Cyan glow -->
    <filter id="cyanGlow">
      <feGaussianBlur stdDeviation="3" result="coloredBlur"/>
      <feMerge>
        <feMergeNode in="coloredBlur"/>
        <feMergeNode in="SourceGraphic"/>
      </feMerge>
    </filter>

    <!-- Gradient for top line -->
    <linearGradient id="lineGrad1" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:transparent"/>
      <stop offset="30%" style="stop-color:#7c3aed"/>
      <stop offset="50%" style="stop-color:#00d4ff"/>
      <stop offset="70%" style="stop-color:#7c3aed"/>
      <stop offset="100%" style="stop-color:transparent"/>
    </linearGradient>

    <!-- Gradient for bottom line -->
    <linearGradient id="lineGrad2" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:transparent"/>
      <stop offset="30%" style="stop-color:#00d4ff"/>
      <stop offset="50%" style="stop-color:#7c3aed"/>
      <stop offset="70%" style="stop-color:#00d4ff"/>
      <stop offset="100%" style="stop-color:transparent"/>
    </linearGradient>

    <!-- Underline gradient -->
    <linearGradient id="underlineGrad" x1="0%" y1="0%" x2="100%" y2="0%">
      <stop offset="0%" style="stop-color:transparent"/>
      <stop offset="50%" style="stop-color:#00d4ff"/>
      <stop offset="100%" style="stop-color:transparent"/>
    </linearGradient>

    <!-- Orb gradient purple -->
    <radialGradient id="orb1" cx="50%" cy="50%" r="50%">
      <stop offset="0%" style="stop-color:#7c3aed;stop-opacity:0.3"/>
      <stop offset="100%" style="stop-color:#7c3aed;stop-opacity:0"/>
    </radialGradient>

    <!-- Orb gradient cyan -->
    <radialGradient id="orb2" cx="50%" cy="50%" r="50%">
      <stop offset="0%" style="stop-color:#00d4ff;stop-opacity:0.2"/>
      <stop offset="100%" style="stop-color:#00d4ff;stop-opacity:0"/>
    </radialGradient>

    <!-- Clip path -->
    <clipPath id="svgClip">
      <rect width="1280" height="320"/>
    </clipPath>
  </defs>

  <!-- HARDCODED BLACK BACKGROUND — never changes -->
  <rect width="1280" height="320" fill="#000000"/>

  <!-- Subtle grid lines -->
  <g opacity="0.04" clip-path="url(#svgClip)">
    <!-- Vertical lines -->
    <line x1="60" y1="0" x2="60" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="120" y1="0" x2="120" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="180" y1="0" x2="180" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="240" y1="0" x2="240" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="300" y1="0" x2="300" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="360" y1="0" x2="360" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="420" y1="0" x2="420" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="480" y1="0" x2="480" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="540" y1="0" x2="540" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="600" y1="0" x2="600" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="660" y1="0" x2="660" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="720" y1="0" x2="720" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="780" y1="0" x2="780" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="840" y1="0" x2="840" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="900" y1="0" x2="900" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="960" y1="0" x2="960" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="1020" y1="0" x2="1020" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="1080" y1="0" x2="1080" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="1140" y1="0" x2="1140" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <line x1="1200" y1="0" x2="1200" y2="320" stroke="#00d4ff" stroke-width="1"/>
    <!-- Horizontal lines -->
    <line x1="0" y1="60" x2="1280" y2="60" stroke="#00d4ff" stroke-width="1"/>
    <line x1="0" y1="120" x2="1280" y2="120" stroke="#00d4ff" stroke-width="1"/>
    <line x1="0" y1="180" x2="1280" y2="180" stroke="#00d4ff" stroke-width="1"/>
    <line x1="0" y1="240" x2="1280" y2="240" stroke="#00d4ff" stroke-width="1"/>
    <line x1="0" y1="300" x2="1280" y2="300" stroke="#00d4ff" stroke-width="1"/>
  </g>

  <!-- Animated glowing orbs -->
  <ellipse cx="0" cy="80" rx="300" ry="300" fill="url(#orb1)" clip-path="url(#svgClip)">
    <animate attributeName="opacity" values="0.6;1;0.6" dur="4s" repeatCount="indefinite"/>
  </ellipse>
  <ellipse cx="1280" cy="260" rx="280" ry="280" fill="url(#orb2)" clip-path="url(#svgClip)">
    <animate attributeName="opacity" values="0.5;1;0.5" dur="5s" repeatCount="indefinite"/>
  </ellipse>
  <ellipse cx="900" cy="160" rx="180" ry="180" fill="url(#orb1)" clip-path="url(#svgClip)">
    <animate attributeName="opacity" values="0.3;0.7;0.3" dur="6s" repeatCount="indefinite"/>
  </ellipse>

  <!-- Top border line animated -->
  <rect x="0" y="0" width="1280" height="2" fill="url(#lineGrad1)">
    <animate attributeName="opacity" values="0.6;1;0.6" dur="2s" repeatCount="indefinite"/>
  </rect>

  <!-- Bottom border line animated -->
  <rect x="0" y="318" width="1280" height="2" fill="url(#lineGrad2)">
    <animate attributeName="opacity" values="0.6;1;0.6" dur="2.5s" repeatCount="indefinite"/>
  </rect>

  <!-- Corner brackets — TL -->
  <path d="M20,20 L20,55 M20,20 L55,20" stroke="#00d4ff" stroke-width="2" fill="none" opacity="0.6">
    <animate attributeName="opacity" values="0.4;0.9;0.4" dur="3s" repeatCount="indefinite"/>
  </path>
  <!-- TR -->
  <path d="M1260,20 L1260,55 M1260,20 L1225,20" stroke="#00d4ff" stroke-width="2" fill="none" opacity="0.6">
    <animate attributeName="opacity" values="0.4;0.9;0.4" dur="3.5s" repeatCount="indefinite"/>
  </path>
  <!-- BL -->
  <path d="M20,300 L20,265 M20,300 L55,300" stroke="#7c3aed" stroke-width="2" fill="none" opacity="0.6">
    <animate attributeName="opacity" values="0.4;0.9;0.4" dur="4s" repeatCount="indefinite"/>
  </path>
  <!-- BR -->
  <path d="M1260,300 L1260,265 M1260,300 L1225,300" stroke="#7c3aed" stroke-width="2" fill="none" opacity="0.6">
    <animate attributeName="opacity" values="0.4;0.9;0.4" dur="2.8s" repeatCount="indefinite"/>
  </path>

  <!-- Floating particles -->
  <circle cx="100" cy="50" r="2" fill="#00d4ff" opacity="0.5">
    <animate attributeName="cy" values="50;30;50" dur="4s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.2;0.8;0.2" dur="4s" repeatCount="indefinite"/>
  </circle>
  <circle cx="300" cy="270" r="1.5" fill="#7c3aed" opacity="0.5">
    <animate attributeName="cy" values="270;250;270" dur="5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.3;0.9;0.3" dur="5s" repeatCount="indefinite"/>
  </circle>
  <circle cx="900" cy="40" r="2" fill="#7c3aed" opacity="0.4">
    <animate attributeName="cy" values="40;60;40" dur="3.5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.2;0.7;0.2" dur="3.5s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1100" cy="280" r="1.5" fill="#00d4ff" opacity="0.5">
    <animate attributeName="cy" values="280;260;280" dur="4.5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.3;0.8;0.3" dur="4.5s" repeatCount="indefinite"/>
  </circle>
  <circle cx="650" cy="30" r="1" fill="#00d4ff" opacity="0.4">
    <animate attributeName="cy" values="30;50;30" dur="6s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.2;0.6;0.2" dur="6s" repeatCount="indefinite"/>
  </circle>
  <circle cx="200" cy="160" r="1.5" fill="#7c3aed" opacity="0.3">
    <animate attributeName="cx" values="200;220;200" dur="7s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.1;0.5;0.1" dur="7s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1050" cy="140" r="1.5" fill="#00d4ff" opacity="0.3">
    <animate attributeName="cx" values="1050;1030;1050" dur="5.5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.1;0.5;0.1" dur="5.5s" repeatCount="indefinite"/>
  </circle>

  <!-- Scanning line effect -->
  <rect x="0" y="0" width="1280" height="1" fill="rgba(0,212,255,0.15)" clip-path="url(#svgClip)">
    <animate attributeName="y" values="-2;322;-2" dur="4s" repeatCount="indefinite"/>
  </rect>

  <!-- Top bracket label -->
  <text x="640" y="68" text-anchor="middle" font-family="'Courier New', monospace" font-size="12"
        font-weight="700" fill="#00d4ff" letter-spacing="8" opacity="0.7">
    ⚡ &lt; DEVOPS ENGINEER /&gt; ⚡
    <animate attributeName="opacity" values="0.5;0.9;0.5" dur="2s" repeatCount="indefinite"/>
  </text>

  <!-- Main Name — Prakhar Shukla with glow -->
  <text x="640" y="178" text-anchor="middle"
        font-family="'Segoe UI', 'Arial Black', sans-serif"
        font-size="80" font-weight="900"
        letter-spacing="6"
        fill="url(#nameGrad)"
        filter="url(#nameGlow)">
    Prakhar Shukla
  </text>

  <!-- Name shimmer overlay -->
  <text x="640" y="178" text-anchor="middle"
        font-family="'Segoe UI', 'Arial Black', sans-serif"
        font-size="80" font-weight="900"
        letter-spacing="6"
        fill="white" opacity="0">
    Prakhar Shukla
    <animate attributeName="opacity" values="0;0.15;0;0;0" dur="3s" repeatCount="indefinite"/>
  </text>

  <!-- Underline below name -->
  <rect x="340" y="190" width="600" height="1.5" fill="url(#underlineGrad)">
    <animate attributeName="width" values="0;600;600" dur="1.5s" begin="0.5s" fill="freeze"/>
    <animate attributeName="x" values="640;340;340" dur="1.5s" begin="0.5s" fill="freeze"/>
  </rect>

  <!-- Description line -->
  <text x="640" y="235" text-anchor="middle"
        font-family="'Courier New', monospace"
        font-size="15" font-weight="600"
        letter-spacing="4"
        fill="#00d4ff"
        filter="url(#cyanGlow)"
        opacity="0.85">
    Cloud
    <animate attributeName="opacity" values="0.7;1;0.7" dur="3s" repeatCount="indefinite"/>
  </text>
  <text x="640" y="235" text-anchor="middle"
        font-family="'Courier New', monospace"
        font-size="15" font-weight="600"
        letter-spacing="4"
        fill="#00d4ff"
        opacity="0.85">
    Cloud  |  Automation  |  Ex HCL
  </text>

  <!-- Separator dots with pulse -->
  <circle cx="590" cy="231" r="2.5" fill="#7c3aed">
    <animate attributeName="r" values="2;3.5;2" dur="2s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.5;1;0.5" dur="2s" repeatCount="indefinite"/>
  </circle>
  <circle cx="690" cy="231" r="2.5" fill="#7c3aed">
    <animate attributeName="r" values="2;3.5;2" dur="2.5s" repeatCount="indefinite"/>
    <animate attributeName="opacity" values="0.5;1;0.5" dur="2.5s" repeatCount="indefinite"/>
  </circle>

  <!-- Side decorative dots left -->
  <circle cx="80" cy="140" r="3" fill="#00d4ff" opacity="0.4">
    <animate attributeName="opacity" values="0.2;0.7;0.2" dur="2s" repeatCount="indefinite"/>
  </circle>
  <circle cx="80" cy="160" r="4" fill="#7c3aed" opacity="0.5">
    <animate attributeName="opacity" values="0.3;0.8;0.3" dur="2.5s" repeatCount="indefinite"/>
  </circle>
  <circle cx="80" cy="180" r="3" fill="#00d4ff" opacity="0.4">
    <animate attributeName="opacity" values="0.2;0.7;0.2" dur="3s" repeatCount="indefinite"/>
  </circle>

  <!-- Side decorative dots right -->
  <circle cx="1200" cy="140" r="3" fill="#00d4ff" opacity="0.4">
    <animate attributeName="opacity" values="0.2;0.7;0.2" dur="2.2s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1200" cy="160" r="4" fill="#7c3aed" opacity="0.5">
    <animate attributeName="opacity" values="0.3;0.8;0.3" dur="2.7s" repeatCount="indefinite"/>
  </circle>
  <circle cx="1200" cy="180" r="3" fill="#00d4ff" opacity="0.4">
    <animate attributeName="opacity" values="0.2;0.7;0.2" dur="3.2s" repeatCount="indefinite"/>
  </circle>

  <!-- Bottom status text -->
  <text x="640" y="285" text-anchor="middle"
        font-family="'Courier New', monospace"
        font-size="11" fill="#7c3aed" letter-spacing="3" opacity="0.6">
    ● SYSTEM ONLINE — ALWAYS BUILDING 🚀
    <animate attributeName="opacity" values="0.4;0.8;0.4" dur="1.5s" repeatCount="indefinite"/>
  </text>

</svg>

[![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=18&duration=3000&pause=800&color=00D4FF&background=000000&center=true&vCenter=true&multiline=false&repeat=true&width=435&height=45&lines=%24+echo+%22Automating...%22+%F0%9F%9A%80;%24+kubectl+get+pods+--all-namespaces;%24+terraform+apply+--auto-approve+%E2%9C%85;%24+docker+compose+up+-d+%7C%7C+Deployed!;%24+git+push+origin+main)](https://git.io/typing-svg)

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/prakhar-shukla-267025191)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:prakharshuklatech@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/PrakharShukla001)
[![Profile Views](https://komarev.com/ghpvc/?username=PrakharShukla001&style=for-the-badge&color=00d4ff&label=PROFILE+VIEWS)](https://github.com/PrakharShukla001)

</div>

<br/>

---

## 🌌 About Me

<div align="center">

<img src="https://raw.githubusercontent.com/devSouvik/devSouvik/master/gif3.gif" width="340" alt="Coding GIF"/>

</div>

<br/>

<div align="center">

```bash
╔═══════════════════════════════════════════════════╗
║         ░▒▓  SYSTEM BOOT SEQUENCE  ▓▒░            ║
╠═══════════════════════════════════════════════════╣
║                                                   ║
║   $ whoami          ▶   Prakhar Shukla            ║
║   $ cat role        ▶   DevOps Engineer [ACTIVE]  ║
║   $ cat past        ▶   Network Eng @ HCL         ║
║   $ curl location   ▶   Lucknow, India 🇮🇳         ║
║   $ uptime          ▶   Always building 🚀       ║
║                                                   ║
║   $ systemctl status passion                      ║
║   ▶  ● passion.service — RUNNING ✅              ║
║                                                   ║
╚═══════════════════════════════════════════════════╝
```

</div>

<br/>

<div align="center">

| ⚡ | Status | 🔍 Detail |
|---|--------|-----------|
| 🔭 | Current Role | DevOps Engineer Intern — pipelines & infra |
| 🏢 | Past Experience | Network Engineer @ HCL Technologies |
| 🌱 | Currently Learning | Kubernetes · AWS · Terraform · CI/CD |
| 🤝 | Open To Collaborate | DevOps Automation · Cloud · Containers |
| 🆘 | Seeking Help With | Advanced K8s · Cloud Architecture |
| 💬 | Ask Me About | Linux · Git · CI/CD · Docker · DevOps |
| ⚡ | Fun Fact | I automate anything that dares to repeat 🚀 |

</div>

---

## 💻 Tech Stack

### 🖥️ Languages
![Apache Groovy](https://img.shields.io/badge/Apache%20Groovy-4298B8.svg?style=for-the-badge&logo=Apache+Groovy&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Bash Script](https://img.shields.io/badge/bash-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![PowerShell](https://img.shields.io/badge/PowerShell-%235391FE.svg?style=for-the-badge&logo=powershell&logoColor=white)
![Windows Terminal](https://img.shields.io/badge/Windows%20Terminal-%234D4D4D.svg?style=for-the-badge&logo=windows-terminal&logoColor=white)

### ☁️ Cloud Platforms
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-%230072C6.svg?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Google Cloud](https://img.shields.io/badge/GCP-%234285F4.svg?style=for-the-badge&logo=google-cloud&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=for-the-badge&logo=oracle&logoColor=white)
![Alibaba Cloud](https://img.shields.io/badge/Alibaba%20Cloud-%23FF6701.svg?style=for-the-badge&logo=alibabacloud&logoColor=white)
![Cloudflare](https://img.shields.io/badge/Cloudflare-F38020?style=for-the-badge&logo=Cloudflare&logoColor=white)

### 🛠️ DevOps & Infrastructure
![Docker](https://img.shields.io/badge/Docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-%232C5263.svg?style=for-the-badge&logo=jenkins&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=for-the-badge&logo=Prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)

### 🗄️ Servers & Databases
![Nginx](https://img.shields.io/badge/Nginx-%23009639.svg?style=for-the-badge&logo=nginx&logoColor=white)
![Apache](https://img.shields.io/badge/Apache-%23D42029.svg?style=for-the-badge&logo=apache&logoColor=white)
![Apache Tomcat](https://img.shields.io/badge/Tomcat-%23F8DC75.svg?style=for-the-badge&logo=apache-tomcat&logoColor=black)
![Apache Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1.svg?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-%23DD0031.svg?style=for-the-badge&logo=redis&logoColor=white)
![Anaconda](https://img.shields.io/badge/Anaconda-%2344A833.svg?style=for-the-badge&logo=anaconda&logoColor=white)

### 🔧 VCS & Collaboration
![Git](https://img.shields.io/badge/Git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)
![GitLab](https://img.shields.io/badge/GitLab-%23181717.svg?style=for-the-badge&logo=gitlab&logoColor=white)
![Gitpod](https://img.shields.io/badge/Gitpod-f06611.svg?style=for-the-badge&logo=gitpod&logoColor=white)
![Jira](https://img.shields.io/badge/Jira-%230A0FFF.svg?style=for-the-badge&logo=jira&logoColor=white)

### 🎨 Design
![Canva](https://img.shields.io/badge/Canva-%2300C4CC.svg?style=for-the-badge&logo=Canva&logoColor=white)
![Adobe](https://img.shields.io/badge/Adobe-%23FF0000.svg?style=for-the-badge&logo=adobe&logoColor=white)
![Adobe Premiere Pro](https://img.shields.io/badge/Premiere%20Pro-9999FF.svg?style=for-the-badge&logo=Adobe%20Premiere%20Pro&logoColor=white)
![Adobe Lightroom](https://img.shields.io/badge/Lightroom-31A8FF.svg?style=for-the-badge&logo=Adobe%20Lightroom&logoColor=white)

---

## 📊 GitHub Stats

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=PrakharShukla001&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=false&show_icons=true&rank_icon=github" height="180"/>
&nbsp;&nbsp;
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=PrakharShukla001&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=false&layout=donut" height="180"/>

</div>

<div align="center">

![Streak](https://nirzak-streak-stats.vercel.app/?user=PrakharShukla001&theme=tokyonight&hide_border=true&fire=00d4ff&ring=7c3aed&currStreakLabel=00d4ff)

</div>

---

## 📈 Contribution Graph

<div align="center">

[![Prakhar's github activity graph](https://github-readme-activity-graph.vercel.app/graph?username=PrakharShukla001&theme=tokyo-night&hide_border=true&area=true&color=00d4ff&line=7c3aed&point=ffffff)](https://github.com/ashutosh00710/github-readme-activity-graph)

</div>

---

## ✍️ Random Dev Quote

<div align="center">

![Quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight)

</div>

---

## 🐍 Contribution Snake

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/PrakharShukla001/PrakharShukla001/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/PrakharShukla001/PrakharShukla001/output/github-snake.svg" />
  <img alt="github-snake" src="https://raw.githubusercontent.com/PrakharShukla001/PrakharShukla001/output/github-snake-dark.svg" />
</picture>

</div>

---

<div align="center">

[![](https://visitcount.itsvg.in/api?id=PrakharShukla001&icon=2&color=1)](https://visitcount.itsvg.in)

*💡 Proudly automating everything that moves — one pipeline at a time.*

![footer](https://capsule-render.vercel.app/api?type=waving&color=0:7c3aed,50:00d4ff,100:000000&height=120&section=footer)

</div>
