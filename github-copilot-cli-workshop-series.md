# Toolkit: GitHub Copilot CLI Workshop Series

This toolkit lists everything to install and set up on your laptop before any course in the GitHub Copilot CLI workshop series. The same
setup serves every course in the series.

## What the courses cover

### AI-assisted development

Working with an agentic coding assistant in the terminal &middot; Writing effective prompts &middot; Reviewing and steering agent output

### Real-world engineering tasks

Exploring and understanding existing code &middot; Automating recurring development tasks &middot; Connecting agents to external tools and
data

### Quality and efficiency

Checking that agent results are reliable &middot; Keeping cost and speed under control

## Goal

By day 1 your laptop is ready for hands-on work with GitHub Copilot CLI: the tools are installed, you are signed in to your GitHub account,
and you can run the verification checks in the Appendix without errors.

## Baseline versions

| Component          | Version             | Notes                                                                           |
|:-------------------|:--------------------|:--------------------------------------------------------------------------------|
| GitHub Copilot CLI | Latest              | Updates frequently; install the newest release                                  |
| Node.js            | Latest LTS          | Only needed for the npm install route; Copilot CLI requires Node.js 22 or later |
| Git                | Latest stable       | Any current release works                                                       |
| Visual Studio Code | Latest stable       | Instructor's editor; any editor works                                           |
| Docker Desktop     | Latest stable       | Optional; the instructor confirms per course                                    |
| GitHub account     | Copilot Free or Pro | Pro recommended                                                                 |

> Complete **Sections 1 to 3** before day 1, then run the **Appendix** checks yourself.

---

## 1. Machine specifications

The heaviest local load is an editor, a terminal, and optionally one or two containers under Docker Desktop, so a standard developer laptop
is enough.

| Resource         | Minimum                                                              | Recommended               | Why                                                                                        |
|:-----------------|:---------------------------------------------------------------------|:--------------------------|:-------------------------------------------------------------------------------------------|
| Operating system | Windows 10 or 11, macOS 13+, or a current Linux distribution         | Latest release of your OS | Copilot CLI supports all three; Windows needs PowerShell v6 or higher                      |
| CPU              | 4 cores                                                              | 8 cores                   | Smooth editor and terminal use alongside optional containers                               |
| RAM              | 8 GB                                                                 | 16 GB                     | Docker Desktop, if used, reserves a few GB                                                 |
| Storage (free)   | 10 GB                                                                | 20 GB                     | Tools plus optional container images                                                       |
| Virtualization   | Enabled in BIOS/UEFI (only if using Docker Desktop)                  | Same                      | Docker Desktop needs it; on Windows it uses WSL 2                                          |
| Privileges       | Permission to install software                                       | Same                      | Installers, and Docker Desktop in particular, need admin rights                            |
| Network          | Outbound HTTPS to github.com, api.github.com, and registry.npmjs.org | Same                      | A TLS-intercepting proxy or VPN is the most common blocker; test on your corporate network |

---

## 2. Software installations

Use your platform's usual install method. Where a tool offers several, pick whichever you already use.

### GitHub Copilot CLI (latest)

The agentic command-line tool every course in the series is built around. Install it with npm, WinGet (Windows), or Homebrew (macOS and
Linux); the npm route needs Node.js 22 or later.
Download: https://docs.github.com/en/copilot/how-tos/copilot-cli/set-up-copilot-cli/install-copilot-cli
After installing, start it once with `copilot` and run `/login` to sign in to your GitHub account.
Verify: `copilot --version`

### Node.js (latest LTS)

Required only if you install Copilot CLI through npm. Skip it if you use WinGet, Homebrew, or the install script.
Download: https://nodejs.org/en/download
Verify: `node --version` and `npm --version`

### Git (latest stable)

Source control; the code review and legacy navigation courses work against Git repositories.
Download: https://git-scm.com/downloads
Verify: `git --version`

### Visual Studio Code (latest stable)

Free choice of editor; the instructor uses VS Code, so using it makes screen-shares easier to follow.
Download: https://code.visualstudio.com/download
Alternatives: [IntelliJ IDEA](https://www.jetbrains.com/idea/download/), [Cursor](https://cursor.com/download)
Verify: `code --version`

### Docker Desktop (latest stable, optional)

Optional. Some courses in the series run services in containers, such as the PostgreSQL MCP server lab; others do not. The instructor will
explain during the course whether Docker (any flavor) is used and what to do with it. Install it now only if you already know your course
needs it, or if you want to be ready. On Linux you may prefer Docker Engine instead of Docker Desktop.
Download: https://docs.docker.com/get-started/get-docker/
Verify: `docker --version`

### Quick "everything installed" check

```
copilot --version
git --version
code --version
node --version
docker --version
```

Skip `node` if you installed Copilot CLI without npm, and skip `docker` if you are not installing Docker.

---

## 3. Subscriptions and accounts

### 3.1 GitHub account with Copilot (required, free or paid)

- Sign up for GitHub: https://github.com/signup
- Plans and pricing: https://github.com/features/copilot/plans
- Copilot CLI is included in every plan. Copilot Free works to get started but has tight usage limits, so Copilot Pro (paid) is recommended
  for the workshops. Pro+ and Max are only worth it if you expect heavy use. Verified teachers, students, and maintainers of popular open
  source projects may qualify for Pro at no cost.
- If your employer manages your Copilot access, ask your administrator to confirm that Copilot CLI is enabled for you.
- Sign in before day 1: run `copilot`, then `/login`, and follow the browser prompts.

---

## Appendix: Verification smoke tests

Run each command and check the result.

| Check                    | Command                       | Expected                                |
|:-------------------------|:------------------------------|:----------------------------------------|
| Copilot CLI installed    | `copilot --version`           | A version number prints                 |
| Copilot CLI signed in    | `copilot` then `/login`       | Login completes and the prompt is ready |
| Git                      | `git --version`               | A version number prints                 |
| Editor                   | `code --version`              | A version number prints                 |
| Node.js (npm route only) | `node --version`              | 22 or higher                            |
| Docker (if installed)    | `docker run --rm hello-world` | Prints "Hello from Docker!"             |

---

## Pre-session checklist

**Machine**

- [ ] My laptop meets the minimum specs and I have install permissions
- [ ] I can reach github.com and api.github.com from my network (try without VPN if blocked)

**Software**

- [ ] GitHub Copilot CLI installed and `copilot --version` works
- [ ] Node.js LTS installed (only if using the npm route)
- [ ] Git installed
- [ ] Visual Studio Code (or my preferred editor) installed
- [ ] Docker Desktop installed, if I know my course needs it (optional; the instructor will confirm)

**Subscriptions**

- [ ] GitHub account created and Copilot plan active (Free works, Pro recommended)
- [ ] Signed in to Copilot CLI with `/login`
