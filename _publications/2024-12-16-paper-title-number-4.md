---
title: "Representation Noising: A Defence Mechanism Against Harmful Finetuning"
type: "publication"
category: journal
permalink: /publication/representation_noising
excerpt: |
    Domenic Rosati, **Jan Wehner**, Kai Williams, Łukasz Bartoszcze, David Atanasov, Robie Gonzales, Subhabrata Majumdar, Carsten Maple, Hassan Sajjad, Frank Rudzicz in _NeurIPS_, 2024

    We propose Representation Noising which prevents harmful fine-tuning by removing harmful representations.

    [[Article]](https://proceedings.neurips.cc/paper_files/paper/2024/hash/172be8b0b88fc2b4aee74237d43f8c04-Abstract-Conference.html) [[PDF]](/files/NeurIPS-2024-representation-noising-a-defence-mechanism-against-harmful-finetuning-Paper-Conference.pdf)
---

Releasing open-source large language models (LLMs) presents a dual-use risk since bad actors can easily fine-tune these models for harmful purposes. Even without the open release of weights, weight stealing and fine-tuning APIs make closed models vulnerable to harmful fine-tuning attacks (HFAs). While safety measures like preventing jailbreaks and improving safety guardrails are important, such measures can easily be reversed through fine-tuning. In this work, we propose Representation Noising (RepNoise), a defence mechanism that operates even when attackers have access to the weights. RepNoise works by removing information about harmful representations such that it is difficult to recover them during fine-tuning. Importantly, our defence is also able to generalize across different subsets of harm that have not been seen during the defence process as long as they are drawn from the same distribution of the attack set. Our method does not degrade the general capability of LLMs and retains the ability to train the model on harmless tasks. We provide empirical evidence that the efficacy of our defence lies in its depth: the degree to which information about harmful representations is removed across all layers of the LLM. We also find areas where RepNoise still remains ineffective and highlight how those limitations can inform future research.

[Article](https://proceedings.neurips.cc/paper_files/paper/2024/hash/172be8b0b88fc2b4aee74237d43f8c04-Abstract-Conference.html){:target="_blank"}   [Download PDF](/files/NeurIPS-2024-representation-noising-a-defence-mechanism-against-harmful-finetuning-Paper-Conference.pdf){:target="_blank"}

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@article{rosati2024representation,
  title={Representation Noising: A Defence Mechanism Against Harmful Finetuning},
  author={Rosati, Domenic and Wehner, Jan and Williams, Kai and Bartoszcze, Lukasz and Gonzales, Robie and Majumdar, Subhabrata and Sajjad, Hassan and Rudzicz, Frank and others},
  journal={Advances in Neural Information Processing Systems},
  volume={37},
  pages={12636--12676},
  year={2024}
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