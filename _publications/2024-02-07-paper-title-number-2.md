---
title: "Explaining Learned Reward Functions with Counterfactual Trajectories"
type: "publication"
category: journal
permalink: /publication/explaining_learned_reward_functions
excerpt: |
    **Jan Wehner**, Frans Oliehoek, Luciano Cavalcante Siebert forthcoming in _AIEB workshops at ECAI 2024_, 2024

    We propose a method for explaining reward functions by showing the rewards given to counterfactual trajectories.

    [[Article]](https://arxiv.org/abs/2402.04856) [[PDF]](/files/explaining_learned_reward_functions.pdf)
---

Learning rewards from human behaviour or feedback is a promising approach to aligning AI systems with human values but fails to consistently extract correct reward functions. Interpretability tools could enable users to understand and evaluate possible flaws in learned reward functions. We propose Counterfactual Trajectory Explanations (CTEs) to interpret reward functions in reinforcement learning by contrasting an original with a counterfactual partial trajectory and the rewards they each receive. We derive six quality criteria for CTEs and propose a novel Monte-Carlo-based algorithm for generating CTEs that optimises these quality criteria. Finally, we measure how informative the generated explanations are to a proxy-human model by training it on CTEs. CTEs are demonstrably informative for the proxy-human model, increasing the similarity between its predictions and the reward function on unseen trajectories. Further, it learns to accurately judge differences in rewards between trajectories and generalises to out-of-distribution examples. Although CTEs do not lead to a perfect understanding of the reward, our method, and more generally the adaptation of XAI methods, are presented as a fruitful approach for interpreting learned reward functions.

[Article](https://arxiv.org/abs/2402.04856){:target="_blank"}   [Download PDF](/files/explaining_learned_reward_functions.pdf){:target="_blank"}

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
