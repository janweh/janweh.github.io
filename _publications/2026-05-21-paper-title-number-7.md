---
title: "Detecting Offensive Cyber Agents: A Detection-in-Depth Approach"
type: "publication"
category: journal
permalink: /publication/detecting_offensive_cyber_agents
venue: "IAPS Report"
authors: "Matt Mittelsteadt, Jam Kraprayoon, Robin Staes-Polet, Oskar Galeev, **Jan Wehner**, Christopher Covino, Shaun Ee"
excerpt: "AI agents can now orchestrate cyberattacks, increasing their speed, scale, and autonomy while lowering costs. This report frames the offensive cyber agent detection challenge, introduces *detection-in-depth* as a strategic framework for policymakers and defenders, and proposes five concrete detection mechanisms."
links:
  - label: "Report"
    url: "https://www.iaps.ai/research/detecting-offensive-cyber-agents"
  - label: "arXiv"
    url: "https://arxiv.org/abs/2605.21956"
---

Artificial Intelligence (AI) agents can now orchestrate cyberattacks. This development is already increasing the speed and scale of cyber attacks, decreasing attack costs, and improving the operational autonomy of cyber capabilities. To defend against these emerging threats, actors must first develop the capability to detect them. This report frames the offensive cyber agent detection challenge by outlining the coming detection gap between offensive cyber agents and traditional cyber capabilities; introducing detection-in-depth, a strategic framework to guide policymakers and defenders responding to this detection gap; and presents five actionable detection mechanisms to support policymakers, industry, and defenders when putting this strategic framework into practice. These include (1) Agent Identifiers for Critical Infrastructure, (2) Agent Honeypots; (3) AI-Automated Alert Analysis and Triage: systems that use AI to filter, prioritize, and interpret the growing volume of detection signals expected from autonomous cyber operations; (4) An Agentic Security Alert Standard: A reporting standard model that providers can use to communicate agentic threats, improving the speed, consistency, and actionability of reports; (5) An Agentic Cybersecurity Exchange (ACE): an institution modeled on the Global Signal Exchange that brings together model and cloud providers to detect offensive cyber agent threats at their origin point and coordinate ecosystem-wide agentic threat disruption.

Citation:

<div class="citation-container" markdown="0">
  <button class="copy-button" onclick="copyBibTeX()">Copy BibTeX</button>
  <pre><code class="bibtex" id="bibtex">@article{mittelsteadt2026detecting,
  title={Detecting Offensive Cyber Agents: A Detection-in-Depth Approach},
  author={Mittelsteadt, Matt and Kraprayoon, Jam and Staes-Polet, Robin and Galeev, Oskar and Wehner, Jan and Covino, Christopher and Ee, Shaun},
  journal={arXiv preprint arXiv:2605.21956},
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
