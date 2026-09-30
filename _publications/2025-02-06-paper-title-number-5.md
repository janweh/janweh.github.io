---
title: "Position: Safety Must Precede the Deployment of Open-Ended AI Agents"
type: "publication"
category: journal
permalink: /publication/safety_is_essential
venue: "ICML 2026"
hide_year: true   # the venue already names a year
authors: "Ivaxi Sheth, **Jan Wehner**, Sahar Abdelnabi, Ruta Binkyte, Mario Fritz"
excerpt: "Open-ended AI is a growing paradigm where AI continuously explores novel and interesting artifacts. This position paper describes specific safety challenges in Open-Ended AI and how they can be mitigated."
links:
  - label: "Article"
    url: "https://openreview.net/forum?id=DMZAZYgFaw"
  - label: "arXiv"
    url: "https://arxiv.org/abs/2502.04512"
---

AI advancements have been significantly driven by a combination of foundation models and curiosity-driven learning aimed at increasing capability and adaptability. Within this landscape, open-endedness, where AI agents autonomously and indefinitely generate novel behaviors, representations, or solutions, has gained increasing interest. This has become relevant in the context of self-evolving agents and long-horizon discovery. This position paper argues that the defining properties of open-ended AI systems introduce a distinct and underexplored class of safety challenges, including loss of predictability, emergent misalignment, and difficulties in maintaining effective control as systems evolve beyond their initial design assumptions, that must be addressed preemptively. These challenges differ qualitatively from those associated with task-bounded or static models and are unlikely to be addressed by existing safety frameworks alone, which is why these risks must be examined proactively, before large-scale deployment. The paper proposes a taxonomy for key challenges, discusses research opportunities, and calls for coordinated action to support the safe and responsible development of open-ended AI.

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@inproceedings{sheth2026position,
  title={Position: Safety Must Precede the Deployment of Open-Ended {AI} Agents},
  author={Sheth, Ivaxi and Wehner, Jan and Abdelnabi, Sahar and Binkyte, Ruta and Fritz, Mario},
  booktitle={Forty-third International Conference on Machine Learning Position Paper Track},
  year={2026},
  url={https://openreview.net/forum?id=DMZAZYgFaw}
}
</code></pre>
</div>

<script>
function copyBibTeX() {
  const bibtex = document.getElementById('bibtex').textContent;
  navigator.clipboard.writeText(bibtex).then(() => {
    const button = document.querySelector('.copy-button');
    const originalText = button.textContent;
    button.textContent = 'Copied!';
    setTimeout(() => {
      button.textContent = originalText;
    }, 2000);
  });
}
</script>
