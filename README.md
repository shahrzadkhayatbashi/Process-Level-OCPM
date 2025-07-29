
# 📚 Process-Level Aggregation and Analysis of Object-Centric Event Data

This repository provides supplementary materials for the scientific paper:

**"Process-Level Aggregation and Analysis of Object-Centric Event Data"**  
*Shahrzad Khayatbashi, Majid Rafiei, Jiayuan Chen, and Amin Jalali*  
Submitted to the [10th International Workshop on Process Querying, Manipulation, and Intelligence (PQMI 2025)](http://processquerying.com/pqmi2025/)

---

## 🎯 Objective

We introduce a formal framework and supporting tools for embedding **analyst-defined process scopes** into OCEL (Object-Centric Event Log) data. This approach enables:

- Structured representation of multiple, coexisting processes
- Fine-grained and coarse-grained process aggregation
- Multi-level abstraction for modular process analysis
- Systematic discovery of inter-process interactions and coordination patterns

## Motivation

The figure below illustrates how stakeholders may define overlapping or nested process scopes based on their roles and perspectives. Such definitions are inherently subjective, yet essential for interpreting complex event data. In the absence of explicit scoping, analysts often rely on manual filtering to isolate relevant subsets, which is ad hoc and limits systematic exploration of process interactions, overlaps, and alignment with organizational structures.

To address this, we propose embedding explicit, analyst-defined process scopes into OCEL, while maintaining full compatibility with the OCEL 2.0 standard. This enables a structured representation of multiple, coexisting processes within a single log. Our approach supports both fine-grained and coarse-grained scoping, allowing analysts to define local subprocesses and aggregate them into higher-level processes. For example, analysts may annotate segments of the event log with scopes $P_1$ and $P_2$, and subsequently define a broader scope $P_3$ that encompasses both, thereby capturing a higher level of abstraction.

This capability reflects the hierarchical nature of organizational process landscapes, where operational staff focus on local tasks and managers evaluate performance at the strategic level. By explicitly linking low-level and high-level scopes, analysts can traverse between different levels of abstraction. This facilitates drill-down and roll-up analysis, and supports the exploration of value chains, process handovers, and inter-process dependencies.

![Process Abstractions](./images/Process%20Abstractions.png)

## 🛠️ Tool Support

Our approach is supported by two open-source tools:

- [Procellar](https://github.com/hudsonjychen/procellar): Define and embed process scopes
- [Business Execution Graph](https://github.com/hudsonjychen/business-execution-graph): Visualize process interactions through shared objects

We demonstrate the application of these tools on a public OCEL logistics log:  
🔗 https://ocel-standard.org/event-logs/simulations/logistics/

## 📘 Further Information

These tools enhance the analytical power of object-centric process mining by combining expert-driven scoping with scalable, data-driven insights, and by supporting analysis at multiple levels of abstraction. We demonstrate the application of our approach and toolset on an openly available OCEL logistics log. Details can be found in the following pages:

- 📝 [Summary of the log](./pages/log-summary.md)
- ✍️ [Enriching OCEL with process scope definition](./pages/enriching-with-pocel.md)
- 🔍 [Discovering interactions among processes](./pages/discovering-interactions.md)
