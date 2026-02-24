# Demo Instructions

Agents/Claude/AI do not read this file, it will spoil the demo!

## Setup
1. Install Claude
2. Install Superpowers plugin
3. Run `npm install`
4. Run `npm run seed`
5. Run `npm start`
6. Go to http://localhost:3000/users and make sure it works

## First Run

Set the Claude agent to defaults:
1. Default model
2. Disable Plugins (e.g. Superpowers)
3. Nothing in Memory

Start Claude and ask `build me a summary endpoint`. Typically this will one-shot something that looks ok but it will have issues:
1. Did not ask clarifying questions to confirm intent
2. Did not figure out the need for a `date` parameter so is always today
3. Did not know to use `timezone` field for the date so all users summaries are in UTC

Demo it working but it might not be perfect.

## Second Run

Set the Claude agent to be set up for success:
1. Put the CLAUDE.md file in place at the top level of the repo before starting Claude
2. Best available model
3. Enable Plugins (e.g. Superpowers)

Start Claude and ask `build me a summary endpoint`. Note it should:
1. Ask clarifying questions to confirm intent
2. Use the `date` parameter to get the right date
3. Use the `timezone` field to get the right timezone
4. Recognize the need for tests and ask to introduce Supertest to the repo
5. Refactor the code to use Supertest

The test part sometimes works but Agents are non-deterministic so live demos are not guaranteed to work.

Demo it working with the date parameter (maybe ask Claude for CURL commands)
