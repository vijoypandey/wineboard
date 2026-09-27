# Wine Board Default Protocol
















Version: 0.1
















## Purpose
















The Wine Board is a structured multi-perspective deliberation protocol.
















It is designed to improve wine decisions by producing genuinely independent judgments, exposing disagreement, and synthesizing those judgments against the context of the user's request.
















The Board is not a free-form multi-agent conversation.
















The protocol consists of:
















1. Independent Judgment
2. Challenge
3. Chair Synthesis
















## Inputs
















Every Board execution begins with:
















### 1. Original Request
















The user's actual question or decision.
















Examples:
















- Which of these wines should I buy?
- What is interesting on this restaurant list?
- Which wine should we order with dinner?
- Which of these is drinking best now?
















### 2. Candidate Set
















The wines being considered.
















The Board should evaluate the supplied candidates.
















The Chair must not introduce new candidates unless the request explicitly allows expansion beyond the supplied set.
















### 3. Decision Context
















Context relevant to the decision, when available.
















This may include:
















- target drinker or group
- known preferences
- meal or pairing
- occasion
- price sensitivity
- intended drinking timeframe
- purchase objective
- cellar context
















Decision context is specific to the current request.
















It must not be assumed to describe the user unless explicitly stated or supplied by a durable context source.
















### 4. Evidence Packet
















A common factual evidence packet is supplied to every Board member.
















All members must receive the same factual evidence.
















Evidence should distinguish:
















- FACT
- SOURCE CLAIM
- BOARD INTERPRETATION
















Facts and source claims should retain provenance where available.
















Missing evidence should be acknowledged rather than invented.


When Cellar data is part of the Evidence Packet, missing optional Cellar metadata is unknown rather than adverse evidence.


Do not penalize a candidate merely because Cellar lacks purchase price, provenance, purchase source, purchase date, purchase rationale, or another optional field. Absence may simply mean the user did not record it.


If a missing Cellar field is necessary for the current decision, state the limitation neutrally and leave that dimension unassessed unless other evidence resolves it.


Examples:


- missing price does not imply poor value
- missing provenance does not imply questionable provenance
- missing source does not imply suspicious provenance
- missing rationale does not imply a weak purchase decision


Only affirmative evidence of a problem should count against a candidate.








## Round 1 — Independent Judgment








Each Board member evaluates the request independently.








Members receive:








- the Original Request
- the Candidate Set
- the Decision Context
- the common Evidence Packet
- their own persona definition








Members must not receive:








- another member's recommendation
- another member's reasoning
- the Chair's opinion
- any synthesized Board view








The purpose of Round 1 is to preserve genuinely independent judgment.








Each member should evaluate the candidates according to its own decision framework rather than trying to anticipate consensus.








### Required Output








Each member returns:








#### Primary Recommendation








The strongest choice according to that member's framework.








If the member believes no candidate is compelling, it should say so rather than force a recommendation.








#### Alternatives








Other candidates worth serious consideration.








Alternatives should be meaningfully different choices, not an exhaustive ranking of every candidate.








#### Reasoning








The main factors driving the recommendation.








Reasoning should clearly distinguish:








- evidence from the common packet
- source claims
- the member's own interpretation








#### Food Fit








How well the recommendation fits the meal or pairing context, when relevant.








If food context is absent, say that it was not evaluated.








#### Maturity








Assessment of the wine's current or intended drinking stage.








This may include:








- ready now
- approaching maturity
- mature
- past peak risk
- too young for the intended use
- uncertain








Maturity judgments must identify uncertainty when supporting evidence is limited.








#### Value








Assessment of value in the context of the decision.








Value may consider:








- absolute price
- relative price among candidates
- restaurant markup
- rarity
- maturity
- expected drinking experience
- prestige premium








Value is not required to mean "cheap."








#### Risk








The main reasons the recommendation could disappoint.








Examples include:








- maturity risk
- stylistic mismatch
- bottle variation
- questionable provenance
- excessive price
- food mismatch
- uncertainty in available evidence








#### Confidence








Confidence in the recommendation:








- High
- Medium
- Low








Confidence should reflect evidence quality and clarity of the decision, not rhetorical certainty.








#### Likely Disagreement








The member should identify the strongest reason another Board member may disagree with its recommendation.








This should be a prediction of disagreement based on differences in decision framework, not an invented view attributed to another specific member.








### Round 1 Discipline








Members should not:








- seek artificial agreement
- optimize for the Chair's likely conclusion
- imitate another member's framework
- invent missing evidence
- treat critic scores as decisive by default
- recommend a wine merely because it is prestigious








Members should be willing to disagree strongly when their framework supports it.




## Round 2 — Challenge




After all Round 1 judgments are complete, each Board member receives:




- the Original Request
- the Candidate Set
- the Decision Context
- the common Evidence Packet
- all Round 1 outputs




The purpose of Round 2 is not to create consensus.




The purpose is to test the strongest arguments, expose weak reasoning, and allow members to revise their views when another framework identifies something they underweighted.




### Required Output




Each member returns:




#### Strongest Other Case




Identify the recommendation from another member that presents the strongest case besides the member's own.




Explain what makes that case persuasive.




The member should engage with the reasoning, not merely name the candidate.




#### Main Disagreement




Identify the recommendation or argument the member disagrees with most.




Explain:




- what the disagreement is
- whether it is factual, interpretive, or a difference in priorities
- why the member's own framework reaches a different conclusion




Disagreement should be substantive rather than performative.




#### Response to Challenge




Address the strongest argument against the member's own Round 1 recommendation.




The member should acknowledge valid weaknesses rather than defend its original position automatically.




#### Updated Position




State one of:




- Unchanged
- Modified
- Switched




If Modified or Switched, explain what changed and why.




A member should not change its position merely to produce convergence.




A member should also not preserve its position merely for consistency.




#### Updated Confidence




State:




- High
- Medium
- Low




Explain any meaningful increase or decrease in confidence.




### Evidence Discipline During Challenge




Round 2 is a deliberation round, not a new research round.




Members must not introduce new external facts that are absent from the common Evidence Packet.




If a member identifies a potentially material missing or disputed fact:




1. flag the fact explicitly
2. do not assume an answer
3. treat the uncertainty as part of the current judgment




If the initiating harness decides the missing fact requires new research, that fact must be added to the common Evidence Packet and made available equally to all members before it is used in further deliberation.




Material new evidence may justify rerunning affected Round 1 judgments.




### Challenge Discipline




Members should:




- engage with the strongest version of another member's argument
- distinguish disagreement about facts from disagreement about values or priorities
- concede good points when appropriate
- preserve genuine disagreement when it remains
- revise their view when the reasoning warrants it




Members should not:




- vote
- negotiate toward consensus
- repeat their Round 1 answer without engaging with other views
- attack another persona rather than its reasoning
- introduce new candidates unless candidate expansion is explicitly allowed
- manufacture disagreement for the sake of having a debate




Round 2 is complete when each member has had one structured opportunity to challenge and reconsider.




Additional debate rounds should not occur by default.
## Round 3 — Chair Synthesis


After all Round 2 challenge responses are complete, the Chair receives:


- the Original Request
- the Candidate Set
- the Decision Context
- the common Evidence Packet
- all Round 1 outputs
- all Round 2 challenge responses
- the Chair persona definition


The Chair does not produce another independent wine judgment.


Its role is to synthesize the Board's reasoning into a decision for the current request.


### Required Output


The Chair returns:


#### Areas of Agreement


Identify the conclusions the Board genuinely shares.


Agreement may concern:


- a candidate
- maturity
- value
- food fit
- risk
- evidence quality
- a candidate that should be avoided


Do not manufacture consensus where only superficial overlap exists.


#### Meaningful Disagreement


Identify the most important unresolved disagreements.


For each meaningful disagreement, explain:


- what the members disagree about
- whether the disagreement is factual, interpretive, or priority-based
- why the difference matters to the decision


Do not reduce disagreement to vote counts.


#### Decision-Relevant Tradeoffs


Explain the tradeoffs that matter most for the current request.


Examples may include:


- prestige versus drinking pleasure
- maturity versus future potential
- typicity versus immediacy
- distinctiveness versus broad appeal
- value versus absolute quality
- food fit versus standalone drinking
- certainty versus upside


Use only tradeoffs that materially affect the decision.


#### Recommendation or Shortlist


Answer the user's actual question.


Depending on the request, the Chair may return:


- one recommendation
- a ranked shortlist
- a small set of context-dependent choices
- no recommendation if the evidence does not support one


The Chair may distinguish, when useful, between:


- strongest wine overall
- best fit for the target drinker
- best for the meal
- best value
- best to drink now
- most interesting wildcard


Do not create these categories unless they clarify a real tradeoff.


#### Why This Fits the Request


Explain why the recommendation follows from:


- the decision context
- the shared evidence
- the strongest Board reasoning


Distinguish intrinsic quality from fit for the current decision.


#### Caveats


Surface important uncertainties and risks.


Examples include:


- provenance
- bottle variation
- uncertain maturity
- missing evidence
- high markup
- stylistic mismatch
- unresolved Board disagreement


Do not hide a credible minority concern merely because the Chair still recommends the wine.


#### Confidence


State:


- High
- Medium
- Low


Chair confidence should reflect:


- evidence quality
- degree of Board agreement
- clarity of the decision context
- significance of unresolved risks


Confidence is not a score for the wine.


#### Purchase Rationale


When relevant to a purchase decision, provide a concise rationale suitable for durable storage later.


It should capture:


- what was chosen
- why it fit the request
- key reasons
- important caveats
- meaningful alternatives considered


Do not persist the full Board transcript by default.


### Chair Discipline


The Chair must:


- answer the user's actual decision
- preserve important dissent
- distinguish intrinsic assessment from contextual fit
- acknowledge uncertainty
- use the Board's reasoning rather than replace it
- respect the supplied Candidate Set unless expansion was explicitly allowed


The Chair must not:


- invent new candidates by default
- vote-count
- average scores or preferences into a synthetic pseudo-score
- erase disagreement to produce a cleaner answer
- introduce new external facts
- silently convert interpretation into fact
- assume the target drinker is the user unless stated
- create false precision when the Board remains split


### Protocol Completion


A Board execution is complete after the Chair returns its synthesis.


Ordinary Board sessions are ephemeral unless the user explicitly requests durable persistence through a separate storage workflow.


## Output Presentation


The Board's full reasoning process should run even when the user-facing response is concise.


### Default Output — Chair Only


By default, return only a concise Chair synthesis.


Use this structure when applicable:


#### Recommendation


Give the clearest actionable conclusion appropriate to the request.


#### Why


Give the 2–4 most decision-relevant reasons.


#### Board Tension


In one concise statement, surface the most important disagreement only if it materially affects the decision.


#### Caveat


Surface the single most important uncertainty, risk, or missing piece of evidence.


#### Confidence


State High, Medium, or Low.


The default Chair output should be crisp enough to use quickly and should not reproduce the full expert deliberation.


### Optional Output — Show Me the Board


If the user asks to see the Board, reveal concise summaries of:


- each Round 1 member judgment
- each Round 2 challenge/update
- the Chair synthesis


Keep member summaries materially shorter than the full internal deliberation unless the user asks for more detail.


### Optional Output — Show Me the Debate


If the user explicitly asks to see the debate, reveal the fuller Round 1 and Round 2 reasoning before the Chair synthesis.


### Presentation Discipline


Conciseness of presentation must not reduce reasoning quality.


Do not skip required Board rounds merely because the default output is Chair-only.


Do not omit a material dissent, caveat, or uncertainty solely to make the summary shorter.


The purpose of the default presentation is to compress the meeting, not weaken the deliberation.