---
title: "Representation Noising: A Defence Mechanism Against Harmful Finetuning"
type: "publication"
category: journal
permalink: /publication/representation_noising
venue: "NeurIPS"
authors: "Domenic Rosati, **Jan Wehner**, Kai Williams, Łukasz Bartoszcze, David Atanasov, Robie Gonzales, Subhabrata Majumdar, Carsten Maple, Hassan Sajjad, Frank Rudzicz"
excerpt: "We propose Representation Noising which prevents harmful fine-tuning by removing harmful representations."
links:
  - label: "Article"
    url: "https://proceedings.neurips.cc/paper_files/paper/2024/hash/172be8b0b88fc2b4aee74237d43f8c04-Abstract-Conference.html"
  - label: "PDF"
    url: "/files/NeurIPS-2024-representation-noising-a-defence-mechanism-against-harmful-finetuning-Paper-Conference.pdf"
---

Releasing open-source large language models (LLMs) presents a dual-use risk since bad actors can easily fine-tune these models for harmful purposes. Even without the open release of weights, weight stealing and fine-tuning APIs make closed models vulnerable to harmful fine-tuning attacks (HFAs). While safety measures like preventing jailbreaks and improving safety guardrails are important, such measures can easily be reversed through fine-tuning. In this work, we propose Representation Noising (RepNoise), a defence mechanism that operates even when attackers have access to the weights. RepNoise works by removing information about harmful representations such that it is difficult to recover them during fine-tuning. Importantly, our defence is also able to generalize across different subsets of harm that have not been seen during the defence process as long as they are drawn from the same distribution of the attack set. Our method does not degrade the general capability of LLMs and retains the ability to train the model on harmless tasks. We provide empirical evidence that the efficacy of our defence lies in its depth: the degree to which information about harmful representations is removed across all layers of the LLM. We also find areas where RepNoise still remains ineffective and highlight how those limitations can inform future research.

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
