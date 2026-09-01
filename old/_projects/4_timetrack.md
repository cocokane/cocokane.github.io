---
layout: page
title: TimeTrack
description: A native macOS menu bar app for work-session accountability, built in Swift
img: assets/img/projects/timetrack.jpg
importance: 4
category: fun
---

A minimal, native macOS menu bar app for **work-session accountability** — not a to-do list, but a log of what you have actually done. Sessions are stored locally per day in YAML files with tags, descriptions, and optional remarks.

### Features

- **Two tracking modes**: Target Time (countdown to daily goal) or Stopwatch
- **Dashboard**: Timeline view with day navigation and session editing
- **Global shortcuts**: ⌥⌘A to open, ⌥⌘P to pause/resume (via Carbon HotKey API)
- **Dark theme** with gold (#FFD700) accent
- **Local-first**: Data stored in `~/Library/Application Support/TimeTracker/` — no cloud, no account
- **Atomic writes** with `.bak` backups for data integrity

Built to deepen Swift and AppKit knowledge; the codebase is a work in progress with planned additions for analytics, tag-based filtering, and CSV/JSON export.

**Tools:** Swift, SwiftUI, AppKit, Yams (YAML serialization)

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <a href="https://github.com/cocokane/TimeTrack" target="_blank" rel="noopener noreferrer" class="btn btn-sm z-depth-0" role="button">
    <i class="fa-brands fa-github"></i> GitHub Repository
  </a>
</div>
