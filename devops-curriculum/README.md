# Cloud & DevOps Curriculum

A free, curated resource list to go with **"Every DevOps Concept Explained"** ~ a ~14 minute walkthrough of every major DevOps concept, from culture down to AI infrastructure, in the order they actually show up in a real engineering workflow.

This isn't alphabetical or tool-by-tool. It follows one pipeline: **culture → Linux/networking → system design → cloud → Git → CI/CD → Docker → Kubernetes → DevSecOps → IaC → GitOps → observability → AI infrastructure.** Each concept exists because the one before it hit a limit. Learn them in this order.

Each section below has:
- **Topics** ~ what to actually know, not just recognize.
- **Resources** ~ free docs and courses to learn it, plus (where one exists) an interactive game or sandbox to *practice* it instead of just reading about it.

## 📚 Table of Contents

- [Free Hands-On Labs](#free-hands-on-labs)
- [1. DevOps Culture & Roles](#1-devops-culture--roles)
- [2. Linux, Windows & Scripting](#2-linux-windows--scripting)
- [3. Networking](#3-networking)
- [4. System Design](#4-system-design)
- [5. Cloud](#5-cloud)
- [6. Git Workflows](#6-git-workflows)
- [7. CI/CD](#7-cicd)
- [8. Docker](#8-docker)
- [9. Kubernetes](#9-kubernetes)
- [10. DevSecOps](#10-devsecops)
- [11. Infrastructure as Code](#11-infrastructure-as-code)
- [12. GitOps](#12-gitops)
- [13. Observability](#13-observability)
- [14. AI Infrastructure & AIOps](#14-ai-infrastructure--aiops)
- [15. End-to-End Project](#15-end-to-end-project)
- [Suggested Order](#suggested-order)

---

## Free Hands-On Labs

Before you go section by section, know this exists: free, browser-based labs that cover almost every topic below, with no local setup or cloud bills.

- 🎮 [KodeKloud Studio](https://kodekloud.com/studio/) ~ free hands-on labs across Linux, Git, Docker, Kubernetes, Terraform, CI/CD, Prometheus/Grafana, and more ~ one place to practice almost every topic in this curriculum
- 🏆 [100 Days of DevOps](https://kodekloud.com/100-days-of-devops) ~ 100 real-world tasks across 8 tool categories (Git, Docker, Kubernetes, Linux, CI/CD, IaC), live environments with automated validation, ends with a verified badge + portfolio
- 🏆 [100 Days of MLOps](https://kodekloud.com/100-days-of-mlops) ~ 100 tasks across 12 tool categories (DVC, MLflow, Feast, Argo Workflows, Kubernetes, Evidently), progressing beginner → advanced (drift-triggered retraining, GitOps, GPU training), also ends with a verified badge

**Progression**: do the topic-specific labs as you hit each section below, then use the 100-day challenges to string it all together ~ DevOps first, MLOps once you reach [§14 AI Infrastructure & AIOps](#14-ai-infrastructure--aiops).

---

## 1. DevOps Culture & Roles

**Topics**
- Why Dev/Ops silos slow releases down and cause friction
- Core culture: automation over manual work, small frequent releases, blameless postmortems
- Roles and how they overlap: DevOps Engineer, SRE, Platform Engineer, Cloud Architect

**Resources**
- 📖 [Google SRE Books](https://sre.google/books/) ~ free, full text: *Site Reliability Engineering*, *The SRE Workbook*, *Building Secure and Reliable Systems*
- 📖 [Atlassian: DevOps Frameworks & DORA Metrics](https://www.atlassian.com/devops/frameworks) ~ culture, CALMS, team topologies
- 📖 [DORA ~ Get Better at Getting Better](https://dora.dev/) ~ the research behind "what makes high-performing teams"

## 2. Linux, Windows & Scripting

**Topics**
- Terminal navigation, processes (`top`, `ps`), disk (`df`, `du`), logs (`/var/log`), permissions, `systemctl`
- Windows Server / PowerShell for Azure-heavy environments
- Bash first, then Python ~ script the second time you do something manually

**Resources ~ Linux (play, don't just read)**
- 🎮 [OverTheWire: Bandit](https://overthewire.org/wargames/bandit/) ~ the classic beginner wargame; SSH into a server, find the password, level up (34 levels)
- 🎮 [SadServers](https://sadservers.com/scenarios) ~ real broken Linux servers in a browser, capture-the-flag style troubleshooting scenarios
- 🎮 [cmdchallenge](https://cmdchallenge.com/) ~ one-line bash challenges, runs in a sandboxed container in your browser
- 🎮 [Linux Journey](https://linuxjourney.com/) ~ free interactive lessons + in-browser terminal, no signup

**Resources ~ Windows / PowerShell**
- 🎮 [PSKoans](https://github.com/vexx32/PSKoans) ~ learn PowerShell by making failing Pester tests pass, koan-style
- 📖 [Microsoft Learn: PowerShell](https://learn.microsoft.com/en-us/training/powershell/) ~ free structured learning paths
- 📖 [Microsoft Learn: Windows Server fundamentals](https://learn.microsoft.com/en-us/training/windowsserver/) ~ for Azure-heavy environments

**Resources ~ Scripting**
- 📖 [explainshell.com](https://explainshell.com/) ~ paste any shell command, get every flag explained
- 🎮 [cmdchallenge](https://cmdchallenge.com/) (same as above) doubles as bash scripting practice

## 3. Networking

**Topics**
- DNS ~ how a name becomes an IP
- IPs, subnets, CIDR ~ split `10.0.0.0/16` without a calculator
- TCP vs UDP, ports and what's actually listening
- Firewalls / security groups, load balancers
- The 4-question debug flow: can I resolve the name → reach the IP → is the port open → is the service listening
- Layer 4 vs Layer 7 load balancing

**Resources**
- 🎮 [SubnettingPractice.com](https://subnettingpractice.com/) ~ the most extensive free subnetting drill site
- 🎮 [Subnetting.net](https://www.subnetting.net/Start.aspx) ~ subnetting as a timed practice game
- 🎮 [CIDRtools IPv4 Subnetting Quiz](https://cidrtools.net/tools/quiz/) ~ Easy/Medium/Hard difficulty levels
- 🎮 [SadServers ~ Networking scenarios](https://sadservers.com/scenarios) ~ DNS, ports, and firewall troubleshooting on real boxes
- 📺 [Learn Networking In 25 MINUTES ~ Networking Fundamentals + Cloud Networking Concepts](https://youtu.be/bEFAFHIahXk)
- 📺 [COMPLETE APIs Crash Course In 14 Minutes (w/ free project)](https://www.youtube.com/watch?v=UXA8MJUWUqU)

## 4. System Design

**Topics**
- Scalability: vertical vs horizontal scaling, stateless vs stateful services
- Availability & reliability: redundancy, failover, replication, single points of failure
- Consistency models: CAP theorem, strong vs eventual consistency
- Load balancing strategies (covered from the networking angle in §3, revisited here at the system level)
- Caching: where to cache (client, CDN, app, DB), cache invalidation, write-through vs write-back
- Database scaling: sharding, replication, read replicas, SQL vs NoSQL trade-offs
- Message queues & async processing: decoupling producers/consumers with Kafka/RabbitMQ/SQS
- Rate limiting and backpressure
- Back-of-the-envelope estimation ~ sizing a system (traffic, storage, bandwidth) before you design it

**Resources**
- 📺 [System Design Concepts CRASH COURSE For Beginners ~ End-To-End DevOps + AIOps Project, Part 1](https://youtu.be/ihQQJuKHY7A)
- 📺 [Gaurav Sen ~ System Design playlist](https://www.youtube.com/playlist?list=PLMCXHnjXnTnvo6alSjVkgxV-VH6EPyvoX) ~ free, 25+ videos, case studies on Netflix, Tinder, WhatsApp, Instagram, Cassandra
- 📖 [donnemartin/system-design-primer](https://github.com/donnemartin/system-design-primer) ~ the original free, open-source primer; includes Anki flashcards and worked interview solutions
- 📖 [binhnguyennus/awesome-scalability](https://github.com/binhnguyennus/awesome-scalability) ~ patterns of scalable/reliable systems, real-world case studies (Netflix, Uber, Discord, Slack)
- 📖 [ashishps1/awesome-system-design-resources](https://github.com/ashishps1/awesome-system-design-resources) ~ curated resource list, same structure this README borrows from

## 5. Cloud

**Topics**
- Compute, storage, networking, IAM, managed databases ~ the 80% you'll touch daily
- The cloud is someone else's data center behind an API: same Linux/network concepts, cloud-specific names
- Pick one provider, go deep for ~3 months before touching a second
- Set a billing alert before you create anything

**Resources**
- 📖 [AWS Skill Builder](https://skillbuilder.aws/) ~ 600+ free digital courses direct from AWS
- 📖 [Microsoft Learn ~ Azure](https://learn.microsoft.com/en-us/training/azure/) ~ free, end-to-end, including full certification paths
- 📖 [Google Cloud Skills Boost](https://www.cloudskillsboost.google/) ~ free courses + monthly credit for labs
- 📺 [freeCodeCamp ~ AWS Certified Cloud Practitioner (free course)](https://www.freecodecamp.org/news/aws-certified-cloud-practitioner-certification-study-course-pass-the-exam/) ~ full exam-prep course, taught by Andrew Brown (ExamPro)

**Free Learning Paths ~ pick one provider**
- **AWS**: [Cloud Practitioner Essentials](https://explore.skillbuilder.aws/learn/course/external/view/elearning/134/aws-cloud-practitioner-essentials) (free course) + [Cloud Practitioner Exam Prep Plan](https://skillbuilder.aws/exam-prep/cloud-practitioner)
- **Azure**: [Azure Fundamentals learning path (4 parts)](https://learn.microsoft.com/en-us/training/paths/microsoft-azure-fundamentals-describe-cloud-concepts/) ~ free, hands-on, maps directly to the AZ-900 exam
- **GCP**: [Getting Started with Google Cloud](https://www.skills.google/paths/8) (free intro path) → [Associate Cloud Engineer path](https://www.cloudskillsboost.google/paths/11) once you're ready to go deeper
- **OCI**: [Become an OCI Foundations Associate (2025)](https://mylearn.oracle.com/ou/learning-path/become-an-oci-foundations-associate-2025/148056) ~ free, ~11+ hours, maps to the OCI Foundations Associate cert

## 6. Git Workflows

**Topics**
- Branch → commit → push → PR → review → merge to `main`
- Feature branching vs trunk-based development
- Small changes, merged often, always reviewed
- Git as the source of truth that later triggers CI/CD and GitOps

**Resources**
- 🎮 [Oh My Git!](https://ohmygit.org/) ~ open-source Git game that visualizes the repo's internal graph in real time as you play
- 🎮 [Learn Git Branching](https://learngitbranching.js.org/) ~ 50+ levels, animated branch diagrams, simulated terminal, no install
- 🎮 [git-game](https://github.com/git-game/git-game) ~ terminal game, 10 levels testing real git commands (see also [git-game-v2](https://github.com/git-game/git-game-v2) for advanced features)
- 📖 [GitHub Skills](https://skills.github.com/) ~ free, hands-on courses run as real GitHub repos (includes Introduction to GitHub, and CI/CD-flavored ones)

## 7. CI/CD

**Topics**
- CI: does this change install, lint, test, and build cleanly?
- CD: Continuous Delivery (human approves prod) vs Continuous Deployment (fully automatic)
- The pipeline shape: push → trigger → install → test → build → push artifact → deploy/approve
- Tools differ (GitHub Actions, GitLab CI, Jenkins), the pattern doesn't

**Resources**
- 📺 [CI/CD Crash Course For Beginners ~ Jenkins, GitHub Actions, GitLab](https://youtu.be/ixNNyLcWXX8)
- 📖 [GitHub Actions documentation](https://docs.github.com/en/actions) ~ build one real pipeline here: test, build, deploy
- 🎮 [KodeKloud Free Labs](https://kodekloud.com/studio/) ~ browser-based CI/CD and DevOps labs, no local setup

## 8. Docker

**Topics**
- The "it works on my machine" problem, and why containers fix it
- Dockerfile → build → image → run → container
- Containers share the host kernel ~ that's why they start in seconds, not minutes
- CI builds the image and pushes it to a registry (Docker Hub, ECR)

**Resources**
- 🎮 [Play with Docker](https://labs.play-with-docker.com/) ~ free browser-based Docker playground, no install
- 🎮 [KodeKloud ~ Docker free labs](https://kodekloud.com/studio/labs/docker) ~ hands-on labs in-browser
- 📖 [Docker Curriculum by prakhar1989](https://github.com/prakhar1989/docker-curriculum) ~ the tutorial most engineers cut their teeth on; build and deploy an image end to end

## 9. Kubernetes

**Topics**
- Declarative desired state: replicas, resources, ports ~ Kubernetes reconciles reality to match
- Pods, Deployments, Services, YAML manifests
- Most Kubernetes debugging is networking debugging (Service→Pod routing, DNS, Ingress)
- Use Kubernetes before you administer Kubernetes ~ deploy to a managed cluster (EKS/AKS/kind) first

**Resources**
- 📺 [The ONLY Kubernetes Course You'll Ever Need (2026) ~ Kubernetes For DevOps + AI, Part 1](https://youtu.be/H_a5DTKSEjY)
- 📺 [Kubernetes For AI: Zero To Hero ~ Ultimate Crash Course, Part 2](https://youtu.be/N9utcNfbCPM)
- 🎮 [Killercoda ~ Kubernetes Playgrounds](https://killercoda.com/playgrounds/scenario/kubernetes) ~ free in-browser cluster, single or multi-node
- 🎮 [Play with Kubernetes](https://labs.play-with-k8s.com/) ~ free browser-based K8s playground from Docker

## 10. DevSecOps

**Topics**
- Shift security left: catch issues while they're cheap to fix, not right before release
- Dependency scanning, secret scanning, static analysis, container image scanning
- A failed security scan blocks the pipeline exactly like a failed test
- Kubernetes security: RBAC, network policies, pod security standards, image scanning in the cluster

**Resources**
- 📖 [OWASP Top 10](https://owasp.org/www-project-top-ten/) ~ the vulnerability classes every scanner is looking for
- 📖 [Trivy documentation](https://trivy.dev/) ~ free, open-source scanner: container images, IaC, secrets, SBOMs, no usage limits
- 📖 [Gitleaks](https://github.com/gitleaks/gitleaks) ~ free secret-scanning tool, easy to drop into any pipeline
- 📖 [Snyk](https://snyk.io/) ~ free tier for dependency and container scanning with a web dashboard
- 📺 [Kubernetes Security ~ End-To-End DevOps + AIOps Project playlist](https://www.youtube.com/playlist?list=PLXkUFcIv0_b7rzZe0o_2-GOS2qn5-0OQy) ~ the DevSecOps/K8s security leg of the full project series (see [§15 End-to-End Project](#15-end-to-end-project) for the whole build)

## 11. Infrastructure as Code

**Topics**
- Infrastructure defined in files, applied with a command ~ not clicked into existence
- Repeatable (identical dev/stage/prod), reviewable (PRs), recoverable (re-apply in a new region)
- If it's not in code, it doesn't exist ~ console clicking is for exploring only

**Resources**
- 📖 [HashiCorp Developer ~ Terraform Tutorials](https://developer.hashicorp.com/terraform/tutorials) ~ official, hands-on, command-line tutorials across AWS/Azure/GCP
- 🎮 [KodeKloud ~ Terraform free labs](https://kodekloud.com/studio/) ~ browser-based Terraform practice

## 12. GitOps

**Topics**
- Traditional CI/CD pushes into the cluster (pipeline holds prod credentials); GitOps flips that
- CI builds/scans/pushes the image → updates a Git repo with desired state → a controller pulls and applies it
- Git becomes the single source of truth: every deploy is a commit, rollback is `git revert`
- The controller detects and reverts manual drift automatically

**Resources**
- 📺 [GitOps Crash Course For Beginners ~ ArgoCD & FluxCD](https://youtu.be/xRIre6L_gAo)
- 📖 [Argo CD documentation](https://argo-cd.readthedocs.io/)
- 📖 [Flux documentation](https://fluxcd.io/flux/)

## 13. Observability

**Topics**
- Three pillars: metrics (Prometheus/Grafana), logs, traces (a request's path across services)
- Dashboards nobody watches are decoration ~ the real skill is alerting on symptoms users feel
- SLOs ~ define a reliability target, measure against it

**Resources**
- 🎮 [play.grafana.org](https://play.grafana.org/) ~ Grafana Labs' public demo instance, explore real dashboards live
- 🎮 [KodeKloud ~ Prometheus & Grafana Playground](https://kodekloud.com/playgrounds/playground-prometheus-grafana) ~ free browser sandbox, build a dashboard and an alert
- 📖 [Prometheus ~ Overview docs](https://prometheus.io/docs/introduction/overview/)

**Certification**
- [Prometheus Certified Associate (PCA)](https://training.linuxfoundation.org/certification/prometheus-certified-associate/) ~ Linux Foundation/CNCF, 90-min proctored exam, no prerequisites, one free retake included. Discount via [ksug.ai](https://ksug.ai/promos): code **MM26CCAI** for 50% off. Codes rotate ~ verify at checkout.

## 14. AI Infrastructure & AIOps

**Topics**
- AI infrastructure: Kubernetes orchestrating GPU workloads, model weights as versioned artifacts, GPU-to-GPU networking
- MLOps: CI/CD extended with continuous training, dataset/model versioning, retraining pipelines
- AIOps: using AI to triage logs/metrics/alerts and speed up root-cause analysis
- Model hosting & serving: inference latency, throughput, GPU scaling

**Resources**
- 📺 [20+ FREE Courses To MASTER Cloud, DevOps & AI (2026)](https://youtu.be/SG1Lv12YUjU) ~ source for the course list below
- 📖 [NVIDIA GPU Operator docs](https://docs.nvidia.com/datacenter/cloud-native/gpu-operator/latest/index.html) ~ how GPUs get provisioned and managed inside Kubernetes
- For the full curriculum on each of these, see this repo's dedicated guides: [MLOps-Practice-Guide](../MLOps-Practice-Guide/), [AIOps-Practice-Guide](../AIOps-Practice-Guide/), [LLMOps-Practice-Guide](../LLMOps-Practice-Guide/)

**Courses ~ free-to-start, with a certification path attached**

Prices, promos, and free-access windows move fast ~ check each page before enrolling.

| Course | Level · Length | Get it free/cheap | Certifies you for |
|---|---|---|---|
| [AI Python for Beginners](https://www.deeplearning.ai/courses/ai-python-for-beginners) ~ DeepLearning.AI (Andrew Ng) | Beginner · ~11.5 hrs | Free to enroll ~ all videos + code examples. Certificate + graded assignments need Pro (no financial-aid tier; annual billing is cheapest). | ~ (skills course, no cert) |
| [AI Security](https://tryhackme.com/aisecurity) ~ TryHackMe | Medium · ~20 hrs, 25 labs | Free account covers a large chunk; full path needs Premium (~$126/yr, 20% off annual for students). Free vouchers surface via CTF events and school Classrooms. | AI Security (AI1) ~ 48-hr hands-on professional cert |
| [AI Infrastructure & Operations Fundamentals](https://www.coursera.org/learn/ai-infrastructure-operations-fundamentals) ~ NVIDIA (via Coursera) | Beginner · ~7–8 hrs, self-paced | Audit free on Coursera ~ full content, no cost. Apply for **Financial Aid** under the enroll button for a free certificate (~15-day approval). Only the exam (~$50–150) costs money. | NVIDIA-Certified Associate: AI Infrastructure & Operations (NCA-AIIO) |
| [Claude Code in Action](https://www.datacamp.com/courses/claude-code-in-action) ~ DataCamp | Intermediate · ~3–4 hrs | First chapter free, no card. Students get 3 months free via the GitHub Student Pack. Watch for DataCamp's Free Access Week (Jun/Nov). | ~ (skills course, no cert) |
| [Certified Kubernetes Administrator (CKA)](https://kodekloud.com/courses/cka-certification-course-certified-kubernetes-administrator) ~ KodeKloud (Mumshad Mannambeth) | ~25 hrs video + labs, 3 mock exams | Free account unlocks preview labs. On the exam itself, [ksug.ai](https://ksug.ai/promos) codes: **MM26CCAI** for 50% off, **MM26BUNAI** for 60% off bundles. Codes rotate ~ verify at checkout, don't stack. | Certified Kubernetes Administrator (CKA) ~ CNCF / Linux Foundation |
| [MLOps Zero to Hero](https://www.udemy.com/course/mlops-zero-to-hero/) ~ Udemy (Abhishek Veeramalla) | ~12 hrs | Udemy runs frequent discounts ~ wait for a sale rather than paying list price. Free lecture notes on [GitHub](https://github.com/iam-veeramalla/mlops-zero-to-hero). 30-day refund guarantee. | ~ (skills course, no cert) |
| [Microsoft Azure AI Fundamentals](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-900/) | Beginner | Prep via [skillupwithlevelup.com](https://skillupwithlevelup.com) ~ score 80%+ on the prep course to get a **free exam voucher**. | Microsoft Certified: Azure AI Fundamentals (AI-900) |
| [AWS Certified AI Practitioner](https://aws.amazon.com/certification/certified-ai-practitioner/) | Beginner | Work through the [AWS Skill Builder Exam Prep Plan](https://skillbuilder.aws/exam-prep/ai-practitioner), complete the challenges, and claim a **50% off exam voucher**. | AWS Certified AI Practitioner (AIF-C01) |
| [Databricks Certified Generative AI Engineer Associate](https://www.databricks.com/learn/certification/genai-engineer-associate) | ~ | Join the annual [Databricks Learning Festival](https://www.databricks.com/learn) (runs in summer, e.g. June–July) and complete one learning path for **50% off the exam**. | Databricks Certified Generative AI Engineer Associate |

**Which one to start with**
- New to code or AI → **AI Python for Beginners** ~ free, beginner-proof
- Security-minded → **TryHackMe AI Security** ~ one of the fastest-growing specializations, with a cert to prove it
- Infrastructure/ops background → **NVIDIA AI Infrastructure & Operations** ~ free to audit, points straight at NCA-AIIO
- Already coding, want to work with AI tools → **Claude Code in Action** ~ reliable AI-assisted dev workflows, not guesswork
- Chasing a Kubernetes job → **KodeKloud CKA** ~ still one of the highest-leverage DevOps certs on the market
- Making the DevOps → MLOps leap → **MLOps Zero to Hero** ~ the production skills that separate "trained a model" from "shipped one"

The move that compounds isn't finishing a course, it's stacking it into a credential: learn free/cheap, certify discounted, and go into the market with proof ~ not just a completion screen. Do the labs; that's the part that actually sticks.

---

## 15. End-to-End Project

**Topics**
- Wiring every concept above into one real, deployed system instead of isolated exercises
- Taking a project from code → CI/CD → container → Kubernetes → GitOps → observability → AIOps, end to end

**Resources**
- 📺 [End-To-End DevOps + AIOps Project ~ Complete Series (playlist)](https://www.youtube.com/playlist?list=PLXkUFcIv0_b7rzZe0o_2-GOS2qn5-0OQy) ~ the full build, including the Kubernetes security / DevSecOps leg referenced in [§10](#10-devsecops)

---

## Suggested Order

If you're starting from zero, go top to bottom exactly as listed above:

**Linux before Docker → one cloud before any cloud cert → Git before CI/CD → Docker before Kubernetes → deploy something before you monitor it.**

Each section exists because the one before it hit a limit ~ culture defines the problem, Linux/networking are the ground it runs on, system design is how you'd architect what you're about to build before you touch a cloud console, and cloud/Git/CI/CD/Docker/Kubernetes/DevSecOps are the delivery chain. IaC/GitOps/observability are how you operate what you shipped, and AI infrastructure/AIOps are the same fundamentals applied to the newest workload type. The end-to-end project (§15) is where you stop learning concepts in isolation and wire all of it together.
