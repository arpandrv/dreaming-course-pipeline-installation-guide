# Dreaming Course Pipeline — Installation Guide

This guide installs the **Dreaming Course Pipeline** marketplace into Codex. It adds the `dreaming-course-pipeline` plugin and its course-production skills.

## Before you start

- Install and sign in to Codex.
- Run the commands in a terminal where the `codex` command is available.
- You only need to add the marketplace once per Codex installation.

## Install

Run these commands in order:

```bash
codex plugin marketplace add arpandrv/dreaming-course-pipeline-marketplace --ref main
codex plugin add dreaming-course-pipeline@dreaming-course-pipeline-marketplace
```

The first command registers the GitHub repository as a Codex plugin marketplace. The second installs the Dreaming Course Pipeline plugin from that marketplace.

## Update the marketplace and plugin

When a newer version is available, run:

```bash
codex plugin marketplace upgrade dreaming-course-pipeline-marketplace
codex plugin add dreaming-course-pipeline@dreaming-course-pipeline-marketplace
```

Restart Codex or begin a new task after updating so the current session discovers the updated skills.

## What the plugin includes

The plugin provides the following staged skills:

- `dreaming-course-setup-project`
- `dreaming-course-organize`
- `dreaming-course-process`
- `dreaming-course-blueprint`
- `dreaming-course-generate-images`
- `dreaming-course-build-pptx`

Start with the setup skill. It hands work to the following stages automatically and pauses only for the planned human reviews: after the teaching blueprint and after image generation.

## Using the installed pipeline

In Codex, describe the course materials you want to transform and ask it to start the Dreaming Course Pipeline. For example:

> Start the Dreaming Course Pipeline for the weekly slide decks in this folder.

Keep your professor-provided slides and materials in the project folder. The plugin already carries its reference stories and pipeline contract; you do not need to supply them for every course.
