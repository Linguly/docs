---
title: Setup Ruby
parent: Docs Setup
last_modified_date: 30.5.2025
---
- TOC
{:toc}

## For Windows
### Step 1: Install Ruby 3.2 (Stable & Compatible)
Download from the RubyInstaller archives: https://rubyinstaller.org/downloads/archives/

Look for:

`Ruby+Devkit 3.2.X (x64) — Example: Ruby+Devkit 3.2.3-1 (x64)`

Install it, and during setup:

- Run ridk install
- Choose option 3 to install MSYS2

### Step 2: Verify Everything Works
Open PowerShell and check:

```powershell
ruby -v     # should say 3.2.x
gem -v
ridk version
```
Then install Bundler:

```powershell
gem install bundler
```

### Step 3: Run Your Project Again
Go to this repo's folder:

```powershell
cd path\to\your\project
bundle install
```