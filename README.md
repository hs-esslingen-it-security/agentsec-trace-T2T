<div align="center">

# From Threats to Tools: A Traceable Mapping for Agentic AI Security

**Supplementary research artifacts**

Hannah Meinhardt · Sabrina Kaniewski · Markus Enzweiler · Tobias Heer


 **Esslingen University of Applied Sciences** 

</div>

---

<br>

Securing agentic AI applications requires connecting known security threats and control requirements to technical mechanisms that can be implemented in practice. However, existing threat taxonomies and security frameworks do not directly identify which security tools address which threats and controls.

We address this gap through a traceable **Threat-to-Control-to-Tool mapping**. It consolidates published threat-to-control relationships, derives technical security requirements, and assesses the documented capabilities of 21 selected open-source security tools across three categories: pre-deployment testing tools, runtime guardrail libraries, and proxy-based gateways.

This repository provides the underlying workbooks to make the mapping and its coverage analysis transparent, reproducible, and extensible. Readers can use them to:

- Trace relationships between threats, security controls, technical requirements, and tool capabilities.
- Compare the documented security functionalities of the selected tools.
- Identify coverage gaps, overlaps, and complementary tool combinations.
- Extend the mapping to additional security tools or requirements.

**Scope:** The tool assessments represent documentation-based technical capability coverage, not empirically verified protection effectiveness. Coverage does not imply that a threat is eliminated or that regulatory compliance is achieved.

## 📖 Mapping Workbooks

| File | Description |
| --- | --- |
| [`Threat_to_Control_to_Tool_Mapping.xlsx`](Threat_to_Control_to_Tool_Mapping.xlsx) | Connects published threat-to-control relationships with technical requirements and tool coverage. Includes architectural-layer classifications and aggregated coverage across threats and controls. |
| [`Requirement_to_Tool_Mapping.xlsx`](Requirement_to_Tool_Mapping.xlsx) | Assesses 21 open-source security tools against the derived technical requirements. Documents tool-specific mechanisms, normalized functionality families, and full or partial requirement fulfillment. |

### `Threat_to_Control_to_Tool_Mapping.xlsx`

| Sheet | Contents |
| --- | --- |
| `Threat-to-Control-to-Tool Mapping` | Main mapping matrix containing threats, published relationships to security controls, architectural-layer assignments (Perception, Reasoning, Memory, or Action), derived technical requirements, and propagated technical coverage. Marked intersections represent retained published relationships rather than newly inferred mappings. |
| `Evaluation` | Selected coverage results and their references to the corresponding analyses and visualizations in the publication. |
| `Calculation` | Supporting calculations and aggregations for threat-level, control-level, and architectural-layer coverage. |

###  `Requirement_to_Tool_Mapping.xlsx`

| Sheet | Contents |
| --- | --- |
| `Requirement-to-Tool Mapping` | Technical requirements assessed against 21 open-source tools. Populated cells identify the documented functionality family and tool-specific mechanism, with fulfillment classified as full or partial. Empty cells indicate that no supporting mechanism was identified. |
| `Evaluation` | Summary results supporting the publication's analysis, including requirement coverage, tool-category contributions, tool dependencies, and complementary tool combinations. |
| `Calculation` | Supporting calculations for requirement coverage, tool comparisons, residual gaps, and tool-portfolio combinations. |

## 🛠️ Supplementary Proof-of-Value Implementation

The [`Proof-of-Value Implementation`](Proof-of-Value%20Implementation/) directory contains supplementary materials from a separate proof-of-value study involving six security tools: Garak, Promptfoo, LLM Guard, Guardrails AI, LlamaFirewall, and NeMo Guardrails.

The study implemented and evaluated these tools in an agentic AI application environment, examining adversarial testing, runtime attack prevention, and the impact on legitimate interactions.

**This experimental study is not part of the publication's documentation-based mapping assessment.** It is provided as supplementary material and referenced in the publication's *Threats to Validity* section to distinguish documented capabilities from experimentally observed tool behavior.

## ✍️ Citation

If you use the mapping artifacts in your research, please cite the accompanying publication:

```bibtex
@misc{meinhardtThreatsToTools,
    author = {Meinhardt, Hannah and Kaniewski, Sabrina and Enzweiler, Markus and Heer, Tobias},
    title = {{From Threats to Tools: A Traceable Mapping for Agentic AI Security}},
    year = {2026},
    note = {Under Review}
}
```
