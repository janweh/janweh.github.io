---
title: "Taxonomy, Opportunities, and Challenges of Representation Engineering for Large Language Models"
type: "publication"
category: journal
permalink: /publication/representation_engineering
excerpt: |
    **Jan Wehner**, Sahar Abdelnabi, Daniel Tan, David Krueger, Mario Fritz in _arXiv preprint_, 2025

    This survey paper reviews the literature on Representation Engineering, a technique for controlling LLMs through their internal representations. We set out a unifying taxonomy, describe methods and applications and showcase weaknesses and opportunities.

    [[Article]](https://arxiv.org/abs/2502.19649) [[PDF]](/files/representation_engineering.pdf)
---

Representation Engineering (RepE) is a novel paradigm for controlling the behavior of LLMs. Unlike traditional approaches that modify inputs or fine-tune the model, RepE directly manipulates the model's internal representations. As a result, it may offer more effective, interpretable, data-efficient, and flexible control over models' behavior. We present the first comprehensive survey of RepE for LLMs, reviewing the rapidly growing literature to address key questions: What RepE methods exist and how do they differ? For what concepts and problems has RepE been applied? What are the strengths and weaknesses of RepE compared to other methods? To answer these, we propose a unified framework describing RepE as a pipeline comprising representation identification, operationalization, and control. We posit that while RepE methods offer significant potential, challenges remain, including managing multiple concepts, ensuring reliability, and preserving models' performance. Towards improving RepE, we identify opportunities for experimental and methodological improvements and construct a guide for best practices. 

[Article](https://arxiv.org/abs/2502.19649){:target="_blank"}   [Download PDF](/files/representation_engineering.pdf){:target="_blank"}

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@article{wehner2025taxonomy,
  title={Taxonomy, Opportunities, and Challenges of Representation Engineering for Large Language Models},
  author={Wehner, Jan and Abdelnabi, Sahar and Tan, Daniel and Krueger, David and Fritz, Mario},
  journal={arXiv preprint arXiv:2502.19649},
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