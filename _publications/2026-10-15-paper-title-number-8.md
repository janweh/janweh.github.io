---
title: "Honeypots for AI Agent Insider Threats"
type: "publication"
category: journal
permalink: /publication/honeypots_for_ai_agent_insider_threats
venue: "IAPS Report"
authors: "**Jan Wehner**, Jam Kraprayoon"
excerpt: "AI agents deployed inside organizations can become insider threats through mistakes, compromise or misaligned goals. This report proposes planting honeypots, decoy opportunities for harmful actions, throughout production environments to detect misbehavior, incriminate malicious agents and deter attacks, and sets out a research agenda for making them work."
links:
  - label: "Report"
    url: "https://www.iaps.ai/research/honeypots-for-ai-agent-insider-threats"
  - label: "arXiv"
    url: "https://arxiv.org/abs/2610.26664"
---

AI agents deployed inside organizations can pose an insider threat if they make mistakes, are compromised by an attacker, or pursue misaligned objectives. We propose honeypots as an AI control method to improve the security of internal agent deployments. Rather than only using honeypots for pre-deployment evaluations, defenders should plant decoy opportunities for harmful actions throughout the production environment to detect misbehavior, incriminate malicious agents, and deter attacks. Such honeypots can elicit misbehavior under real deployment conditions, identify malicious agents even if chain-of-thought monitorability degrades, provide reliable warnings about agent misbehavior to security teams, and scale cheaply to many agent instances. The presence of honeypots also introduces uncertainty about which opportunities are real, thus deterring malicious agents from attacking and reducing the rate of misbehavior. We discuss the limitations of honeypots and give reasons to expect them to remain effective as agent capabilities increase. Finally, we outline key research questions to measure and improve the effectiveness of honeypots: testing the robustness of honeypots, comparing their detection effectiveness with other monitoring methods, understanding their incrimination and deterrence effects, and building supporting infrastructure.

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@article{wehner2026honeypots,
  title={Honeypots for AI Agent Insider Threats},
  author={Wehner, Jan and Kraprayoon, Jam},
  journal={arXiv preprint arXiv:2610.26664},
  year={2026}
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
