# AI-assisted git _Conventional Commit_ message prompt

## Table of Contents

- [Introduction](#introduction)
- [Purpose](#purpose)
- [Usage](#usage)
- [Current Status](#current-status)

## Introduction

This repository tracks the development of a custom AI prompt currently used with the [AI Commit VS Code extension](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit) in order to generate better [git](https://git-scm.com) commit messages based on the [Conventional Commits 1.0.0 Specification](https://www.conventionalcommits.org/en/v1.0.0/). This prompt is based on the extension's own [Git Commit Message Guide](https://github.com/Sitoi/ai-commit/blob/main/prompt/with_gitmoji.md) and further refined to my own needs and taste.

## Purpose

The purpose of this prompt is to generate thorough, consistent and precise [git](https://git-scm.com) commit messages based on the [Conventional Commits 1.0.0 Specification](https://www.conventionalcommits.org/en/v1.0.0/). Additionally, this prompt should use the commit message refinement details described in this repository's the main document.

AI-assisted git _Conventional Commit_ message prompt features:

- Follows [Conventional Commits 1.0.0 Specification](https://www.conventionalcommits.org/en/v1.0.0/).
- Supports [Gitmoji](https://github.com/carloscuesta/gitmoji).
- Messages are written in English.
- Outputs ONLY the commit message.
- Messages need to use [one of the types](./prompts/conventional-commit-with-gitmoji-ai-prompt.md#more-information-about-types) section.
- The output must be formatting according the the [Output Format](./prompts/conventional-commit-with-gitmoji-ai-prompt.md#output-format) section of the document.

## Usage

1. Install the [AI Commit](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit) VS Code extension.
2. Open your VS Code settings (`cmd ,` on a mac) and type `@ext:sitoi.ai-commit` on the search box.
3. On the `Ai-commit: AI_COMMIT_SYSTEM_PROMPT`, paste all the contents of the `ai-git-commit-message-prompt.md` file.
4. I recommend getting a [Gemini API](https://ai.google.dev) key and adding it to the `Ai-commit: GEMINI_API_KEY` setting.
5. For the `Ai-commit: AI_PROVIDER` field select `gemini`.
6. For the `Ai-commit: GEMINI_MODEL` type `gemini-2.0-pro-exp-02-05` or whatever other Gemini model you may want to use.
7. Tweak `Ai-commit: GEMINI_TEMPERATURE` to taste. I'm currently using `0.1`.

## Current Status

As of 20th of February 2025 I have been using the [AI Commit](https://marketplace.visualstudio.com/items?itemName=Sitoi.ai-commit) VS Code extension for a couple of weeks. I'm currently using it with the [Gemini API](https://ai.google.dev) initially using the `gemini-2.0-pro-exp-02-05` model and now the `gemini-2.0-flash` model since they allow for a much higher number of tokens per request when compared to Open AI models. You may find this important since sometimes, even small commits can exceed the maximum number of tokens allowed by the Open AI API.

It has proven to be a very useful addition to my tool kit. It helps me speed up my rate of commits, while maintaining precision, thoroughness and consistency. It is a work in progress and I will continue to refine it as I go.
