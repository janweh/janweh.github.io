---
title: 'Should the AI Safety Community Prioritize Safety Cases?'
date: 2026-01-13
permalink: /posts/2026/01/how-promising-are-ai-safety-cases/
tags:
  - AI Safety
  - AI Governance
published: true
---

I recently wrote an [Introduction to AI Safety Cases](https://www.lesswrong.com/posts/38HzJMYdr2YL5gWQs/safety-cases-explained-how-to-argue-an-ai-is-safe). It left me wondering whether they are actually an impactful intervention that should be prioritized by the AI Safety Community.

Safety Cases are structured arguments, supported by evidence that a system is safe enough in a given context. They sound compelling in theory—structured arguments forcing developers to affirmatively demonstrate safety rather than just "test and hope" (read my [previous post](https://www.lesswrong.com/posts/38HzJMYdr2YL5gWQs/safety-cases-explained-how-to-argue-an-ai-is-safe) for a longer explanation). They force to make reasoning about safety explicit, are flexible to changes in the technology and put the burden on the deveoper. Anthropic and DeepMind have committed to making Safety Cases in their RSPs.

To figure out how useful they are, I emailed researchers actively working on AI Safety Cases and reviewed the growing literature. This post synthesizes what I learned: first, a brief overview of what Safety Cases are and what work currently exists; then, expert responses to key questions about their feasibility, impact, and limitations. If you have perspectives you'd like to add, I'm happy to incorporate additional expert opinions—feel free to reach out or comment here.

**Questions addressed in this post:**

1. What is currently being done on AI Safety Cases? — *Sketches and prototypes emerging*
2. Will Safety Cases have a strong, positive influence on the safety of Frontier AI Systems? — *Experts disagree*
3. What is currently the largest gap to being able to build comprehensive AI Safety Cases? — *Consensus on Methodology, basic science, technical safety challenges*
4. Will we be able to build convincing safety cases for catastrophic risks before catastrophic risks from AI are possible? — *Unlikely for 5+ years*
5. What is the largest challenge in the adoption of AI Safety Cases in legislation? — *Political will*
6. Should Safety Cases be a large focus for the field of AI Governance? — *Experts disagree, some argue to prioritize transparency*


## What is currently being done on AI Safety Cases?

Actors such as companies, governments, and academics are building sketches for Safety Cases for Frontier LLMs and thus advancing best practices. Here is a (likely incomplete) list of Sketches for AI Safety Cases:

*An incomplete list of Safety Case sketches, including the paper title, institutions involved, threat model, and core strategy.*

| Sketches of Safety Cases | Objective | Core Strategy |
| :---- | :---- | :---- |
| [An Example Safety Case for Safeguards Against Misuse](https://arxiv.org/pdf/2505.18003) (Redwood Research, UK AISI and others) | Misuse | Threat Modelling from expert judgment \+ capability evaluations \+ safeguard evaluations via red teaming |
| [A sketch of an AI control safety case](https://arxiv.org/pdf/2501.17315) (UK AISI and Redwood Research) | Internally deployed Model Exfiltrating sensitive data | Control Protocol evaluated by Red vs Blue Team Evaluation |
| [An alignment safety case sketch based on debate](https://arxiv.org/abs/2505.03989) (UK AISI) | Outer Alignment | Hypothetical, theoretical, and empirical evidence that give safety assurances for Debate Protocols  |
| [Safety case template for frontier AI: A cyber inability argument](https://arxiv.org/abs/2411.08088) (GovAI and UK AISI) | Harm from Cyber Offense | Risk Modelling \-\> Proxy Tasks \-\> Capability Evaluation |
| [Towards evaluations-based safety cases for AI scheming](https://arxiv.org/abs/2411.03336) (Apollo and others) | Scheming Risks | Evaluating ability to Scheme, cause Harm, or circumvent safeguards |
| [Manipulation Attacks by Misaligned AI: Risk Analysis and Safety Case Framework](https://arxiv.org/pdf/2507.12872) (Meridian Impact) | Ability of internally deployed model to manipulate employees | Multiple sketches of arguments for Inability, Control and Trustworthiness |
| [Anthropic's Pilot Sabotage Risk Report](https://alignment.anthropic.com/2025/sabotage-risk-report/) (Anthropic) | Sabotage from internal models | Analyzing multiple risk pathways with Inability, Control, and Trustworthiness arguments |
| [Three Sketches of ASL-4 Safety Case Components](https://alignment.anthropic.com/2024/safety-cases/) (Anthropic) | Sabotage from internal models | Sketches based on Mechanistic Interpretability, AI Control, and Incentive Analysis |
| [Evaluating Frontier Models for Stealth and Situational Awareness](https://arxiv.org/abs/2505.01420) (Google) | Scheming Risks | Inability Argument by evaluating proxy tasks |


While some of these sketches focus on proving some Objective (top-down), others are motivated by sketching how a particular method could give safety assurances (bottom-up). Many Safety Cases use [CAE](https://www.adelard.com/asce/cae/) or [GSN](https://scsc.uk/gsn) as standard notation.

Further work attempts to gather the kind of evidence that would let us build strong safety cases like Science of Evals, [Chain-of-Thought Monitorability](https://arxiv.org/pdf/2510.19476), or [Red-Blue-Team Control Evaluations](https://arxiv.org/abs/2501.17315). Finally, [Bart et al](https://www.cambridge.org/engage/api-gateway/coe/assets/orp/resource/item/68bbf625728bf9025ebb3dcc/original/frontier-ai-safety-confidence-evaluate.pdf) argue for making Claims in Safety Cases Probabilistic, allowing us to assess the confidence that our Objective is met.

After an initial wave of position papers arguing for safety cases people are now busy making "sketches" (ie outlines of possible safety cases) for different safety properties. This is in an attempt to develop better methodology for Safety Cases. Some Frontier AI Companies are attempting to make initial Safety Cases for real production models.

## Will Safety Cases have a strong, positive influence on the safety of Frontier AI Systems?

**TLDR:** Experts disagree on whether Safety Cases will substantially improve frontier AI safety. As best practice in safety-critical industries, they offer flexibility compared to rigid rules and can coordinate diverse stakeholders. However, skeptics argue their practical impact on company behavior may be small (especially for less responsible actors) and they risk providing false assurance while being costly to produce and enforce.

Epistemic effects on safety researchers cut both ways: Constructing Safety Cases forces researchers to make their reasoning explicit, confronting assumptions and rare failure modes that standard evaluation might miss. However, framing the task as "building an argument for safety" risks incentivizing motivated reasoning over objective risk assessment.

**Joshua Clymer:** "I expect most of the value of safety cases will come from improving the clarity of researchers' thinking.
I think I have personally developed a better understanding of how to mitigate AI risks as a result of thinking about safety cases. For example, one problem you run into when thinking about safety cases is that AI systems might have problems that are rare enough to not be seen in evaluations, but common enough to occur in deployment. These problems could be really catastrophic. For example, maybe some future version of Claude is very susceptible to adversarial towards humans at a low probability, and once it becomes adversarial towards humans, it repeats the argument that convinced it to all the other instances of Claude, and soon they're all adversarial too. This is the kind of thing that's really hard to rule out just by evaluating Claude's behavior or even looking at its internals.
So, how should developers mitigate this risk? I think they're going to have to set up a diverse society of AI models with de-correlated misalignment issues.
Not many people are thinking about this right now, and I wouldn't be either if I wasn't considering how to make a comprehensive safety case."

**Anon Expert**: "Yes"

[**Ryan Greenblatt**](https://www.lesswrong.com/posts/neTbrpBziAsTH5Bn7/ai-companies-are-unlikely-to-make-high-assurance-safety)**:** "There is still the question of whether making such safety cases with a less conservative threshold would influence AI company behavior... My sense is that all of these effects exist, but are relatively small, especially for relatively less responsible companies"

[**Ryan Greenblatt**](https://www.lesswrong.com/posts/KMbZWcTvGjChw9ynD/focus-transparency-on-risk-reports-not-safety-cases) (separate post):
"Trying to write a safety case seems like it would have bad epistemic effects on researchers in practice due to putting researchers in the frame of trying to argue why a model is safe."

[**Lucas Texeira et al**](https://www.lesswrong.com/posts/EzrFeLRuww7zTSXhy/toward-safety-case-inspired-basic-research) argue Safety Cases will be valuable as "boundary objects" that coordinate collaboration between basic researchers, applied scientists, and policymakers.

[**Buhl et al.:**](https://arxiv.org/abs/2410.21572) "Safety cases \[...\]  are seen as more comprehensive and flexible than traditional approaches to assurance. \[...\] However, safety cases have also been criticized for providing a false sense of assurance when in reality it is very difficult to produce an adequate safety case or review it effectively \[...\] While there is little empirical evidence for the efficacy of safety cases... and such evidence is difficult to produce given the nature of risk, practitioners mostly consider them effective and they are a recognised best practice in the UK."

They further note that "Safety cases provide a way to integrate different sources of evidence into a single, comprehensive assessment of a system's safety" and are "helpful for checking if risk assessment is comprehensive and valid." Additionally, "Safety cases make otherwise implicit arguments explicit, which \[...\] can highlight reasoning flaws or assurance gaps \[..., \] makes it easier to see how overall system safety is affected if the evidence changes \[... and\] can help stakeholders communicate more clearly about disagreements"

Buhl et al. argue that compared to governments setting specific rules, safety cases are advantageous because they are more flexible and thus durable, incentives innovation in safety and allocate the responsibility to the developer (who is best placed to figure out reasonable safety procedures). However, rules are easier to enforce, more transparent and cheaper to comply with.

## What is currently the largest gap to being able to build comprehensive AI Safety Cases?

**TLDR:** Currently few companies are attempting to publish safety cases, mostly because it's substantial work with unclear value-add. Safety Cases for AI systems are especially difficult because they have many use cases, are constantly advancing in capabilities, and are opaque.

We currently don't have consensus on good methodology, agreement on when a Safety Case is adequate, and lack basic science to justify assumptions and quantify uncertainty.

There are also many technical challenges to making strong safety cases. These include insufficient cybersecurity, monitors colluding with the AI systems they oversee, and misbehaviors that only appear outside of testing distributions (e.g., sandbagging or alignment faking). To make stronger safety cases would require advances in scaling human supervision, interpretability, formal verification, and mitigating scheming risks.

**Joshua Clymer**: "I think we totally can build comprehensive AI safety cases right now. But publishing them is more work than it's worth.

I think the main barrier to establishing safety cases in the AI industry is getting companies to publish them. And the main barrier to getting companies to publish them is that there's a lot of work to write. So, if you want to work on safety cases, I think you should just join an AI company and help them write safety cases. I would start by joining Anthropic since they're already interested in doing things like this.

The next question is how useful this would be in absolute terms, relative to some other way you could spend your time.

I think it would be more useful to do ordinary alignment or control research at an AI company like Anthropic, or if you want to do non-technical work, it's probably more useful to help with comms/awareness building projects if you think you'd be good at that."

**Anon expert**: "Frontier AI is a general purpose technology, the range of applications is very wide.  Currently, the emphasis is on the AI developers building these safety cases.  Due to the wide range of applications, many such safety cases will be required, and building a good one takes a lot of work.   Also the AI capabilities are advancing rapidly, which creates a challenge.  The top-level claim of safety cases is often given in binary claims (e.g. of the type 'The system is sufficiently safe' \- in practice such claims often cannot be made unequivocally \- there should generally be a 'level of confidence' associated with such claims \- but this level of confidence is hard to determine.  The AI is also inscrutable \- which can make it hard to make safety claims for the AI itself (may be easier to make claims of the system within which an AI is embedded \- but this is a difficult thing for an AI developer to do)"

[**Ryan Greenblatt**](https://www.lesswrong.com/posts/neTbrpBziAsTH5Bn7/ai-companies-are-unlikely-to-make-high-assurance-safety) argues that companies are unlikely to be able to reach SL-5 level of cybersecurity and to sufficiently mitigate risk from scheming. These would be necessary for building a comprehensive safety case.

"A core challenge with \[empirical safety case arguments\] is that misaligned behavior may only arise for parts of the input distribution, which may not arise during testing"

[**Rohin Shah** **et al**](https://arxiv.org/pdf/2504.01849) point to multiple technical challenges:

- Inability Safety Cases could be undermined by Sandbagging
- Control Safety Cases face the risks that the AI monitor might collude with the AI it is controlling
- "To establish a robust control safety case based on monitoring \[...\] the primary challenge lies in scaling \[human\] supervision through automatic monitoring"
- Safety Cases based on empirical arguments about safety behavior face the challenge "that misaligned behavior may only arise for parts of the input distribution, which may not arise during testing" eg Alignment Faking.
- Safety Cases based on interpretability or provable verification require significant progress in these fields.

[**Lucas Texeira et al**](https://www.lesswrong.com/posts/EzrFeLRuww7zTSXhy/toward-safety-case-inspired-basic-research): "progress on constructing substantive safety cases is bottlenecked by the absence of a mature basic science which could, in the future, support system modeling with well founded assumptions and quantifiable uncertainty."

[**Buhl et al.:**](https://arxiv.org/abs/2410.21572) One "technical challenge is to develop and build consensus on methodology for frontier AI safety case" This includes "setting an appropriate bar for what constitutes an adequate safety case". Another "technical challenge is to develop the safeguards necessary to assure the safety of advanced future systems"

[**Goemans et al.:**](https://arxiv.org/abs/2411.08088) Argue there is a need for more "granular evaluations that correspond to specific risk models", to address "limitations of human uplift experiments" and for "a more systematic approach to addressing defeaters". Additionally, they point out that "the opacity of frontier AI systems in combination with their open-endedness and large action space make it challenging to assert the completeness of any safety analysis."

## Will we be able to build convincing safety cases for catastrophic risks before catastrophic risks from AI are possible?

**TLDR:** While we can already make rudimentary safety cases for some risks (e.g., against misuse), experts agree that we cannot yet make them for existential risks from more advanced AI systems and likely won't for at least five years—largely because we can't empirically iterate on superintelligent systems. One expert argues a Safety Case for ASI Safety with >90% confidence could be constructed that justifies the safety of an initial AI system and uses it to recursively validate increasingly capable successors up to superintelligence. Others are skeptical that there will be sufficient progress in cybersecurity and scheming mitigation in time.

**Joshua Clymer:**  "I think it depends on what you mean by "catastrophic risk." OpenAI and Anthropic have both said that their frontier LLMs are close to providing misuse actors meaningful assistance with constructing chemical and biological agents. If that meets your definition of catastrophic risk, then I do think that these companies could provide high assurance of safety. Anthropic showed that their safeguards [are robust to thousands of hours of red teaming](https://arxiv.org/abs/2501.18837) from fairly high-skilled contractors. So jailbreaks are hard to find. Bad actors might purchase them, but Anthropic can monitor the black markets too. If these don't really exist, or if Anthropic can patch the problems before misuse actors can benefit much from them, then that's a good argument for safety.

Now, if by "catastrophic risk," what you mean is something like extinction-level threats from dramatically superhuman AI, then I don't expect that companies will be able to provide high assurance against this risk for at least the next five years. Currently, there's very little scientific consensus around how you justify the safety of dramatically superhuman AI. And even if there was scientific consensus, we should have a lot of model-uncertainty. This isn't a domain where we can empirically iterate very much. We can't train takeover-capable superintelligent systems and be wrong about the risks they pose many times. So there's always a chance that we're all kind of confused about how to evaluate these risks, and reality proves us wrong.

However, I do think it's possible to be more than 90% confident that superintelligence is safe \- or maybe even more than 95% confident if developers have a couple years to do careful research. Many people would disagree with me about this, so let me elaborate. The basic argument you'd want to construct looks like this: We started with some AI system that we trust within some scope of tasks. We trust this AI system with those tasks because it generally seemed to behave well on similar tasks, and we don't think this AI system is intelligently throwing off our evaluations.Now, if we can trust this initial AI system to tackle ML research problems within some scope, then perhaps one of those problems is developing another AI system, AI System 2, that will safely tackle harder problems still. And then we can trust AI system 2 to develop an AI system 3 that we can trust with even more difficult tasks. And the process continues like that until there's some AI system N that's superintelligent.

At every step, AI system N credibly assures us that AI system N+1 is safe, so our trust gets passed on in a chain. We don't have to understand on the object level why a superintelligent system is safe so long as we are confident that the *initial conditions* were set correctly.

See [Appendix A](#appendix-a-joshua-clymers-technical-sketch-of-recursive-deference-safety-case) for a more precise sketch of this argument.

Once again, I think this kind of argument could provide \>90% assurance of the safety of superintelligence, but couldn't provide the level of assurance that would be warranted in the near-term."

[**Ryan Greenblatt**](https://www.lesswrong.com/posts/neTbrpBziAsTH5Bn7/ai-companies-are-unlikely-to-make-high-assurance-safety) argues that "AI companies are unlikely to make high-assurance safety cases if timelines are short". He argues it will be very difficult and unlikely that, within 4 years, AI companies can reach sufficient levels of cybersecurity and that they can sufficiently mitigate risks from scheming AIs. Additionally, he finds it unlikely that companies would "unilaterally slow down if they are unable to make high-assurance safety cases".

[**Buhl et al.:**](https://arxiv.org/abs/2410.21572) "It is already feasible to produce rudimentary safety cases based on existing safety frameworks, though significant research breakthroughs will likely be needed to produce safety cases for future systems."

## What is the largest challenge in the adoption of AI Safety Cases in legislation?

**TLDR:** Safety Cases can be burdensome and have a reputation for overregulation, making them unattractive to US policymakers. Mandating Safety Cases for Frontier AI would require much more political buy-in into AI Risk than is currently there. Additionally, if governments want to mandate AI Safety Cases they need to establish bodies with sufficient capacity to review safety cases.

**Joshua Clymer:  "**Safety cases have historically been burdensome. They're often used in industries like the nuclear industry where people write hundreds of pages, and the documents are reviewed in a very slow process.
People in the United States don't want to introduce those frictions, and I think for good reason.
Safety cases are also most popular in Europe, and the European approach to regulation has a bad rap in U.S. politics right now.
So I think people shouldn't use the word "safety cases" in the United States in order to avoid all the historical baggage, and instead use some other term like "risk assessments"

[**Ryan Greenblatt**](https://www.lesswrong.com/posts/neTbrpBziAsTH5Bn7/ai-companies-are-unlikely-to-make-high-assurance-safety)**:** "It seems somewhat unlikely that in short timelines the government ends up broadly agreeing with my views on AI capabilities and misalignment risks to the extent that would be needed for the relevant government action. I don't expect the government to be fully sleepwalking, but in short timelines, very fast action might be required and the government might need to update very quickly toward aggressive action."

[**Buhl et al.**](https://arxiv.org/abs/2410.21572) argue that there are important institutional challenges to adopt safety cases in regulation like: "Appointing or establishing a body to receive safety cases securely" "Building capacity and expertise to effectively review safety cases" and "Incorporating third parties into safety case review"

## Should Safety Cases be a large focus for the field of AI Governance?

**TLDR:** While one expert argues Safety Cases are important, others argue that Safety Cases currently don't seem politically feasible and the AI Safety community should focus more on scenarios in which there is little willingness to pay safety taxes. Instead researchers should focus on Transparency through Risk Reports and producing legible evidence of danger.

**Joshua Clymer:** "I think risk reports are a better framing in the near-term (see [this post](https://blog.redwoodresearch.org/p/focus-transparency-on-risk-reports)).
Safety cases aren't as politically viable because they are more work to make, and create a much more restrictive gate on AI development.
In the near term, I think it makes sense for policy to focus on transparency. And the best thing for transparency is for companies to report the risks they observe (not to try to convince everyone that AI systems are safe)."

**Anon Expert**: "Probably yes, given answer to (2) [positive influence of Safety Cases] \- AI developer's want to deploy (potentially unsafe) AI \- and should therefore be required to make an argument for why they think it is sufficiently safe to deploy the AI (i.e. provide a safety case)."

[**Ryan Greenblatt**](https://www.lesswrong.com/posts/neTbrpBziAsTH5Bn7/ai-companies-are-unlikely-to-make-high-assurance-safety)**:** "I'm relatively less excited about work very specifically focused on safety cases that does not transfer to potentially producing legible evidence of danger. In particular, I worry that some people are spending time constructing tests which could be part of a safety case (if they indicated safety), but if the tests indicated danger this wouldn't actually change anyone's actions.". Instead people should focus on providing evidence of risk and generally focus on a regime where there is less willingness to pay safety taxes. "I think risk analysis is often a better frame, at least when thinking about technical safety (rather than political or messaging implications), in the case where development would likely proceed even if a safety case can't be made."

[**Buck Shlegeris**](https://x.com/bshlgrs/status/1884283464591237369)**:** "In general, AI safety researchers focus way too much on scenarios where there's enough political will to adopt safety techniques that are seriously costly and inconvenient. \[...\] So people focus way more on safety cases and other high-assurance safety strategies than is deserved given how likely they seem."

[**Ryan Greenblatt**](https://www.lesswrong.com/posts/KMbZWcTvGjChw9ynD/focus-transparency-on-risk-reports-not-safety-cases) argues Transparency should focus on Risk Reports rather than Safety Cases because

1. He expects companies won't be able to make strong safety cases, thus making this an unproductive frame.
2.  "Trying to write a safety case seems like it would have bad epistemic effects on researchers in practice due to putting researchers in the frame of trying to argue why a model is safe"
3. People disagree heavily on the risks, "so focusing on collecting relevant evidence/information seems more helpful than focusing on safety cases".

*Thanks to Joshua Clymer and the anonymous expert for sharing their perspectives via email, and to the researchers whose published work I've synthesized here.*

# My Takeaways

Safety Cases were proposed in recent years as a mechanism of governing Frontier AI. Nowadays the field is mostly busy building prototypes of arguments that could be made for different safety problems. Anthropic and DeepMind have stated they must provide Safety Cases once their models hit specific risk thresholds and are currently doing test runs to develop the institutional muscle for actually making strong safety cases.

In my ideal world companies would be required to provide strong Safety Cases before deploying (or building) advanced AI Systems, because I believe they have properties (flexibility, responsibility on developer, comprehensive) that make them well suited for governing AI. Additionally, governments would have capable teams to review them and 3rd parties would be able to scrutinize the arguments made by companies.  However, building such safety cases for advanced AI requires levels of political buy-in that are currently not there and solutions to currently unsolved safety problems. This makes me sceptical that the AI Safety Community should do more work on AI Safety Cases on the current margin.

I still believe it is an important thing for companies to work towards being able to make strong safety cases. This will make it more feasible for governments to adopt Safety Cases as a governance paradigm and can sharpen researchers' thinking. However, technical researchers should prioritize work that remains valuable regardless of whether Safety Cases become load-bearing governance mechanisms.

# Appendix A: Joshua Clymer's Technical Sketch of Recursive Deference Safety Case

1. ***It is safe to defer to Agent 0 on tasks in scope S\_0 (where S\_0 can be defined as the tasks where Agent 0 says we should defer to it)***
   1. ***We evaluated Agent 0 on some tasks E, and its behavior on E was safe (i.e. it would have been safe for us to defer to Agent 0 on tasks in E).***
   2. ***The science of non-adversarial generalization implies that safe behavior on E will generalize to safe behavior on S\_0 (the tasks where we are proposing to defer to Agent 0).***
   3. ***Agent 0 won't generalize to S\_0 adversarially (and so it is ok to apply the science of non-adversarial misgeneralization).***
      1. ***Agent 0 itself is not adversarially trying to induce dangerous misgeneralization from evaluations (it is not 'faking alignment' during evals)***
      2. ***Agent 0 won't be / hasn't been hijacked by another actor that is trying to induce an unsafe misgeneralization.***
   4. ***The set of tasks S\_0 where we are proposing to defer to Agent 0 includes the task of constructing an agent Agent 1 that can be deferred to with a broader scope of tasks S\_1.***

***This is the first deference safety case. And subsequent deference safety cases can be made via an inductive argument:***

***Suppose we want to justify that Agent K can be deferred to with tasks in S\_K.***

***Then, we can argue:***

1. ***It is safe to defer to Agent 0 on tasks in S\_0 (already justified by the first safety case)***
2. ***Agent N says that it is safe to defer to Agent N+1 within set S\_{N+1}, for all 0 \< N \< K.***
3. ***The task of determining that it is safe to defer to Agent N+1 with tasks in S\_{N+1} always lies within set S\_N. (this last claim is true by definition if we define S\_N to be the set of tasks for which Agent N says we can defer to it).***

***So the third safety case amounts to "each AI system keeps telling us that it's safe to defer to the next one"***
