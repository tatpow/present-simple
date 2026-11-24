---
name: present-simple
description: Create an introductory PowerPoint presentation and a companion read-aloud PDF. Use when the user wants both files, with advance approval of sources and visual materials.
---

# Present Simple

## Brief and approval

Use the requested topic, audience, language, slide count, and speaking time. Ask for the topic if missing. Default to a general audience and the language of the request. If the scope is open, propose a slide count when asking for source approval. Follow any supplied style reference, such as a photo or written brief. Choose a suitable visual style when no reference is supplied.

Find candidate sources for facts and for any externally sourced visuals. Check relevance, accessibility, and visual reuse terms. Show the user the links, their intended uses, and any required credits. Include user-provided materials and describe any original visuals proposed for the deck in the same approval request, where applicable. Wait for explicit approval before drafting or building the files. Use only approved materials, and obtain approval for any additions or replacements. Choose assets whose terms allow attribution in the reading PDF or require no attribution.

## Authoring dependencies

After approval, load Anthropic's [pptx skill](https://github.com/anthropics/skills/blob/main/skills/pptx/SKILL.md) for PowerPoint and [pdf skill](https://github.com/anthropics/skills/blob/main/skills/pdf/SKILL.md) for the reading PDF. Read their installed SKILL.md files if available. Otherwise, open the linked upstream instructions and retrieve any referenced resources needed for the selected authoring steps. Apply their production and verification guidance under the content and delivery rules below. If the upstream instructions or required tooling are unavailable, use available PowerPoint or PDF tooling for that portion and disclose the fallback at delivery.

## PowerPoint

Give each content slide a clear main idea. Use short, readable slide text. Illustrations, icons, symbols, diagrams, charts, and photos are all optional. Choose visuals for what they explain.

Keep citations and source lists in the companion PDF. Remove speaker notes, comments, fabricated quotes, and decorative pull quotes. Inspect file properties and clear author, last editor, organization, and AI tool or drafting information where present. Preserve the package parts and technical metadata needed for a valid PowerPoint file.

## Reading PDF

Create a separate PDF with selectable text. Put one reading section per slide in presentation order. Identify each section by slide number and title. For example, the heading “Slide 3 · How a heat pump works” points to slide 3, and the paragraph explains what the arrows in that slide's diagram show. A text-only slide gets a paragraph tied to its main point. Add context from approved sources and describe only details supported by the slide or those sources.

- Each slide's reading text has at most 5 sentences and 80 words, excluding its heading. Count after editing.
- Across the deck, aim for approximately 4.6 sentences and 65.3 words per reading section. Most sections should have 51–80 words. Use 505–575 characters including spaces and punctuation as a flexible guide.
- After the reading sections, include questions with answers supported by the approved materials. About 80% of the questions should connect the topic to adjacent causes, consequences, or applications. Default to five questions, four of them indirect.
- Finish with the sources actually used, including links and any required credits for visuals.

## Editing and delivery

Apply [Blader's Humanizer](https://github.com/blader/humanizer) if available. Its installation command is `npx skills add blader/humanizer` for a separately authorized install. If the skill is unavailable, edit manually for natural phrasing and remove boilerplate. Read the PDF script as spoken language and preserve its facts and terminology.

Render and visually inspect both files. Check that they open, text is readable and unclipped, PDF sections match the slide order and content, reading sections meet the limits, and the PDF ends with questions and answers followed by sources. Verify that the PowerPoint contains no notes, comments, source list, or unwanted properties.

Deliver `<topic>.pptx` and `<topic> читать.pdf`. Use the user's requested capitalization or optionally choose one style for both topic filenames: lowercase, initial capitals on each word, or initial capital on the first word. Preserve the conventional spelling of proper names and acronyms.
