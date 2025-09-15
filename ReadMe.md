# Research Plan

**Model discovery & shortlisting.**  
I will be using and comparing 4 LLM's —  

**ChatGPT (OpenAI)** <img src="https://raw.githubusercontent.com/microsoft/ML-For-Beginners/main/3-Web-App/04-ai-openai/images/openai-logo.png" width="26" />,  
**Gemini (Google DeepMind)** <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Google_Gemini_logo.png/512px-Google_Gemini_logo.png" width="26" />,  
**Claude (Anthropic)** <img src="https://avatars.githubusercontent.com/u/110213622?s=200&v=4" width="26" />,  
**Perplexity AI** <img src="https://raw.githubusercontent.com/perplexity-ai/.github/main/profile/perplexity-logo.png" width="26" />.  

I am selecting these models due to their established capability to process natural language, producing context-based explanations, and responding to Socratic-style prompts. The shortlist was constructed based on the following:  
(a) overall-purpose reasoning power both in code and natural language,  
(b) accessibility for research/education purposes via APIs or web interfaces,  
(c) support for multi-turn conversation and large contexts (which is useful for complete code files + instructions), and  
(d) evidence

## Models tested and why
I tested **ChatGPT (OpenAI)**, **Gemini (Google DeepMind)**, **Claude (Anthropic)**, and **Perplexity AI**. These are top-edge frontier LLMs available through API or web interfaces, selected since they already show excellent reasoning and conversational capabilities. They embody various design approaches:
- ChatGPT — instruction-following and broad ecosystem support.
- Gemini — multimodal integration and Google search grounding strengths.
- Claude — alignment-oriented, safe, and large context windows.
- Perplexity — retrieval-augmented, aiming to generate grounded, resource-dense answers.

## What characterizes a model as appropriate for high-level competence analysis?
- Can **describe reasoning in natural language** and translate code to concepts.
- **Following instructions** to produce Socratic questions rather than direct answers.
- **Context size** to store student code + test outcomes.
- **Grounding ability** (e.g., Perplexity’s retrieval, Gemini’s integration with search).  
- **Safety/alignment** so prompts don’t “give away” solutions or mislead students.  

## How to test whether a model generates meaningful prompts
1. Provide each model with the same set of student Python code examples.  
2. Ask: *“Generate three diagnostic, non-solution prompts to help the student reflect.”*
3. Compare outputs to a gold set composed by teachers.
4. Teachers rate on: diagnosticity, solution-neutrality, conceptual focus, and pedagogical depth.
5. Students test in small pilots with model vs baseline hints; measure post-test learning gains.

## Trade-offs: accuracy vs interpretability vs cost
- **Accuracy**: ChatGPT and Gemini tend to provide the most accurate reasoning; Claude excels in safe, long-context pedagogy; Perplexity is best at grounding with citations.
- **Interpretability**: Claude and Perplexity are more transparent (citations, thoughtful phrasing), whereas ChatGPT and Gemini might "hallucinate" but explain better.
- **Cost & access**: Perplexity (free plan) is cheapest; ChatGPT and Claude API calls cost moderate; Gemini’s cost depends on API tier. Interpretability often trades off with breadth of reasoning.  

## Why this evaluation matters — strengths and limitations
- **ChatGPT**: excellent at instruction-following, but can sometimes “give the solution” instead of scaffolding.
- **Gemini**: excellent at reasoning with grounding, but less clear in citations than Perplexity.
- **Claude**: safest in alignment, extremely long context, but possibly too cautious and not delve sufficiently into technical interrogation.
- **Perplexity**: good citations/grounding, but poorer at Socratic pedagogy than the others.

**Conclusion:**
- For **pedagogical prompt generation**, **Claude** is best aligned with non-solution scaffolding.
- For **technical accuracy**, **ChatGPT/Gemini** tend to excel.
- For **interpretability**, **Perplexity** contributes value through citations.
- The best approach could be a **hybrid pipeline** that uses Claude for scaffolding questions and ChatGPT/Gemini for code reasoning depth.

## Evaluation & validation protocol (Python student code use case)
For each model, I will conduct staged validation:  
1. *Static checks* — present representative student Python code snippets (correct, partially-correct, misconception-prone) and record the model's feedback.  
2. *Prompt-generation task* — instruct the model to produce scaffolding prompts that invite deeper thought without exposing full solutions.  
3. *Comparative analysis* — score the prompts for clarity, diagnosticity, and whether they are solution-neutral.  
4. *Human evaluation* — have instructors rate the four models' output.  
5. *Student pilot* — A/B test whether students instructed by model prompts perform better post-test scores than those instructed by baseline hints.  


