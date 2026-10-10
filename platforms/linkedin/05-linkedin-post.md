# Beyond the Answer: Designing AI Support That Advances the Case

**Subtitle:** Evidence, deterministic rules, and human handoff

**Summary:** A B2B refund design reference for enterprise AI delivery.

“We initiated the refund. The buyer still hasn't received it.”

An AI assistant can explain refund policies. But can it retrieve the right transaction, interpret the evidence, and hand over an unresolved case without losing context?

I am documenting this question in Enterprise Support Agent, an open-source design reference for enterprise AI delivery.

The proposed workflow separates four responsibilities:

• LLMs interpret messages and collect missing information.
• Read-only tools retrieve transaction and account data.
• Deterministic rules control routing and allowed actions.
• Humans investigate exceptions and handle account writes.

The most important distinction: “status retrieved” is not “problem resolved.”

The refund case includes Discovery, Workflow, Architecture, Risks, and Acceptance documents. Agent code drafts and mock connectors exist, but this publication does not claim a validated runnable demo, completed evaluation suite, or production ROI. The proposed 160 test cases remain a plan.

For FDEs and AI solutions architects, the delivery question is: what evidence would make this workflow acceptable to the support team?

If you work in enterprise technical support, SaaS service operations, or AI implementation, comment or message **LI-POST** with an anonymized example: customer request, systems involved, human decision point, and resolution criteria.

I am looking for real workflows to discuss, rather than generic automation targets.

Design reference:
https://github.com/bob798/enterprise-support-agent/tree/main/examples/refund-not-received

#EnterpriseAI #FDE #AISolutions #AIAgents #CustomerSupport
