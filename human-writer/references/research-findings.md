# StoryScope: findings and editing implications

Prepared for PrismAgent Solutions · October 25, 2026

## Source and scope

Jenna Russell, Rishanth Rajendhran, Chau Minh Pham, Mohit Iyyer, and John Wieting. *StoryScope: Investigating idiosyncrasies in AI fiction*. arXiv:2604.03136v6, August 10, 2026.

- [Versioned paper](https://arxiv.org/abs/2604.03136v6)
- [Full text](https://arxiv.org/html/2604.03136v6)
- [PDF](https://arxiv.org/pdf/2604.03136v6)
- [Authors' code and data](https://github.com/jenna-russell/storyscope)

The paper's arXiv page identifies its license as CC0. This document paraphrases the findings and supplies original examples and editorial interpretations. The research authors and their institutions have not endorsed this resource.

The study examines **fiction**, using human short stories and AI stories generated from reverse-engineered prompts. It reports a nominal corpus of 61,608 stories from 10,272 prompts, with a mean length of about 4,753 words. The five model sources are Claude Sonnet 4.6, GPT-5.4, Gemini 3 Flash, DeepSeek V3.2, and Kimi K2.5. These are the tested model versions, not permanent descriptions of the products.

The pipeline extracts structured story representations, compares sources, discovers features, and assigns feature values. It trains classifiers on those features. The 304-feature taxonomy contains 257 features retained for the strict narrative model; 47 are excluded as style-related. A feature's presence in the taxonomy does not make it an AI signature or a writing defect.

## What “93%” means

The primary narrative model scores **93.2% macro-F1**, averaging class-level F1 scores for human and AI stories. This balances precision and recall; it is not the proportion of all possible writing that Google can correctly identify. The all-feature model scores 96.0%; the 30-core-feature model scores 84.8%. Results are benchmark performance, not an authorship probability for a particular paragraph.

The paper does not demonstrate that Google Search applies this classifier, that these numbers transfer to business emails or social posts, or that a prompt can remove all authorship signals. It evaluates five models and a specific fiction-generation setup.

Section 4.2 applies LAMP surface editing to 278 Gemini-generated stories. Narrative classification macro-F1 changes from 95.5% to 93.9% on that experiment. This is evidence that surface cleanup leaves much of the narrative signal intact. The Human Writer skill has not been evaluated against StoryScope or any external detector and makes no evasion or authorship guarantee.

## How to read the feature tables

Tables 14 and 15 present **20 AI-leaning and 13 human-leaning directional cues**, spanning **30 distinct underlying features**. Three features occur on both sides with different category values: emotional expression, reference explicitness, and subplot integration.

The examples below are invented illustrations of a feature, not quotations from the paper, classifier test cases, or evidence of authorship. A story may use any of these techniques well. Edit only when a change improves the intended writing.

### All 20 AI-leaning core cues (Table 14)

| # | Feature or elevated option | Original quick example | Appropriate editing response |
|---|---|---|---|
| A1 | Explicit themes and moralizing | “And that was how she learned that courage means acting despite fear.” | If the scene already conveys the lesson, trim the explanation. Keep it if the narrator's voice depends on it. |
| A2 | Emotion expressed through the body | Fear repeatedly appears as tight ribs, knotted stomachs, and cold hands. | Remove repetitive physical shorthand; use a plain emotion word or meaningful behavior when it fits. |
| A3 | Strong thematic unity | Every minor event, object, and side conversation repeats the same lesson about trust. | Retain useful texture or conflicting implications already present. Do not create irrelevant subplots. |
| A4 | Olfactory sensory imagery | Every room arrives with a catalog of coffee, dust, rain, and cedar smells. | Keep scent where it matters to action, memory, or atmosphere; cut decorative repetition. |
| A5 | Character introduced through external description | The first paragraph catalogs a person's coat, eyes, height, and hair before they do anything. | Consider opening with an existing action or line of dialogue if it serves the scene. |
| A6 | Setting mirrors psychology | Rain always signals grief; sunshine arrives exactly when the character forgives someone. | Remove redundant emotional signaling, while preserving intentional symbolism. |
| A7 | Continuous main causal chain | Each clue immediately produces the next action, with no interruption or competing pressure. | For developmental fiction edits, consider whether existing complications need space. Keep useful causality. |
| A8 | Dense sensory description | A simple door-opening includes temperature, scent, texture, light, and sound. | Keep details that affect the experience and cut those that only delay the action. |
| A9 | Resolution driven by protagonist choice | One decisive personal choice resolves every external obstacle. | Examine whether the established world supports the resolution; suggest changes separately if it does not. |
| A10 | Narrator explicitly comments on the theme | The narrator pauses after an argument to explain what it teaches about loyalty. | Trust the reader where the dialogue already carries the point. |
| A11 | Clear spatial grounding at the opening | A story begins by locating the street, building, room, and furniture before introducing tension. | Keep orientation readers need; move surplus description to where it becomes relevant. |
| A12 | Dialogue used for philosophical debate | Characters discussing a missed train launch into speeches about fate and freedom. | Check whether the dialogue fits their immediate aims and individual voices. |
| A13 | Fine-grained physical space | The prose specifies the exact position of every chair in a scene where none matters. | Retain spatial details needed to follow action; remove unnecessary mapping. |
| A14 | No subplots | Only the central quest receives attention; other relationships never affect it. | Do not add a subplot to a short piece merely to counter this cue. In developmental work, flag a neglected existing thread. |
| A15 | Heavy moral or philosophical weighting | Even a routine purchase becomes a meditation on what it means to be good. | Match the weight of reflection to the story's actual stakes and voice. |
| A16 | Diffuse intertextual echoes | “Like a hero from an ancient tale” replaces a specific reference the character might make. | Use an accurate, relevant named reference if the source supports it; otherwise remove the empty comparison. |
| A17 | Environmental or ecological emphasis | A relationship scene repeatedly detours into the ecosystem beyond the window. | Keep environmental focus when it is part of the story's purpose; reduce incidental detours. |
| A18 | Resolution through internal understanding | A concrete conflict concludes solely with “she finally understood,” leaving practical consequences unexplored. | Preserve intentional inward endings; flag an accidental mismatch between conflict and resolution. |
| A19 | More investment before the threat | Several paragraphs of memories precede the first sign of danger. | Adjust pacing only if the setup delays the experience the author wants. |
| A20 | Deep access to inner life | Each gesture is followed by a full account of thought, memory, and interpretation. | Cut thoughts already implied by action; retain interiority that contributes something new. |

### All 13 human-leaning core cues (Table 15)

These are comparative findings, not ingredients that must be inserted into a rewrite.

| # | Feature or elevated option | Original quick example | Appropriate editing response |
|---|---|---|---|
| H1 | Specific named intertextual reference | A character compares a predicament to *Hamlet*. | Preserve accurate, relevant references; do not fabricate reading history or citations. |
| H2 | Direct address to the reader | “You may think I should have left. I did too.” | Retain purposeful address when it belongs to the narrator's voice. |
| H3 | Balanced explicit and implicit references | One named work appears alongside a subtler echo of another tradition. | Preserve the author's range rather than forcing every allusion to be explicit. |
| H4 | Surprise changes the meaning of earlier scenes | A discovery makes an earlier apparent betrayal read as protection. | Preserve established clues and causal consistency; propose a new twist separately. |
| H5 | More dialogue relative to narration | An argument unfolds in exchanged lines rather than a narrated summary. | Keep dialogue that reveals action or voice. Do not fabricate quotations in nonfiction. |
| H6 | Fourth-wall permeability | The narrator interrupts the story to question how it is being told. | Keep deliberate metanarrative play; do not add it to unrelated prose. |
| H7 | Thematically parallel subplot | A secondary relationship examines trust differently from the main relationship. | Preserve useful existing secondary threads; avoid adding new ones during a line edit. |
| H8 | Chronological discontinuity | The narrative moves from an aftermath to the earlier decision that caused it. | Retain purposeful order; protect comprehension and actual event chronology. |
| H9 | Wider variety of locations | A story moves among home, workplace, and another town, with each place affecting events. | Preserve meaningful settings. More locations are not inherently better. |
| H10 | Flashbacks or flash-forwards | A childhood scene interrupts a present-day confrontation. | Keep time shifts that change understanding; do not add them to instructions or factual timelines. |
| H11 | Morally ambivalent protagonist | A character helps a friend while concealing a selfish reason. | Preserve complexity already in the text; do not invent motives or accusations in factual writing. |
| H12 | Explicit emotion labels | “She was angry.” | A direct label can be stronger than a chain of bodily metaphors. Use it when consistent with the voice. |
| H13 | Nonlinear order delays disclosure | The reader encounters the consequence before learning the event that explains it. | Maintain deliberate suspense in fiction; do not obscure information the reader needs to act. |

## Model fingerprints (Section 5 and Table 17)

Fingerprints concern attribution among sources, not a universal human/AI boundary. Table 17 prints the top five per source, or all three for Kimi. The paper reports additional fingerprints without fully defining each in that compact table. The 28 displayed entries are all included below. A measurement example for an unsigned feature does **not** establish which direction characterizes the model.

| Source | Displayed feature or option | Original illustration or measurement example |
|---|---|---|
| Human | Introduction in dialogue | The reader meets someone through “You took my seat.” |
| Human | Single focal character | One character's perceptions remain the lens throughout. |
| Human | Narrator address: no direct address | The narrator never explicitly addresses an audience. This is a different variable and task from H2; do not flatten the findings into one rule. |
| Human | Back-loaded revelation | The major explanation arrives near the end. |
| Human | Crossover-genre ambition | A detective structure is used to pursue a literary family drama. |
| Claude | Strength of event escalation | Compare how sharply stakes rise between successive events; Section 5 reports flatter escalation. |
| Claude | Event-type diversity | Compare a sequence of conversations with a sequence mixing travel, confrontation, discovery, and negotiation. The table alone does not specify a signed editing rule. |
| Claude | Ending with epilogue or flash-forward | A final paragraph moves ten years beyond the main action. |
| Claude | No dream or vision distortion | The story has no dream-based interruption of ordinary time. |
| Claude | Uncanny or haunted setting mood | A familiar house feels subtly wrong. |
| GPT | Salient gossip and rumor | A rumor travels among neighbors and changes what characters do. |
| GPT | Distant retrospective narrator | “Thirty years later, I still remember that afternoon.” |
| GPT | Subverts reader expectations | An apparently reliable helper becomes an obstacle. |
| GPT | No iterative or habitual narration | Events are told as individual occurrences rather than “Every Sunday, we...” summaries. |
| GPT | Partial or ambiguous reconciliation | Two estranged people speak again without clearly forgiving each other. |
| Gemini | Expanding protagonist social world | The central character acquires more connections as events develop. |
| Gemini | Primarily direct speech | Conversations appear mainly as quoted dialogue rather than paraphrase. |
| Gemini | Siege or ordeal narrative schema | Characters endure a prolonged threat or test. |
| Gemini | Personal-name introductions | A character is named rather than identified only by a role. |
| Gemini | Frequent flashbacks | Present events are repeatedly interrupted by earlier scenes. |
| DeepSeek | Narrator presence or visibility | Compare unobtrusive narration with a narrator who comments on telling the story; the table lists the variable without a signed option. |
| DeepSeek | Emotion through behavioral cues | A character folds a letter twice before answering. |
| DeepSeek | Plot-versus-atmosphere orientation | Compare event-driven prose with a scene chiefly devoted to mood; the table does not prescribe a direction. |
| DeepSeek | Evenly interleaved backstory | Past context is distributed through the present action. |
| DeepSeek | Embedded storytelling scenes | One character tells a story inside the larger story. |
| Kimi | Character introduced in action | The first glimpse is someone dropping a suitcase from a train. |
| Kimi | In medias res entry | The opening starts during an ongoing argument. |
| Kimi | No explicit trait labels | Behavior implies generosity instead of the narrator calling someone generous. |

Section 5 also describes Claude's uniform voice and reverent relationship to tradition; GPT's ensemble-oriented social worlds; DeepSeek's earlier provision of crucial context; Gemini's tidy, extended endings and bleak settings; and Kimi's position near the shared AI cluster. These are corpus observations. Their mixtures demonstrate why “invert every AI pattern” is not a coherent editing method: a flashback can be human-leaning in one comparison and a Gemini fingerprint in another.

## Limits and source inconsistencies

- Human material comes from Books3 short stories; AI material is generated from prompts inferred from those stories. This is not a random sample of every human and AI writing situation.
- Much feature discovery and extraction uses LLMs. The paper reports repeated-extraction agreement and a small human validation exercise (12 stories, 240 story-feature items per annotator, two annotators), not universal human agreement across the whole corpus.
- Grouped splits, length-matching checks, topic checks, and a memorization-risk audit strengthen the experiment, but do not establish performance on short business posts or heavily human-edited mixed-authorship documents.
- The v6 text has inconsistent accounting across sections: the main experiment and Appendix D give different split counts, and the public repository describes a slightly smaller feature dataset than the nominal 61,608-story corpus. Preserve the paper's headline result as reported; do not silently reconcile these discrepancies into invented counts.
- The abstract page describes GPT dream sequences, while the v6 full-text abstract and Section 5 discuss gossip. This guide follows the versioned full text and identifies that mismatch rather than treating both as a confirmed fingerprint.
- Fingerprint counts vary by representation: the paper mentions 75 fingerprint features, a 101-feature core-plus-fingerprint variant, and per-source counts totaling more than 75. Do not describe that total as a count of unique independent signs.
- Neither the 304-feature taxonomy nor the selected cues is a universal “AI checklist.” No individual cue proves authorship, poor quality, or deception.

## Applying this to PrismAgent business writing

The transferable editorial ideas are to remove redundant explanation, choose supported specifics over generic claims, preserve voice, and match structure to the reader's purpose. This application is our judgment, not a result established by StoryScope.

Business writing often needs the very traits that distinguish AI fiction in this benchmark: a clear goal, explicit reasoning, a logical sequence, and a complete conclusion. Keep those benefits. Do not add moral ambiguity, fake sensory experiences, arbitrary nonlinearity, or unresolved instructions to chase a supposed “human score.”

The complete 304-feature taxonomy is published in the authors' MIT-licensed repository linked above, as `data/taxonomy.json`. It is optional research material and is not needed for routine skill use. The skill package does not contain the copyrighted human story corpus or the authors' detector implementation.
