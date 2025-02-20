# AI assisted Git commit message prompt

## Introduction

This repository tracks the development of a custom AI prompt to use with the [AI Commit](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit) VS Code extension in order to generate better [git](https://git-scm.com) commit messages.

## Purpose

The desired outcome of this prompt is to generate [git](https://git-scm.com) commit messages based on the [Conventional Commits 1.0.0 Specification](https://www.conventionalcommits.org/en/v1.0.0/) and to further refine it with the rules outlined in this repository's the main document.

AI git commit message prompt features:

- Follows [Conventional Commits 1.0.0 Specification](https://www.conventionalcommits.org/en/v1.0.0/)
- Supports [Gitmoji](https://github.com/carloscuesta/gitmoji)
- Messages are written in English
- Outputs ONLY the commit message

## Usage

1. Install the [AI Commit](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit) VS Code extension.
2. Open your VS Code settings (`cmd ,` on a mac) and type `@ext:sitoi.ai-commit` on the search box.
3. On the `Ai-commit: AI_COMMIT_SYSTEM_PROMPT`, paste all the contents of the `ai-git-commit-message-prompt.md` file.
4. I recommend getting a [Gemini API](https://ai.google.dev) key and adding it to the `Ai-commit: GEMINI_API_KEY` setting.
5. For the `Ai-commit: AI_PROVIDER` field select `gemini`.
6. For the `Ai-commit: GEMINI_MODEL` type `gemini-2.0-pro-exp-02-05` or whatever other Gemini model you may want to use.
7. Tweak `Ai-commit: GEMINI_TEMPERATURE` to taste. I'm currently using `0.1`.

## Current Status

As of 20th of February 2025 I have been using the [AI Commit](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit) VS Code extension for a couple of weeks. I'm currently using it with the [Gemini API](https://ai.google.dev) using the `gemini-2.0-pro-exp-02-05` model since it allows for the highest number of tokens per request. You may find this important since sometimes, even small commits can exceed the maximum number of tokens allowed by the Open AI API.

It has proven to be a very useful addition to my tool kit. It helps me speed up my rate of commits, while maintaining precision, thoroughness and consistency. It is a work in progress and I will continue to refine it as I go.
