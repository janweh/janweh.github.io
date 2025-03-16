---
title: "On robust vs fast solving of qualitative constraints"
type: "publication"
category: journal
permalink: /publication/robust_vs_fast_solving_qualitative_constratins
excerpt: |
    **Jan Wehner**, Michael Sioutis, Diedrich Wolter in _Journal of Heuristics_, 2023

    This paper introduces the notion of Robustness to Qualitative Contraint Networks and finds a tradeoff between speed and robustness in heuristics for solving QCNs.

    [[Article]](https://link.springer.com/article/10.1007/s10732-023-09517-8) [[PDF]](/files/On_robust_vs_fast_solving_qualitative_constraints.pdf)
---

Qualitative Constraint Networks (QCNs) comprise a Symbolic AI framework for representing and reasoning about spatial and temporal information via the use of natural disjunctive qualitative relations, e.g., a constraint can be of the form "Task A is scheduled after or during Task C". In qualitative constraint-based reasoning, the state-of-the-art approach to tackle a given QCN consists in employing a backtracking algorithm, where the branching decisions during search and the refinement of the QCN are governed by certain heuristics that have been proposed in the literature. Although there has been plenty of research on how these heuristics compare and behave in terms of checking the satisfiability of a QCN fast, to the best of our knowledge there has not been any study on how they compare and behave in terms of obtaining a tractable refinement of a QCN that is also robust. In brief, a robust refinement of a QCN can be primarily seen as one that retains as many qualitative solutions as possible, e.g., the configuration "Task A is scheduled after or during Task C" is more robust than "Task A is scheduled after Task C". Here, we make such a preliminary comparison and evaluation with respect to prominent heuristics in the literature, and reveal that there exists a trade-off between fast and robust solving of QCNs for datasets consisting of instances of Allen's Interval Algebra and Region Connection Calculus. Furthermore, we investigate reasons for the existence of this trade-off and find that more aggressive heuristics are more efficient at the cost of producing less robust refinements. 

[Article](https://link.springer.com/article/10.1007/s10732-023-09517-8){:target="_blank"}   [Download PDF](/files/On_robust_vs_fast_solving_qualitative_constraints.pdf){:target="_blank"}

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@article{wehner2023robust,
  title={On robust vs fast solving of qualitative constraints},
  author={Wehner, Jan and Sioutis, Michael and Wolter, Diedrich},
  journal={Journal of Heuristics},
  volume={29},
  number={4},
  pages={461--485},
  year={2023},
  publisher={Springer}
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
