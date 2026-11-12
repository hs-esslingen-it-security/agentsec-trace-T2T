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

### 📚 Sources

The mapping builds on the following sources. All source frameworks and tools remain the property of their respective owners and are subject to their own license terms; please consult the originals. Cut-off dates: threat and control sources as published by **July 2026**, tool documentation as available by **August 2026**.

#### Threat sources
| Source | Link |
| --- | --- |
| MITRE ATLAS | https://atlas.mitre.org |
| Cisco Integrated AI Security and Safety Framework (2026) | https://www.cisco.com/site/us/en/learn/topics/artificial-intelligence/ai-security-safety-framework.html |
| OWASP Top 10 for Agentic Applications (2026) | https://genai.owasp.org |
| NIST AML: Adversarial Machine Learning Taxonomy, NIST AI 100-2e2025 | https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-2e2025.pdf |

#### Control and governance sources
| Source | Link |
| --- | --- |
| AIUC-1 | https://standard.aiuc-1.com/security |
| CSA AI Controls Matrix (AICM) v1.1 | https://cloudsecurityalliance.org/artifacts/ai-controls-matrix-v1-1 |
| MITRE ATLAS Mitigations | https://atlas.mitre.org |
| NIST AI Risk Management Framework 1.0 (NIST AI 100-1) | https://airc.nist.gov/airmf-resources/airmf/ |
| EU AI Act, Regulation (EU) 2024/1689 | http://data.europa.eu/eli/reg/2024/1689/oj |
| ISO/IEC 42001:2023 and ISO/IEC 27001:2022 | https://www.iso.org |
| BSI AIC4 (2021) and BSI C5:2026 | https://www.bsi.bund.de |

#### Assessed tools
| Category | Tools |
| --- | --- |
| Pre-deployment testing | [Garak](https://github.com/NVIDIA/garak), [Promptfoo](https://github.com/promptfoo/promptfoo), [HiveTrace.red](https://github.com/HiveTrace/HiveTraceRed), [Avenlis SandStrike](https://github.com/StateraSolutions/avenlis-sandstrike), [LLM-RTK](https://github.com/koraydns/llm-rtk), [Agentic Radar](https://github.com/splx-ai/agentic-radar) |
| Runtime guardrail libraries | [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails), [LLM Guard](https://github.com/protectai/llm-guard), [Guardrails AI](https://github.com/guardrails-ai/guardrails), [LlamaFirewall](https://github.com/meta-llama/PurpleLlama/tree/main/LlamaFirewall), [ModelArmor](https://docs.kubearmor.io/kubearmor/use-cases/modelarmor), [Edictum](https://github.com/edictum-ai/edictum), [tenuo](https://github.com/tenuo-ai/tenuo) |
| Proxy-based gateways | [OpenGuardrails](https://github.com/openguardrails/openguardrails), [LiteLLM](https://github.com/BerriAI/litellm), [Plano](https://github.com/katanemo/plano), [Apache APISIX](https://github.com/apache/apisix), [TrustGate](https://github.com/NeuralTrust/TrustGate), [Pipelock](https://github.com/luckyPipewrench/pipelock), [MCP Secure Gateway](https://github.com/lasso-security/mcp-gateway), [Pomerium](https://github.com/pomerium/pomerium) |

Tool assessments are based on the official documentation and repositories available at the cut-off date; later changes are not reflected.


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
