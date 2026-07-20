<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24243e&height=220&section=header&text=Abhishek%20Musmade&fontSize=54&fontColor=ffffff&fontAlignY=40&desc=Software%20Engineer%20%7C%20Backend%20Development%20%7C%20Node.js&descAlignY=60&descColor=a0a0ff&animation=fadeIn&fontAlignX=50" />
  
  <br/>
  
  [![Typing SVG](https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=20&duration=2800&pause=1000&color=7B8CDE&center=true&vCenter=true&multiline=false&width=650&lines=Building+scalable+backend+systems;Node.js+%7C+Express.js+%7C+MongoDB+%7C+Redis;Clean+Code+%7C+SOLID+Principles](https://git.io/typing-svg)
  
  <br/>
  
  [![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishekmusmade-0582a7289)
  [![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Abhimusmade010)
  [![Profile Views](https://komarev.com/ghpvc/?username=Abhimusmade010&label=Profile+Views&color=7B8CDE&style=for-the-badge)](https://github.com/Abhimusmade010)
</div>

---

## ⚡ About Me
```yaml
name         : Abhishek Musmade
role         : Software Engineer · Backend Development
education    : B.E. (IT) @ Pune Institute of Computer Technology (2023-2027)

currently    :
  building   → FixIT (Hardware/Software Maintenance Platform)
  learning   → Advanced System Design · AWS Ecosystem

philosophy   : Clean Code → SOLID Principles → Maintainable Systems

strengths    :
  - Core backend layers: REST APIs, JWT Auth, RBAC, request validation
  - Optimizing application performance and ensuring data consistency
  - Object-Oriented Programming (OOP) and Design Patterns

highlights   :
  cgpa       : 9.34
  dsa        : 500+ algorithmic problems solved
  achieved   : 99.21 Percentile in MHT-CET (District Rank 5)




**Core Architecture Decisions:**
  > **Storage** — Integrated AWS S3 using presigned URLs for secure image/video uploads.
  > **Infrastructure** — Deployed resilient backend on AWS EC2 using PM2 for process management and Nginx as a reverse proxy.

  **What it does:**
  - 🔐 JWT authentication & RBAC integration
  - 📊 Secure REST APIs with search, filtering, and pagination
  - ⏱️ Node-Cron auto-escalation reminders
  - 📧 Nodemailer email notifications & CSV export via excelJS

  ![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)
  ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white)
  ![AWS S3](https://img.shields.io/badge/AWS_S3-232F3E?style=flat-square&logo=amazon-aws&logoColor=white)
  ![Redis](https://img.shields.io/badge/Redis-DD0031?style=flat-square&logo=redis&logoColor=white)
</td>
<td width="50%" valign="top">
  ### 🏨 [FindYourStay](#)
  **Hotel Booking Engine**
  A highly optimized booking platform ensuring data consistency through transactional operations and caching layers.

  **Core Architecture Decisions:**
  > **Consistency** — Engineered approval-based booking lifecycles utilizing MongoDB Transactions for atomic operations.
  > **Performance** — Integrated Redis caching to significantly improve hotel API response times.

  **What it does:**
  - 🔑 RBAC supporting Customers, Hotel Admins, and Super Admins
  - 🛡️ JWT based stateless authentication
  - 🖼️ Cloudinary integration for optimized media storage and delivery
  - ⚡ High-performance REST APIs

  ![Express.js](https://img.shields.io/badge/Express.js-000000?style=flat-square&logo=express&logoColor=white)
  ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=flat-square&logo=mongodb&logoColor=white)
  ![Redis](https://img.shields.io/badge/Redis-DD0031?style=flat-square&logo=redis&logoColor=white)
  ![JWT](https://img.shields.io/badge/JWT-black?style=flat-square&logo=JSON%20web%20tokens)




name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
