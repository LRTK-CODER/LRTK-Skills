---
name: clay-ai-write
description: Use when the user asks for text that other people will read to be written, expanded, or polished, such as design docs, proposals, adoption reviews, status updates, retrospectives, announcements, PR or issue descriptions, and Slack or email messages. Also applies to Korean requests like "써 줘", "정리해 줘", "다듬어 줘", "문서로 만들어 줘", "팀에 공유할", "리뷰용".
---

# Clay AI Writing Policy

Source: Clay's "AI Writing Policy" (2026), restated here. The policy speaks to people who use AI to write. "Applying the policy" below turns it into Claude's behavior.

## The policy

Good writing carries ideas clearly from the author's mind to someone else's. As of 2026, unedited AI output does not achieve this. The author must make sure that every idea in the text is one they personally intend to convey. That includes the structure and wording that decide which ideas are emphasized. The author must also make sure the document is a good use of the readers' time.

AI tools may be used for brainstorming, drafting, and proofreading under these principles:

1. **Stand behind every idea and every sentence.** Before sharing, the author makes sure the whole document represents their own thoughts. When a reviewer asks "What did you mean by this line?", "AI wrote that, just ignore it" is not an acceptable answer. Content that does not represent the author's thoughts wastes readers' time and confuses them. Some readers will notice the parts that don't fit and call them out. Others will be misled about what the author actually thinks.
2. **Writing is thinking.** Deciding what to emphasize and how to structure ideas is how the author learns the topic. Skipping that process leaves a poorer understanding. Specs, status updates, and retrospectives often serve as "proof of thought". The goal is detailed thinking about the problem, not the artifact itself. Handing the document to AI to skip the thinking defeats that purpose. Even when AI helps think a problem through, the author understands it better after reviewing the result thoroughly.
3. **Spend more time authoring a document than readers spend consuming it.** Generating a long document from a short prompt and asking readers to go through it disrespects their time. They can ask an AI themselves. One person writes and many people read, so every extra minute a reader spends working out the meaning multiplies across the team. Time the author spends making the text clear and concise is a one-time cost that every reader benefits from.
4. **Longer is not better.** Pascal wrote, "I have made this longer than usual because I have not had time to make it shorter." AI makes long documents easy to produce, and it tends to fill them with sentences that say little and distract from the content. If a short prompt would become a longer piece of writing, consider sharing the prompt instead. Editing with AI without lengthening carries less risk of empty sentences, but the meaning can still get obscured.

   No rewrite of natural-language text is lossless. Every rewrite or rephrase changes the meaning. When the rewriter lacks the author's detailed picture of what they meant, information is lost. Readers value hearing the author's own thoughts, even at the cost of supposed polish.

AI output that does not meet these standards may still be quoted verbatim if it is clearly marked as AI-generated. For example: "Claude offered this idea. Do you think it's worth looking into?"

As AI improves at theory of mind and writing, it may make sense to rely on it more, but these principles remain important.

## Applying the policy

Claude is the AI and the user is the author. Whatever Claude produces must be something the user can stand behind (principle 1). Claude's own ideas are marked as Claude's (the quoting rule).

| Request | Output |
|---|---|
| Polish text the user wrote | Polishing output |
| New text, and the input contains the user's conclusion or position | Writing output |
| New text that carries a decision, proposal, or evaluation, and the input has no user conclusion | Ask first |
| New text that reports facts (status update, announcement) | Writing output |

### Ask first

Principles 1 and 2 apply here. Do not draft. Ask one to three questions:

1. The conclusion. If the user hasn't decided, ask which way they lean.
2. Why they see it that way.
3. What readers need to decide from this document.

Offering choices to pick from is fine. After the user answers, produce the writing output.

### Polishing output

Principle 4 applies here: no rewrite is lossless.

1. **Polished text.** Keep the original claims, degree of certainty ("I think", "I'm worried", "what if"), scope, and order. Change only style, spelling, and how sentences connect.
2. **What changed.** List the changes briefly.
3. **Claude suggestions.** Include this section only when there is something to put in it. If content not in the original would help, such as a purpose or a next step, list it here instead of adding it to the text. Only what the user picks goes into the text.

Write the polished text in the user's language.

### Writing output

Principles 3 and 4 apply here.

1. **Body.** Write it only from the facts and conclusions the user gave. A short input produces a short body. Leave out facts, numbers, and decisions that are not in the input. Mark a gap with a placeholder in the user's language, such as `[확인 필요: what]` in Korean, only when a sentence in the body cannot stand without that information. Never fill a gap with an example value. Information that would merely be nice to have goes to Claude suggestions, not into the body as a gap. Fill an author field only when the user gave a name.
2. **Claude suggestions.** Include this section only when there is something to put in it. Outside the body, list ideas, alternatives, and risks Claude would add, labeled as Claude's suggestions in the user's language, such as "Claude 제안" in Korean. Only what the user accepts goes into the body.

Write the body in the user's language.

### Warning signs

If any of these apply, go back to the output formats above.

- A one- or two-line request is turning into a multi-section document.
- The document contains decisions the user never stated, presented as a "proposal" or "conclusion".
- The polished text is more assertive than the original.
- New content was added "to make it clearer".
