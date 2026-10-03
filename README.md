# Evaluating Evidence-Based Reasoning on Nigeria's Fuel Price Reforms

An evaluation project examining how well an AI model reasons about economic evidence, interprets data, and handles claims about causation, inflation, and household welfare.

## About the Project

Economic issues often involve several factors happening at the same time. A change in one policy or market condition may be associated with changes in prices, household costs, government revenue, or broader economic indicators. Explaining these relationships accurately requires more than identifying facts. It requires careful use of evidence and a clear distinction between what the evidence shows and what can reasonably be inferred from it.

This project evaluates **Gemini** on that kind of reasoning using Nigeria's fuel-price reforms and their wider economic context as a case study.

Rather than testing the model on factual recall alone, I designed questions that require it to:

- assess whether evidence supports a causal claim;
- interpret inflation statistics correctly;
- distinguish macroeconomic conditions from household welfare;
- explain how the same economic shock can produce different effects;
- separate information directly supported by a source from inference;
- use sources accurately and stay within the evidence provided.

The project combines source research, question design, model testing, response evaluation, and analytical writing.

## Why This Topic?

Nigeria's fuel-price reforms provide a useful case for testing economic reasoning because several changes can occur alongside one another: petrol prices, transportation costs, inflation, household purchasing power, government revenue, and broader macroeconomic conditions.

This makes it possible to test whether a model can move beyond a simple "A happened, therefore A caused B" explanation and instead examine the evidence, competing explanations, and limits of the available data.

The project also reflects my background in **Mass Communication**, where evaluating claims, interpreting information, identifying context, and communicating evidence clearly are important parts of analytical work.

## Evaluation Questions

The model was tested with four questions, each targeting a different reasoning skill.

### Question 1 — Causal Reasoning

The first question examined whether the available evidence was sufficient to conclude that the removal of Nigeria's fuel subsidy directly caused subsequent inflation.

The model was required to distinguish between:

- temporal association;
- a plausible causal mechanism; and
- evidence strong enough to establish causation.

It was also asked to identify alternative factors that could have contributed to inflation.

### Question 2 — Interpreting Inflation Data

The second question focused on NBS inflation figures for February 2026.

The model had to explain the difference between year-on-year and month-on-month inflation and identify why a decline in the annual inflation rate does not mean that prices themselves have fallen.

### Question 3 — Macroeconomic Conditions and Household Welfare

The third question examined how improvements in macroeconomic indicators can occur alongside continued pressure on household incomes and high poverty levels.

The model was asked to explain why GDP growth or a lower inflation rate alone cannot provide a complete picture of household living standards.

### Question 4 — Competing Economic Mechanisms

The fourth question examined how higher global fuel, food, and fertilizer prices can produce different effects at the same time.

The model had to explain the different economic channels involved and show why describing such a shock as simply "good" or "bad" would leave out important context.

## Sources

The evaluation used a defined source set rather than allowing the model to draw on unrestricted information.

Sources included:

- **Reuters** — reporting on Nigeria's fuel subsidy removal, petrol prices, transportation costs, and public reactions.
- **International Monetary Fund (IMF)** — Nigeria's 2026 Article IV consultation, including discussion of global fuel, food, and fertilizer prices, government revenue, inflation, poverty, and food security.
- **World Bank** — Nigeria Development Update, April 2026, covering macroeconomic conditions and household-level economic pressures.
- **National Bureau of Statistics (NBS)** — Consumer Price Index and Premium Motor Spirit price data.

Full source details and links are available in [`sources/sources.md`](sources/sources.md).

## Testing Method

Each question was tested in a **fresh Gemini conversation** to avoid carrying information or corrections from one question into another.

The same evaluation instruction was used for each test:

> You are being evaluated on your ability to reason from evidence. Answer the question using only the sources provided in the prompt. Distinguish clearly between information directly supported by a source and your own inference. Do not introduce facts that cannot be supported by the provided sources. Where the evidence does not establish causation, say so explicitly.

For each question:

1. The source material and question were provided to Gemini.
2. The model's first complete response was retained.
3. No follow-up correction or regeneration was used.
4. The response was preserved in its original form.
5. The response was evaluated against the same rubric.

The raw responses are available in [`responses/model_responses.md`](responses/model_responses.md).

## Evaluation Framework

Responses were assessed using seven criteria:

| Criterion | What was examined |
|---|---|
| **Factual Accuracy** | Whether the response correctly represented the information in the sources |
| **Causal Reasoning** | Whether the model distinguished association, plausible mechanisms, and established causation |
| **Evidence and Source Grounding** | Whether claims were supported by the sources provided |
| **Evidence vs. Inference** | Whether the model clearly separated source-supported information from interpretation |
| **Contextual and Analytical Reasoning** | Whether the response considered relevant economic context and multiple mechanisms |
| **Instruction Adherence** | Whether the model followed the requirements of each question |
| **Clarity and Analytical Precision** | Whether the reasoning was clearly and accurately expressed |

The full rubric is available in [`evaluation/rubric.md`](evaluation/rubric.md).

## Key Findings

Across the four questions, Gemini generally produced coherent and well-structured answers.

### What it handled well

The model consistently showed an ability to:

- distinguish temporal association from causation;
- interpret year-on-year and month-on-month inflation correctly;
- recognize that lower inflation does not mean lower prices;
- separate macroeconomic performance from household welfare;
- explain multiple economic effects occurring at the same time;
- identify some of the limits of the available evidence;
- acknowledge when part of an explanation was an inference rather than a direct finding from a source.

### Where closer review was needed

The main recurring issue was **source precision**.

Several responses included explanations that were reasonable in a broader economic context but went beyond what the supplied sources directly established. For example, the model sometimes treated descriptive data as evidence for a causal mechanism or expanded a source's wording into a broader explanation.

This did not necessarily make the answers fundamentally incorrect. However, it showed why a response can sound convincing while still requiring careful checking against the underlying evidence.

The evaluation therefore placed particular emphasis on whether the model stayed within the boundaries of the information provided.

The complete evaluation is available in [`evaluation/evaluation_results.md`](evaluation/evaluation_results.md).

## Final Analysis

The evaluation showed that strong-looking answers still need to be examined at the level of individual claims.

The most useful distinction throughout the project was between:

**What the source directly says → What can reasonably be inferred → What the evidence cannot establish**

This was especially important when the model discussed causation or attempted to explain how one economic development affected another.

The final analysis of the four responses is available in [`findings/final_analysis.md`](findings/final_analysis.md).


## Skills Demonstrated

This project demonstrates practical skills in:

- AI model evaluation
- Research and source verification
- Analytical writing
- Question and prompt design
- Evidence-based reasoning
- Causal reasoning
- Statistical interpretation
- Close reading of source material
- Identifying unsupported or overstated claims
- Documentation and quality assurance
- Communicating complex information clearly

## What I Contributed

I selected and documented the source material, designed the evaluation questions, established the testing procedure, tested the model, preserved the original responses, developed the evaluation rubric, assessed the responses against the available evidence, and synthesized the findings.

The purpose was not to determine whether a particular economic policy was good or bad. The focus was on whether an AI model could reason carefully from evidence and communicate conclusions without going beyond what the sources support.

## Repository Navigation

- [Source Documentation](sources/sources.md)
- [Evaluation Questions](questions/evaluation_questions.md)
- [Raw Model Responses](responses/model_responses.md)
- [Evaluation Rubric](evaluation/rubric.md)
- [Evaluation Results](evaluation/evaluation_results.md)
- [Final Analysis](findings/final_analysis.md)


## Project Structure

```text
nigeria-economic-reasoning-evaluation/
│
├── README.md
│
├── sources/
│   └── sources.md
│
├── questions/
│   └── evaluation_questions.md
│
├── responses/
│   └── model_responses.md
│
├── evaluation/
│   ├── rubric.md
│   └── evaluation_results.md
│
└── findings/
    └── final_analysis.md


