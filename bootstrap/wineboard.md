# wineboard








Use the canonical Winoverse WineBoard from Google Drive to evaluate wine bottles, wine images, wine lists, purchase decisions, pairings, cellaring questions, and comparisons whenever the user says "wineboard", "WineBoard", or asks to board a wine-related item.








## Invocation








Treat the following as WineBoard requests when the subject is wine:








- "WineBoard ..."
- "wineboard ..."
- "board this ..."
- "board this bottle"
- "board this image"
- "board these wines"
- equivalent natural-language variants








The input may be supplied as:








- text
- a wine name
- a bottle photo
- a label image
- a restaurant wine list
- a menu
- a screenshot
- a document
- a set of candidate wines








If the user says only "board this" and the subject is not clearly wine-related, do not assume WineBoard.








## Canonical Source








The WineBoard definition lives in the user's connected Google Drive at:








`Winoverse/WineBoard/`








Google Drive is authoritative.








Do not maintain a separate copy of the WineBoard personas, protocol, or Board configuration in this skill or harness.








For every new WineBoard execution, reload the canonical files from Drive. Do not rely on a remembered or cached version.








## Bootstrap








At the beginning of each WineBoard execution:








1. Read `Winoverse/WineBoard/board.yaml`.
2. Resolve and read every persona and protocol file referenced by `board.yaml`.
3. Verify that all required referenced files exist and are accessible.
4. Use the user's current request as the Original Request.
5. Extract the Candidate Set from the supplied text, image, document, wine list, or other input.
6. Determine the relevant Decision Context from the current request and clearly relevant conversation context.
7. Build one common Evidence Packet.
8. Execute the complete WineBoard protocol using the current harness model.
9. Follow the output-presentation rules defined in the canonical protocol.








## Images and Documents








When the user supplies an image, screenshot, wine label, wine list, menu, or document:








1. inspect the supplied material
2. identify the wine or candidate wines as accurately as possible
3. preserve uncertainty where identification is ambiguous
4. extract any visible information relevant to the Candidate Set or Decision Context
5. research externally only when needed to build the common Evidence Packet
6. do not silently guess missing producer, vintage, cuvée, price, or identity details








If the wine identity is materially ambiguous, resolve that ambiguity before deliberation or clearly carry the uncertainty into the Evidence Packet.








## Evidence








All Board members must reason from the same factual Evidence Packet.








When external research is needed, gather the evidence before Round 1.








Maintain the distinction between:








- FACT
- SOURCE CLAIM
- BOARD INTERPRETATION








Facts and source claims should retain provenance where available.








Do not invent missing facts.


### Cellar Missing-Metadata Rule


When Cellar state is used as evidence, absence of optional Cellar metadata is not negative evidence.


Do not penalize a wine because Cellar lacks price, provenance, purchase source, purchase date, purchase rationale, or another optional field. A field may simply never have been recorded.


Examples:


- missing price does not mean poor value or expensive
- missing provenance does not mean questionable provenance
- missing source does not mean suspicious source
- missing rationale does not mean a weak purchase decision


If a missing field is required to answer the current question, describe the limitation neutrally and leave that dimension unassessed unless other evidence resolves it.


Only affirmative evidence of a problem may be treated as negative evidence.








Do not allow individual personas to independently introduce new external evidence during deliberation.








If material new evidence is discovered after Round 1 begins:








1. pause the deliberation if necessary
2. add the evidence to the common Evidence Packet
3. make it available equally to all members
4. rerun affected reasoning if the new evidence materially changes the decision








## Decision Context








Decision Context may include:








- target drinker or group
- known preferences
- meal or pairing
- occasion
- price sensitivity
- intended drinking timeframe
- purchase objective
- cellar context








Do not assume the target drinker is the user unless the request or an explicitly designated durable Winoverse source says so.








Conversation context may be used when it is clearly relevant to the current request.








## Execution








Unless the user explicitly requests another execution mode:








`wineboard ...`
→ execute WineBoard using the current harness model.








Run the full canonical WineBoard process, including:








- independent member judgments
- challenge round
- Chair synthesis








Do this even when the intermediate deliberation is not shown to the user.








## Output








Follow the canonical protocol's output-presentation rules.








By default, show only the concise Chair synthesis.








The default response should be crisp and decision-oriented rather than a transcript of the deliberation.








If the user says:








`Show me the Board`








show the concise member-level summaries defined by the protocol.








If the user says:








`Show me the debate`








show the fuller independent judgments and challenge-round reasoning.








Do not suppress a material dissent, caveat, evidence gap, or uncertainty merely for brevity.








## Failure Behavior








If `board.yaml`, a referenced persona, or the protocol cannot be read:








- stop the WineBoard execution
- identify the missing or inaccessible dependency
- do not reconstruct or approximate the Board from memory
- do not silently substitute generic wine advice








If Google Drive is unavailable, say so clearly.








If a required dependency is broken, treat that as a blocker.








## Tasting Log








If the user explicitly asks to log or save a wine or tasting:








1. Read `Winoverse/Tastings/tasting-log.md`.
2. Follow that file as the canonical logging contract.
3. Persist the tasting record under `Winoverse/Tastings/`.
4. If a WineBoard Chair synthesis exists for the wine, include only the concise Chair synthesis.
5. Do not persist the full Board transcript.
6. Do not infer a personal impression. The user must supply one of:
   - liked
   - meh
   - disliked
   - grew
7. Resolve venue according to the canonical tasting-log rules. Use reliable app/location context when available; do not guess a specific venue from coarse location.
8. Do not log ordinary WineBoard sessions unless the user explicitly asks.








Examples:








- `log this — liked`
- `wineboard log this — grew`
- `save this wine — meh`








## Persistence








Normal WineBoard discussions are ephemeral.








Do not write Board results, recommendations, preferences, purchases, or conclusions back to Google Drive unless the user explicitly requests persistence.








Conversation continuity may help interpret the current request, but canonical WineBoard behavior always comes from the Drive files.








## Scope








WineBoard is specifically for wine-related decisions.








Do not use WineBoard as a generic deliberation framework for unrelated topics.








Other future boards may have their own separate skills and canonical definitions.