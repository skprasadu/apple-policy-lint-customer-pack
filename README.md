# Apple Policy Lint — Customer Onboarding Pack

This repo contains **drop-in templates** to onboard a Swift repo to Apple Policy Lint.

## What you copy into your repo
1) `.github/workflows/apple-policy-baseline.yml`
2) `.github/workflows/apple-policy-lint.yml`
3) `.p2i/config.json`

## Required one-time repo setting
Repo → Settings → Actions → General
- Workflow permissions: **Read and write**
- ✅ Allow GitHub Actions to create and approve pull requests

## Onboarding flow
1) Merge the copied files to `main`
2) Run **Apple Policy Lint - Update baseline** (workflow_dispatch)
3) Merge the PR it creates (adds `.p2i/baseline.json`)
4) Open a PR with a Swift change → lint runs automatically and gates on new issues

## Why baseline exists