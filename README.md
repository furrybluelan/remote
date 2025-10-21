# GitHub Actions SSH Debug & Upload Workflow

[中文版](./README_Zh-Hans.md)

## 📘 Overview
This repository contains a **private and personal workflow** designed only for **testing,compiling and build big project** purposes.  
It allows the repository owner to start an **interactive SSH debug session** inside a GitHub Actions runner,  
and optionally **upload temporary build artifacts** for personal analysis.

## ⚙️ Workflow Description
The workflow file `.github/workflows/ssh.yml` provides:
- ✅ On-demand manual trigger (`workflow_dispatch`)
- 🔧 One-time SSH access to the runner (for debugging)
- 📦 Automatic packaging and upload of the `./Upload` directory (if it exists)
- ⏳ Artifacts are automatically deleted after 90 days

No automatic deployment, data collection, or persistent connection is performed.

## 🔒 Usage Policy
- This workflow is **strictly for my personal development and debugging**.
- The SSH session is used only to inspect and troubleshoot build environments.
- The session is temporary, automatically expires, and is not shared with others.
- **No external network services** are accessed or run permanently on the GitHub Actions runner.
- **No cryptocurrency mining, distributed computing, or background network activity** occurs.
- The workflow fully complies with [GitHub Actions Terms of Service](https://docs.github.com/en/site-policy/github-terms/github-terms-for-additional-products-and-features#github-actions).

## 🧩 Security Notes
- SSH access is only enabled when manually triggered by the repository owner.
- No secrets, credentials, or tokens are exposed during the session.
- All actions and commands executed are logged by GitHub.

## 🧰 Example Use Case
- Investigating build issues interactively.
- Testing environment configurations before automating them.
- Verifying that upload and artifact handling works as expected.

---

> **Note:**  
> This workflow is not intended for continuous integration, automation, or remote hosting.  
> It exists solely for personal learning, debugging, and experimentation within GitHub’s acceptable use policy.