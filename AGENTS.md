## Skill invocation policy

- **User-Invoked Skills**: If the file `SKILL.md` says `disable-model-invocation: true` or the file `agents/openai.yaml` says `policy.allow_implicit_invocation: false` then human MUST explicitly invoke it, and the model CANNOT invoke it on its own.

- **Model-invoked**: If the conditions above are not met, then the model can invoke the skill on its own, and the human can also invoke it.

## Agent skills

### Issue tracker

<placeholder>

### Triage labels

Use the default labels `needs-triage`, `needs-info`, `ready-for-agent`, `ready-for-human`, and `wontfix`. See `docs/agents/triage-labels.md`.

### Domain docs

<placeholder>
