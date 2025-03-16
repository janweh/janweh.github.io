---
title: "Immunization against harmful fine-tuning attacks"
type: "publication"
category: journal
permalink: /publication/immunization_against_harmful_finetuning
excerpt: |
    Domenic Rosati, **Jan Wehner**, Kai Williams, Lukasz Bartoszcze, Hassan Sajjad, Frank Rudzicz in _Findings of the Association for Computational Linguistics: EMNLP 2024_, 2024

    LLMs can be fine-tuned with harmful data to remove their safeguards. We formalize the problem and set out conditions for a solution.

    [[Article]](https://aclanthology.org/2024.findings-emnlp.301/) [[PDF]](/files/immunization_against_harmful_finetuning.pdf)
---

Large Language Models (LLMs) are often trained with safety guards intended to prevent harmful text generation. However, such safety training can be removed by fine-tuning the LLM on harmful datasets. While this emerging threat (harmful fine-tuning attacks) has been characterized by previous work, there is little understanding of how we should proceed in constructing and validating defenses against these attacks especially in the case where defenders would not have control of the fine-tuning process. We introduce a formal framework based on the training budget of an attacker which we call “Immunization” conditions. Using a formal characterisation of the harmful fine-tuning problem, we provide a thorough description of what a successful defense must comprise of and establish a set of guidelines on how rigorous defense research that gives us confidence should proceed.

[Article](https://aclanthology.org/2024.findings-emnlp.301/){:target="_blank"}   [Download PDF](/files/immunization_against_harmful_finetuning.pdf){:target="_blank"}

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@inproceedings{rosati-etal-2024-immunization,
    title = "Immunization against harmful fine-tuning attacks",
    author = "Rosati, Domenic  and
      Wehner, Jan  and
      Williams, Kai  and
      Bartoszcze, Lukasz  and
      Sajjad, Hassan  and
      Rudzicz, Frank",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2024",
    year = "2024",
    publisher = "Association for Computational Linguistics",
}</code></pre>
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
