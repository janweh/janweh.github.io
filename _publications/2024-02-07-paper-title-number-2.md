---
title: "Explaining Learned Reward Functions with Counterfactual Trajectories"
type: "publication"
category: journal
permalink: /publication/explaining_learned_reward_functions
venue: "AIEB workshops at ECAI"
authors: "**Jan Wehner**, Frans Oliehoek, Luciano Cavalcante Siebert"
excerpt: "We propose a method for explaining reward functions by showing the rewards given to counterfactual trajectories."
links:
  - label: "Article"
    url: "https://arxiv.org/abs/2402.04856"
  - label: "PDF"
    url: "/files/explaining_learned_reward_functions.pdf"
---

Learning rewards from human behaviour or feedback is a promising approach to aligning AI systems with human values but fails to consistently extract correct reward functions. Interpretability tools could enable users to understand and evaluate possible flaws in learned reward functions. We propose Counterfactual Trajectory Explanations (CTEs) to interpret reward functions in reinforcement learning by contrasting an original with a counterfactual partial trajectory and the rewards they each receive. We derive six quality criteria for CTEs and propose a novel Monte-Carlo-based algorithm for generating CTEs that optimises these quality criteria. Finally, we measure how informative the generated explanations are to a proxy-human model by training it on CTEs. CTEs are demonstrably informative for the proxy-human model, increasing the similarity between its predictions and the reward function on unseen trajectories. Further, it learns to accurately judge differences in rewards between trajectories and generalises to out-of-distribution examples. Although CTEs do not lead to a perfect understanding of the reward, our method, and more generally the adaptation of XAI methods, are presented as a fruitful approach for interpreting learned reward functions.

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@article{wehner2024explaining,
      title={Explaining Learned Reward Functions with Counterfactual Trajectories}, 
      author={Jan Wehner and Frans Oliehoek and Luciano Cavalcante Siebert},
      journal={arXiv preprint 2402.04856}
      year={2024},
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
