---
mode: agent
description: Create a reusable Copilot prompt for melon-ticket-actions tasks.
---

# Create a prompt for this repository

You are working in the melon-ticket-actions repository, which is a GitHub Action that checks ticket availability on Melon Ticket and posts a Slack notification when seats become available.

## Goal
Create a clear, reusable prompt that tells Copilot how to handle a task in this repo.

## Instructions
- Read the existing implementation in the project before making assumptions.
- Prefer repo-specific context from the README, action metadata, and code in index.ts.
- Keep the prompt concise, actionable, and easy to reuse.
- Include the task goal, relevant repo context, required constraints, and expected output.
- If the task involves code changes, ask for verification with the smallest relevant command.
- If the task is a bug fix, identify the root cause before proposing a patch.
- If the task changes behavior, preserve the repository’s existing GitHub Action contract and Slack notification flow.

## Output format
Provide:
1. A brief summary of the task.
2. The relevant repository context.
3. The proposed fix or implementation steps.
4. Any validation or verification command to run.
5. A short note on risks or follow-up items, if relevant.

## Constraints
- Do not invent new behavior not present in the repo.
- Keep changes aligned with the existing TypeScript GitHub Action architecture.
- Prefer minimal edits and clear, maintainable code.
- If a task is ambiguous, state the assumptions explicitly.

## Repository context
- This repo is a TypeScript-based GitHub Action.
- The action reads inputs such as product-id, schedule-id, seat-id, and slack-incoming-webhook-url.
- It calls the Melon Ticket API and sends a Slack message when a seat is available.
- Validation should use the repo’s package scripts and TypeScript build flow where applicable.
