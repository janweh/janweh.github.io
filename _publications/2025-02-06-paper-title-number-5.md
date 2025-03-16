---
title: "Safety is Essential for Responsible Open-Ended Systems"
type: "publication"
category: journal
permalink: /publication/safety_is_essential
excerpt: |
    Ivaxi Sheth, **Jan Wehner**, Sahar Abdelnabi, Ruta Binkyte, Mario Fritz forthcoming in _SSI-FM ICLR 2025 Workshop_, 2025

    Open-ended AI is a growing paradigm where AI continuously explores novel and interesting artifacts. This position paper describes specific safety challenges in Open-Ended AI and how they can be mitigated.

    [[Article]](https://arxiv.org/abs/2502.04512) [[PDF]](/files/safety_is_essential_in_open_ended_ai.pdf)
---

AI advancements have been significantly driven by a combination of foundation models and curiosity-driven learning aimed at increasing capability and adaptability. A growing area of interest within this field is Open-Endedness - the ability of AI systems to continuously and autonomously generate novel and diverse artifacts or solutions. This has become relevant for accelerating scientific discovery and enabling continual adaptation in AI agents. This position paper argues that the inherently dynamic and self-propagating nature of Open-Ended AI introduces significant, underexplored risks, including challenges in maintaining alignment, predictability, and control. This paper systematically examines these challenges, proposes mitigation strategies, and calls for action for different stakeholders to support the safe, responsible and successful development of Open-Ended AI. 

[Article](https://arxiv.org/abs/2502.04512){:target="_blank"}   [Download PDF](/files/safety_is_essential_in_open_ended_ai.pdf){:target="_blank"}

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@article{sheth2025safety,
  title={Safety is Essential for Responsible Open-Ended Systems},
  author={Sheth, Ivaxi and Wehner, Jan and Abdelnabi, Sahar and Binkyte, Ruta and Fritz, Mario},
  journal={arXiv preprint arXiv:2502.04512},
  year={2025}
}
</code></pre>
</div>

<style>
.citation-container {
  position: relative;
  margin: 1em 0;
}

.copy-button {
  position: absolute;
  top: 5px;
  right: 5px;
  padding: 5px 10px;
  background-color: #f8f9fa;
  border: 1px solid #dee2e6;
  border-radius: 4px;
  cursor: pointer;
  font-size: 0.9em;
  transition: all 0.2s ease;
}

.copy-button:hover {
  background-color: #e9ecef;
}

.bibtex {
  background-color: #f8f9fa;
  padding: 15px;
  border-radius: 4px;
  border: 1px solid #dee2e6;
  margin: 0;
  white-space: pre-wrap;
  line-height: 1.5;
  font-family: monospace;
}

pre {
  white-space: pre-wrap;
  word-wrap: break-word;
  margin: 0;
}

code {
  display: block;
}
</style>

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