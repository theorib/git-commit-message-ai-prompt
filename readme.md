# AI-assisted git _Conventional Commit_ message prompt

## Table of Contents

- [Introduction](#introduction)
- [Purpose](#purpose)
- [Prompt Features](#prompt-features)
- [Choosing the best AI API to use with AI Commit](#choosing-the-best-ai-api-to-use-with-ai-commit)
  - [The need for a large AI context window](#the-need-for-a-large-ai-context-window)
- [Setup](#setup)
- [Usage](#usage)
- [Current Status](#current-status)

## Introduction

This repository tracks the development of a **custom AI prompt** for use with the [AI Commit VS Code extension](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit). The prompt's purpose is to generate **better [git](https://git-scm.com) commit messages** based on the [_Conventional Commits_ 1.0.0 Specification](https://www.conventionalcommits.org/en/v1.0.0/).

This project's current iteration is loosely based on the extension's original prompt message [Git Commit Message Guide](https://github.com/Sitoi/ai-commit/blob/main/prompt/with_gitmoji.md) and further refined to my needs and taste.

## Purpose

The purpose of this prompt is to generate thorough, consistent and precise [git](https://git-scm.com) commit messages based on the [_Conventional Commits_ 1.0.0 Specification](https://www.conventionalcommits.org/en/v1.0.0/). This prompt achieves this by giving AI precise instructions on composing a commit message based on the current commit's [git diff](https://git-scm.com/docs/git-diff).

The detailed prompt instructions are in the [prompt document](./prompts/conventional-commit-with-gitmoji-ai-prompt.md) of this repository.

## Prompt Features:

AI-assisted git _Conventional Commits_ prompt features:

- Follows [_Conventional Commits_ 1.0.0 Specification](https://www.conventionalcommits.org/en/v1.0.0/).
- Supports [Gitmoji](https://github.com/carloscuesta/gitmoji).
- Messages are written in English.
- Outputs ONLY the commit message.
- Messages need to use [one of the defined types](./prompts/conventional-commit-with-gitmoji-ai-prompt.md#more-information-about-types).
- The output must be formatted according to the [Output Format](./prompts/conventional-commit-with-gitmoji-ai-prompt.md#output-format) section.

## Choosing the best AI API to use with AI Commit

I chose [Gemini](https://ai.google.dev) as the AI API provider for git commit messages for a few reasons:

- It has [one of the largest context windows](https://artificialanalysis.ai/leaderboards/models) out of all of the currently available APIs out there (more on this below) and the biggest context window out of all the APIs supported by [AI Commit](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit).
- The cost related to using Gemini API for this purpose is negligible. I currently spend less than 0.10 USD per month using it nearly every day, multiple times a day indiscriminately.
- Gemini's latest AI models are quite competent in understanding and providing good commit messages based on [git diffs](https://git-scm.com/docs/git-diff).

### The need for a large AI context window

A large context window is essential for generating git commit messages since the [git diffs](https://git-scm.com/docs/git-diff) used by this extension combined with the provided instructions can easily exceed most other AI API's maximum context window, even with very common and relatively simple commits such as a dependency update.

You may choose to use any other supported APIs such as ChatGPT, Azure or DeepSeek APIs but you are likely to have issues with context window size.

## Setup

1. Generate a [Gemini API](https://ai.google.dev) key and add it to the `Ai-commit: GEMINI_API_KEY` setting. If you need help with this, there are quite a few online tutorials such as [How to Obtain a Gemini API Key](https://dev.to/explinks/how-to-obtain-a-gemini-api-key-step-by-step-guide-4m97).

2. Install the [AI Commit](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit) VS Code extension.
3. Open your VS Code settings (`cmd + ,` on a mac) and type `@ext:sitoi.ai-commit` on the search box.
4. Edit AI Commit's extension settings:
   1. On the `Ai-commit: AI_COMMIT_SYSTEM_PROMPT`, paste all the contents of the `ai-git-commit-message-prompt.md` file.
   2. For the `Ai-commit: AI_PROVIDER` field select `gemini`.
   3. For the `Ai-commit: GEMINI_MODEL` type `gemini-2.0-flash` or whatever other Gemini model you may want to use.
   4. Tweak `Ai-commit: GEMINI_TEMPERATURE` to taste. I'm currently using `0.1`.

## Usage

Use the extension to create your AI generate git commit messages:

1. Make changes to a file in your git repository and **stage the changes**.
2. Navigate to VS Code's **Source Control Tab**.
3. From there, you can **press** the little **AI commit button** on top of the `Changes` sub-tab or search for `AI Commit` in VS Code's Command Palette (`command + p` on a Mac). Once you click the button or execute the command, the AI Commit **extension will populate** the tab's **commit message input field** with the AI-generated commit message you can then **review it**, tweak it and eventually **hit commit**.

Optionally, and this is a very powerful feature, before calling the AI Commit extension in step 3, you can provide it with **extra context**, specific to your current commit.

To do this, simply **type the extra information into the commit message input field** (in VS Code's Source Control Tab) before pressing the commit button (or executing the `AI Commit` command).

This can tremendously improve the quality of the commit messages you get from Gemini. I especially recommend this feature if the first commit message you got was not to your satisfaction.

Even a tiny bit of context is normally enough to steer Gemini in the right direction. AI Commit will then pass what you typed together with the instructions provided by you in the Setup step 4.1 to the Gemini API returning a better commit message.

## Current Status

As of the 21st of April 2025, I have been using the [AI Commit](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit) VS Code extension for a few months. I'm currently using it with the [Gemini API's](https://ai.google.dev) `gemini-2.0-flash` model as a good balance between context window size, speed, cost and ability to create good commit messages based on [git diffs](https://git-scm.com/docs/git-diff).

It has proven to be a very useful addition to my tool kit. It helps me speed up my rate of commits while maintaining precision, thoroughness and consistency. It is by no means perfect and it's a work in progress. I will continue to refine it as I go. I recommend always checking the output before committing as hallucinations are not uncommon.
