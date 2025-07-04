# Graph_Visualization

This repository visualizes **linked argumentative structures** — claims and premises — as interactive graphs using [Cytoscape.js](https://js.cytoscape.org/). It is designed to work alongside the [argument_linking_llm](https://github.com/Horizontal-Labs/synapse-sparks/blob/main/LLM_Linking.ipynb) 

---

##  Overview

The purpose of this repo is to:

- Parse structured premise–claim link data from `output.json`
- Convert it into Cytoscape-compatible format (`nodes` and `edges`)
- Render it as an interactive, color-coded argument graph

This enables dynamic, web-based argument visualization.
---

##  How It Works

1. **Input**: JSON file from an LLM output (e.g. `output.json`)
2. **Conversion**: Python script transforms it into Cytoscape elements
3. **Visualization**: A complete `graph.html` is generated

---

##  Input Format

The input `output.json` file must have the following structure:

```json
{
  "linked_premises": [
    {
      "premise_text": "EVs have zero tailpipe emissions.",
      "stance": "pro",
      "linked_claim_text": "Electric vehicles are better for the environment."
    },
    {
      "premise_text": "Battery mining damages ecosystems.",
      "stance": "con",
      "linked_claim_text": "Electric vehicles are better for the environment."
    },
    {
      "premise_text": "Remote workers report fewer distractions.",
      "stance": "pro",
      "linked_claim_text": "Remote work improves productivity."
    },
    {
      "premise_text": "AI-generated art lacks intentional creativity.",
      "stance": "con",
      "linked_claim_text": "AI-generated art is true creativity."
    },
    {
      "premise_text": "Some premises are too vague to match any claim.",
      "stance": "pro",
      "linked_claim_text": null
    }
  ]
}



