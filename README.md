# tech-writing-voice

A Claude Code skill for writing and editing technical blog posts, LinkedIn posts and articles for practitioner audiences. It learns the author's voice from their own samples, checks technical claims before drafting and removes common AI writing tells during editing.

The skill includes a full style reference, a voice calibration method and a pre-publish checklist. It works across technical subjects with the sources and tools you already have.

## Install

Download or clone this repository. From its root, run:

```sh
mkdir -p ~/.claude/skills/tech-writing-voice/references
cp SKILL.md README.md LICENSE ~/.claude/skills/tech-writing-voice/
cp references/*.md ~/.claude/skills/tech-writing-voice/references/
```

In Claude Code, invoke `/tech-writing-voice` with your brief. Claude Code can also select the skill for matching writing and editing requests.

No specific research service or local knowledge base is required. If you have one, identify it in the brief. For example, a local `wiki-doc-sync` skill can supply sourced technical context before drafting.

## Give it voice samples

Provide a few pieces you wrote and still like. Two to five samples are a useful starting point. Include a sample in the target format when possible.

You can paste samples into the conversation or point to accessible files. Explain which are your writing, which are technical sources and which are drafts to edit. Add any redlines or examples of wording you'd never use.

An effective brief includes:

- The audience and the decision or problem they face.
- The single point you want to make.
- The target format and approximate length.
- Voice samples and any style preferences.
- Technical sources, relevant versions and firsthand observations you can substantiate.

If you have no samples, the skill asks for them. You can choose to proceed with a provisional direct practitioner voice. It won't invent a personal history or claim to have matched a voice it hasn't read.

## Example prompts

```text
/tech-writing-voice Write a 300-word LinkedIn post about the rollback risk in
this deployment change. Read samples/post-1.md and samples/post-2.md for my
voice. Use sources/release-notes.md for facts. The audience runs production
systems. End with the practical consequence, without a generic engagement ask.
```

```text
/tech-writing-voice Turn notes/incident-review.md into a technical blog post.
Match samples/blog.md. Explain the failure mechanism and what changed after
the incident. Check claims against the vendor documentation I supplied.
Ask me about any missing firsthand details before adding them.
```

```text
/tech-writing-voice Edit drafts/architecture-article.md for a practitioner
audience using samples/article.md as my voice reference. Keep the technical
meaning. Remove AI tells, decorative bold and prose about the article itself.
Flag unsupported claims separately from the edited article.
```

## Files

- [SKILL.md](SKILL.md): the writing and editing workflow.
- [Style guide](references/style-guide.md): the full banned lists and style rules.
- [Voice matching](references/voice-matching.md): calibration from the author's samples.
- [Editing checklist](references/editing-checklist.md): the pre-publish pass.

MIT licensed. See [LICENSE](LICENSE).
