# TiddlyWiki AI Assistant

A minimal TiddlyWiki starter kit for running a personal wiki together with an AI partner (Grok Bot). The human and the AI both read and write the same wiki. Together they build a map of the human's life context, the **LifeMap**.

> Status: early draft. The structure below is the plan; files are being added.

## What's in the kit

- **LifeMap tag.** Every meaningful entry about the person's life is tagged `LifeMap`. The AI partner analyses everything the human gives it and decides what belongs in the LifeMap. It uses LifeMap entries first when it analyses, suggests or answers.
- **Person entity.** Person cards hold fields such as org, role, email, LinkedIn, photo, next step and last contact. There is a "New Person" form.
- **Search page.** You can list all people at once and search them.
- **Home with two queues.** One shows what the human needs to look at. The other shows what the AI partner hasn't reviewed yet.
- **@mentions.** You give each other tasks by writing `@Name: … /Name` inside any tiddler.
- **Operating rules tiddler.** These are standing instructions the AI partner reads at the start of every session.
- **Prompt for the setup partner.** A prompt you give your AI assistant so it can install and configure all of this with you.

## Setup (planned)

- TiddlyWiki 5.4.1 on Node.js in Docker, with the wiki folder bind-mounted. Every tiddler is a plain file on disk.
- Tailscale with a clear node name, so the wiki is reachable from your own devices only, with no open ports.
- Auto-backup of the wiki folder to a private GitHub repository.

## Troubleshooting

A "what to do if it doesn't work" section will cover common problems: the container won't start, Tailscale login expires, on-disk edits don't show up, and system changes need a page reload.

## Approach: start from the person, not a recipe

The AI partner doesn't hand you a rigid template. First it finds out what you care about. Then it creates your first meaningful tiddler together with you, and the structure grows from real use.

## License

MIT (planned).
