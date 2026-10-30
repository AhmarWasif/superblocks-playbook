# Superblocks Deployment Playbook (draft)

An interactive draft of a customer deployment playbook for Superblocks, from signed contract to renewal. Answer the account setup questions and each stage's checklist and watch-outs adapt to that customer.

Drafted by Sardar Ahmar Wasif and built with Claude Code. Not an official Superblocks product. The SoFi example uses public information only, and the sample meeting is fictional. Product details are based on the public Superblocks docs as of October 2026.

## Files

- `index.html`: the whole site. Account data is saved in the visitor's browser only.
- `api/suggest.js`: a Vercel function behind "Update from a meeting". It sends a pasted transcript and the account's playbook state to Claude and returns suggested updates, which the visitor reviews before anything changes. It stores nothing.

## Setup

Add an `ANTHROPIC_API_KEY` environment variable in the Vercel project settings and redeploy. Without it, the rest of the site works and the meeting feature says it isn't connected. Set a monthly spend limit on the key in the Claude Console, since the site is public.
