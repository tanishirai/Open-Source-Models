# 📘 Python Screening Task 3: Evaluating Open Source Models for Student Competence Analysis  

 

## Research Plan  

 

I will identify candidate open-source code-specialized LLMs by exploring model hubs such as Hugging Face, BigCode, and Meta, focusing on models that (a) are trained or fine-tuned specifically for Python, (b) have permissive licensing for academic or research use, and (c) are practical to run locally at the 7B–15B parameter scale. The most promising candidates are Meta’s **Code Llama – Python** and BigCode’s **StarCoder2**, since both are open-source, designed for code understanding, and widely tested in research and education contexts.  

 

For evaluation, I will create a small benchmark of student-written Python programs that include correct solutions, partially correct code, and common misconception-driven errors. The evaluation will test three capabilities: (1) **analysis** — whether the model can identify gaps or misconceptions, (2) **prompt generation** — whether the model can create scaffolded, non-solution prompts to probe conceptual understanding, and (3) **pedagogical safety** — whether the model avoids giving direct solutions and instead encourages deeper learning. Effectiveness will be assessed using a mix of automatic metrics (error detection, prompt relevance) and human judgment from educators (clarity, usefulness, and alignment with learning objectives). All results and documentation will be made reproducible via this repository.  

 

---

 

## Reasoning  

 

**1. What makes a model suitable for high-level competence analysis?**  

A suitable model must (a) understand Python code semantics and error patterns, (b) be instruction-tuned to produce controlled outputs (diagnostic prompts rather than full answers), and (c) be practical to run on limited resources. Code-specialized LLMs like Code Llama (Python) meet these requirements.  

 

**2. How would you test whether a model generates meaningful prompts?**  

By using annotated student code samples and checking if the generated prompts encourage conceptual reflection (e.g., *“What happens if the loop runs zero times?”*) rather than providing the fix directly. Educators can rate prompts on clarity, usefulness, and non-solution framing.  

 

**3. What trade-offs exist between accuracy, interpretability, and cost?**  

Large models (e.g., 34B) provide more accuracy but are expensive to run and harder to deploy in classrooms. Smaller models (7B) are affordable and interpretable but may miss subtle reasoning gaps. Instruction-tuned checkpoints improve safety and controllability but sometimes reduce raw accuracy.  

 

**4. Which model did you choose and why?**  

I selected **Code Llama – Python** as the primary model. Its strengths include Python specialization, flexible parameter sizes for cost–accuracy trade-offs, and instruction-tuned variants for controlled outputs. Its main limitation is computational cost at larger scales, along with the risk of revealing full solutions if not carefully prompted.  

 

---
