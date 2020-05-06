# Conventional Comments

## Format

```
<label> [decoration]: <subject>

[discussion]
```

- label - This is a single label that signifies what kind of comment is being left.
- subject - This is the main message of the comment.
- decoration (optional) - This is an extra decorating label for the comment.
- discussion (optional) - This contains supporting statements, context, reasoning, and anything else to help communicate the “why” and “next steps” for resolving the comment.

> **question (non-blocking):** At this point, does it matter which thread has won?

> Maybe to prevent a race condition we should keep looping until they've all won?

```
{
  "label": "question",
  "subject": "At this point, does it matter which thread has won?",
  "decoration": ["non-blocking"],
  "discussion": "Maybe to prevent a race condition we should keep looping until they've all won?"
}
```

## Labels

|             | We strongly suggest using the following labels:                                                                                                                                                                                                     |
| ----------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| praise:     | Praises highlight something positive. Try to leave at least one of these comments per review. Do not leave false praise (which can actually be damaging). Do look for something to sincerely praise.                                                |
| nitpick:    | Nitpicks are small, trivial, but necessary changes. Distinguishing nitpick comments significantly helps direct the reader's attention to comments requiring more involvement.                                                                       |
| suggestion: | Suggestions are specific requests to improve the subject under review. It is assumed that we all want to do what's best, so these comments are never dismissed as “mere suggestions”, but are taken seriously.                                      |
| issue:      | Issues represent user-facing problems. If possible, it's great to follow this kind of comment with a suggestion.                                                                                                                                    |
| question:   | Questions are appropriate if you have a potential concern but are not quite sure if it's relevant or not. Asking the author for clarification or investigation can lead to a quick resolution.                                                      |
| thought:    | Thoughts represent an idea that popped up from reviewing. These comments are non-blocking by nature, but they are extremely valuable and can lead to more focused initiatives and mentoring opportunities.                                          |
| chore:      | Chores are simple tasks that must be done before the subject can be “officially” accepted. Usually, these comments reference some common process. Try to leave a link to the process description so that the reader knows how to resolve the chore. |

## Examples

### Example 1

> **nitpick:** `little star => little bat`

> Can we update the other references as well?

### Example 2

> **praise:** Beautiful test!

## Source

[Conventional Comments](https://conventionalcomments.org/)
