# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A static, three-file HTML/CSS page used for practicing Git. This folder is the "colleague" clone of `hello-git-site` (GitHub: `TomGM/hello-git-site`), used to simulate a second person working on the same repo (e.g. for pushing, pulling, and resolving merge conflicts). The site content is deliberately trivial; the Git history is the point.

There is no build, lint, or test tooling and no dependencies.

## Running

- Open directly: `start index.html` (PowerShell)
- Or serve over HTTP: `python -m http.server 8000`, then visit `http://localhost:8000`

## Structure

- `index.html` – all content; each line of text is its own `<p>` so Git diffs and merge conflicts stay line-sized. Keep it that way when adding content.
- `style.css` – the only stylesheet, linked from `index.html`.

## Git workflow

- Work happens on `feature/*` branches merged into `main` via GitHub pull requests (see PR #1, #2 in history). Don't commit straight to `main` unless asked.
- Because this clone and the original both edit `index.html`, expect conflicts around the same lines; pull from `origin` before starting new work.
