# Toolkit: Claude Code + Spring Boot + Spring AI

Preparation and prerequisites for the hands-on training.

## What the course covers

### Claude Code

The agentic loop and context window &middot; settings &middot; `CLAUDE.md` &middot; memory &middot; hooks &middot; commands &middot; skills
&middot; plugins &middot; tools &middot; sub-agents &middot; MCP servers

### Spring Boot 4.1

Dependency injection, beans, and components &middot; JPA and JDBC integration &middot; controllers and REST endpoints &middot; exception
handling and validation &middot; DTOs and request/response mapping

### Spring AI 2.0

`ChatClient` and chat models &middot; prompts and prompt templates &middot; structured output &middot; tool / function calling &middot;
embeddings and vector stores &middot; retrieval-augmented generation (RAG) &middot; chat memory &middot; the MCP server and client starters
(`@McpTool`, `@McpResource`) &middot; observability

## Goal

Every participant builds their **own MCP server** with Spring Boot + Spring AI and connects it to Claude Code, giving the assistant
controlled access to internal applications and databases. The database used in class is **Oracle**, run locally through **Docker**. The
project is tracked on **GitHub**.

## Baseline versions used by the instructor

| Component       | Version                                  | Notes                                                                   |
|:----------------|:-----------------------------------------|:------------------------------------------------------------------------|
| JDK             | BellSoft Liberica 25 LTS                 | free, 100% open-source OpenJDK, supported to 2033                       |
| Spring Boot     | 4.1.x                                    | latest, from Spring Initializr                                          |
| Spring AI       | 2.0.x                                    | needs Boot 4.1 + Framework 7; `@McpTool` API; Streamable-HTTP transport |
| Maven           | 3.9.x (optional)                         | generated Spring Boot projects include the Maven Wrapper (`mvnw`)       |
| Node.js         | 24 LTS                                   | for npm / npx-based MCP servers and tooling                             |
| Git             | latest (2.55.x or newer)                 | Claude Code uses Git Bash on Windows                                    |
| Docker Desktop  | latest                                   | Oracle database and MCP containers                                      |
| Oracle Database | `gvenzl/oracle-free:23-slim` (23ai Free) | swap the tag if a specific version is required                          |
| Claude Code     | latest                                   | native installer                                                        |
| IntelliJ IDEA   | Ultimate (instructor's IDE)              | participants free to choose any IDE                                     |

> Complete **Sections 1 to 3** before day 1. The Appendix at the end lets you self-verify.

---

## 1. Machine specifications

Assume a vanilla laptop. The heaviest load is the Oracle container plus an IDE plus Claude Code sessions running together.

| Resource         | Minimum                                                                                                                                 | Recommended        | Why                                                                                                 |
|:-----------------|:----------------------------------------------------------------------------------------------------------------------------------------|:-------------------|:----------------------------------------------------------------------------------------------------|
| Operating system | Windows 11 64-bit, macOS 13 Ventura, or 64-bit Linux (Ubuntu 22.04+)                                                                    | Latest patch level | Docker Desktop and Claude Code support all three                                                    |
| CPU              | 4 physical cores                                                                                                                        | 8 cores            | Oracle Free in Docker plus IDE indexing plus build                                                  |
| RAM              | 16 GB                                                                                                                                   | 32 GB              | Oracle Free container alone wants about 2 GB; add Docker Desktop, IDE, browser, and Claude Code     |
| Storage (free)   | 50 GB on SSD                                                                                                                            | 100 GB on SSD      | Oracle image 2 to 9 GB, Docker layers, `~/.m2` repository, JDK, IDE, Node modules                   |
| Virtualization   | Enabled in BIOS / UEFI                                                                                                                  | Same               | Required by Docker Desktop; on Windows use the **WSL2** backend                                     |
| Privileges       | Local admin / install rights                                                                                                            | Same               | Needed to install runtimes and Docker                                                               |
| Network          | Outbound HTTPS to `repo.maven.apache.org`, `registry.npmjs.org`, `hub.docker.com`, `github.com`, `api.anthropic.com`, `start.spring.io` | Same               | A corporate proxy or VPN that intercepts TLS is the most common blocker; sort this out before class |

---

## 2. Software installations

You are an engineer, so pick the install method you prefer (installer, package manager, version manager). Each entry below gives what it is,
why the course needs it, the official download page, and the command to confirm it works. Skip anything you already have at the required
version.

### Git (latest, 2.55.x or newer)

Version control for the course project, and Claude Code shells out to Git Bash on Windows. Download: https://git-scm.com/downloads
Verify: `git --version`

### Node.js 24 LTS

Runs npm / npx-distributed MCP servers and related tooling. Also required if you install Claude Code through npm instead of the native
installer. Download: https://nodejs.org/en/download
Verify: `node --version` and `npm --version`

### Claude Code (latest)

The CLI you will drive all day. The native installer is self-contained and auto-updates. Install and full
instructions: https://code.claude.com/docs/en/setup
Quick install: `irm https://claude.ai/install.ps1 | iex` (Windows PowerShell) or `curl -fsSL https://claude.ai/install.sh | bash` (macOS /
Linux / WSL). Requirements: macOS 13+, Windows 10 1809+, or Ubuntu 20.04+ / Debian 10+; 4 GB+ RAM. First run: launch `claude`, sign in with
your Anthropic account (Section 3.1). Verify: `claude --version`, then `claude doctor` for a full diagnostic.

### BellSoft Liberica JDK 25 (LTS)

The Java runtime for Spring Boot and Spring AI. Liberica is a free, fully open-source OpenJDK build, TCK-verified, free for commercial and
production use, and is the JDK behind Spring Boot's official container images. Download: https://bell-sw.com/pages/downloads/ (select **JDK
25 LTS**, Full or Standard JDK package)
After install: set `JAVA_HOME` to the JDK 25 directory and put its `bin` on `PATH`. Verify: `java -version` reports `25` (build string shows
`Liberica`).

### Apache Maven 3.9.x (optional)

The build tool. **You can skip installing it**: every project generated by Spring Initializr ships the Maven Wrapper (`mvnw` on macOS/Linux,
`mvnw.cmd` on Windows), which downloads the correct Maven version on first use. Install the standalone CLI only if you want `mvn` on your
`PATH`. Download: https://maven.apache.org/download.cgi
Verify (if installed): `mvn -v` shows `Apache Maven 3.9.x` and `Java version: 25`. Otherwise use `./mvnw -v` inside the project.

### Docker Desktop (latest)

Runs the Oracle database and, later, containerized MCP servers. Needs virtualization enabled and, on Windows, the WSL2 backend.
Download: https://www.docker.com/products/docker-desktop/
Verify: `docker --version` and `docker run --rm hello-world`
Note: sign in with a free Docker Hub account (Section 3.4) to avoid anonymous pull-rate limits.

### Oracle database image (pre-pull)

Pull ahead of time on a good connection so class time is not spent downloading several GB.

```
docker pull gvenzl/oracle-free:23-slim
```

Image page: https://hub.docker.com/r/gvenzl/oracle-free
This image needs no Oracle login and bundles license acceptance. Smoke-test that it starts:

```
docker run -d --name oratest -p 1521:1521 -e ORACLE_PASSWORD=pw gvenzl/oracle-free:23-slim
docker logs -f oratest      # wait for: DATABASE IS READY TO USE
docker rm -f oratest        # clean up
```

**If the course or your team needs a specific Oracle Database version**, browse the available tags
at https://hub.docker.com/r/gvenzl/oracle-free/tags (or Oracle's own registry at https://container-registry.oracle.com for older or
enterprise editions) and pick a tag that:

- runs on your machine's architecture (arm64 vs amd64) and fits its RAM. The `-slim` and `-faststart` variants are the lightest; full images
  and older enterprise editions need noticeably more memory and disk.
- covers the SQL and database features the course exercises.

Then `docker pull` that tag instead and use it when you start the container.

### IDE (your choice)

You are free to use any IDE. **The instructor uses IntelliJ IDEA Ultimate**, so screen-shares and shortcuts will match it.

| IDE                                     | Notes                                                                                                                                   | Link                                     |
|:----------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------|
| **IntelliJ IDEA Ultimate** (instructor) | Full Spring, Spring Boot, and database tooling. Paid, see Section 3.3. Community edition does **not** include Spring or database tools. | https://www.jetbrains.com/idea/download/ |
| VS Code                                 | Free. Add the **Extension Pack for Java** and **Spring Boot Extension Pack**.                                                           | https://code.visualstudio.com/           |
| Spring Tool Suite (Eclipse)             | Free.                                                                                                                                   | https://spring.io/tools                  |

Verify: open the IDE and confirm it detects JDK 25.

### Optional but useful

- `jq` for inspecting JSON returned by MCP calls: https://jqlang.github.io/jq/
- Postman for exercising MCP HTTP endpoints: https://www.postman.com/downloads/

### Quick "everything installed" check

```
git --version
node --version && npm --version
java -version
docker --version
claude --version
# mvn -v        # only if you installed the standalone Maven CLI
```

Expand this to a full smoke test with the Appendix.

---

## 3. Subscriptions and accounts

### 3.1 Anthropic account and Claude subscription (required)

- Create an account: https://claude.ai
- **Claude Pro is the minimum** plan for this course. The free Claude.ai plan does not include Claude Code access, and Claude Code consumes
  tokens continuously during agent and MCP work.
- Heavy users can move to **Claude Max** (5x or 20x) for higher limits: https://www.anthropic.com/pricing
- Alternative: an **Anthropic API Console** account with prepaid credits (pay per token, no session caps): https://console.anthropic.com/
- Pricing overview: https://www.anthropic.com/pricing

### 3.2 GitHub account (required, free)

- Sign up: https://github.com/join
- The course project is tracked on GitHub. Before class, set up authentication: add an SSH key
  (https://docs.github.com/authentication/connecting-to-github-with-ssh) or create a personal access token for HTTPS
  (https://docs.github.com/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).

### 3.3 JetBrains account and IntelliJ IDEA Ultimate (required only if you use IntelliJ)

- Buy or start a trial: https://www.jetbrains.com/store/ (Individual or Commercial subscription)
- Ultimate is needed for the Spring, Spring Boot, and database features shown in class. Free routes:
    - 30-day trial
    - Free for students and teachers: https://www.jetbrains.com/community/education/
    - Free for open-source contributors: https://www.jetbrains.com/community/opensource/
- Participants on VS Code or Spring Tool Suite can skip this entirely.

### 3.4 Docker Hub account (recommended, free)

- Sign up: https://hub.docker.com/
- Signing in to Docker Desktop lifts the anonymous image pull-rate limit, which matters when several people pull the Oracle image on the
  same network.

### 3.5 Oracle account (not required)

The `gvenzl/oracle-free` image is on Docker Hub and needs no login. Only if you prefer Oracle's official image
(`container-registry.oracle.com/database/free`) do you need an Oracle SSO account and a license
click-through: https://container-registry.oracle.com

---

## Appendix: Verification smoke tests

Run each command and check the result.

| Check              | Command                       | Expected                                    |
|:-------------------|:------------------------------|:--------------------------------------------|
| Git                | `git --version`               | `git version 2.55` or newer                 |
| Node               | `node --version`              | `v24.x`                                     |
| npm                | `npm --version`               | any 10.x or newer                           |
| Java               | `java -version`               | version `25`, build string shows `Liberica` |
| Maven (optional)   | `mvn -v` or `./mvnw -v`       | `Apache Maven 3.9.x`, `Java version: 25`    |
| Docker             | `docker --version`            | any recent version                          |
| Docker run         | `docker run --rm hello-world` | `Hello from Docker!`                        |
| Claude Code        | `claude --version`            | prints e.g. `2.1.x (Claude Code)`           |
| Claude Code health | `claude doctor`               | no red items                                |

Oracle end-to-end (about 1 to 3 minutes on first run):

```
docker run -d --name oratest -p 1521:1521 -e ORACLE_PASSWORD=pw gvenzl/oracle-free:23-slim
docker logs -f oratest      # wait for: DATABASE IS READY TO USE
docker rm -f oratest        # clean up
```

---

## Pre-session checklist

**Machine**

- [ ] 16 GB RAM or more, 50 GB free SSD space
- [ ] Virtualization enabled; WSL2 backend on Windows
- [ ] Local admin rights; corporate proxy or VPN does not block the hosts in Section 1

**Software**

- [ ] Git, latest (2.55.x or newer)
- [ ] Node.js 24 LTS
- [ ] Claude Code installed, signed in, `claude doctor` clean
- [ ] BellSoft Liberica JDK 25, `JAVA_HOME` set
- [ ] Maven (optional, the `mvnw` wrapper covers it)
- [ ] Docker Desktop running, `hello-world` works
- [ ] `gvenzl/oracle-free:23-slim` image pulled (or the specific tag the course needs)
- [ ] IDE installed and detecting JDK 25

**Subscriptions**

- [ ] Anthropic account with Claude Pro (or Max, or API credits)
- [ ] GitHub account with an SSH key or personal access token set up
- [ ] IntelliJ IDEA Ultimate license or trial (only if using IntelliJ)
- [ ] Docker Hub account, signed in to Docker Desktop
