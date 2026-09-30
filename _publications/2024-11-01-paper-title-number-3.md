---
title: "Immunization against harmful fine-tuning attacks"
type: "publication"
category: journal
permalink: /publication/immunization_against_harmful_finetuning
venue: "Findings of EMNLP"
authors: "Domenic Rosati, **Jan Wehner**, Kai Williams, Lukasz Bartoszcze, Hassan Sajjad, Frank Rudzicz"
excerpt: "LLMs can be fine-tuned with harmful data to remove their safeguards. We formalize the problem and set out conditions for a solution."
links:
  - label: "Article"
    url: "https://aclanthology.org/2024.findings-emnlp.301/"
  - label: "PDF"
    url: "/files/immunization_against_harmful_finetuning.pdf"
---

Large Language Models (LLMs) are often trained with safety guards intended to prevent harmful text generation. However, such safety training can be removed by fine-tuning the LLM on harmful datasets. While this emerging threat (harmful fine-tuning attacks) has been characterized by previous work, there is little understanding of how we should proceed in constructing and validating defenses against these attacks especially in the case where defenders would not have control of the fine-tuning process. We introduce a formal framework based on the training budget of an attacker which we call “Immunization” conditions. Using a formal characterisation of the harmful fine-tuning problem, we provide a thorough description of what a successful defense must comprise of and establish a set of guidelines on how rigorous defense research that gives us confidence should proceed.

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
