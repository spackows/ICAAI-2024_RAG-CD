# Content rewriting experiment
To demonstrate the impact how knowledge base content is written has on RAG solution success, we ran an experiment:
1. We extracted 189 questions about the Earth (as well as related articles and expected answers) from the [Natural Questions data set and benchmark](https://ai.google.com/research/NaturalQuestions)
2. We built a simple RAG solution to answer the questions using the extracted articles as a knowledge base
3. We rewrote portions of the articles in which answers were grounded, applying our RAG content guidelines
4. We ran the questions through our RAG solution with the updated knowledge base content
5. We compared results before and after the content updates

<p>&nbsp;</p>

**Quick links:**
- [How we collected the sample questions](#how-we-collected-the-sample-questions-answers-corresponding-article)
- [Article quick reference](#article-quick-reference)
- [Notebook for extracting text from article HTML](../notebooks/10_html-text.ipynb)
- [HTML tables deep dive](table-processing.md)
- [Notebook with our simple RAG solution](../notebooks/11_answer-natural-questions.ipynb)
- [Analyis of results](results-analysis.md)

<p>&nbsp;</p>

