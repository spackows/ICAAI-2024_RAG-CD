# RAG CD perspective
Samples related to Content Design for retrieval-augmented generation (RAG)

## Sample notebooks
<table>
<tr>
<th valign="top">Notebook</th>
<th valign="top">Description</th>
</tr>
<!-- 1. Filter input -->
<tr>
<td valign="top">
<p><b>1.&nbsp;Filter&nbsp;input</b>&nbsp;(&nbsp;<a href="notebooks/01_filter.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/01_filter.png" width="150px" /></p>
</td>
<td valign="top">
<p>Filter out the following malicious input:
<ul>
<li>Javascript injection</li>
<li>Prompt injection</li>
</ul>
</p>
</td>
</tr>
<!-- 2. Classify input -->
<tr>
<td valign="top">
<p><b>2.&nbsp;Classify&nbsp;input</b>&nbsp;(&nbsp;<a href="notebooks/02_classify-input.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/02_classify-input.png" width="150px" /></p>
</td>
<td valign="top">
<p>Classify user input into one of these categories:
<ul>
<li>Keyword search</li>
<li>Question (including question type)</li>
<li>Instruction</li>
</ul>
</p>
</td>
</tr>
<!-- 3. Identify HAP -->
<tr>
<td valign="top">
<p><b>3.&nbsp;Identify&nbsp;HAP</b>&nbsp;(&nbsp;<a href="notebooks/03_hap.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/03_hap.png" width="150px" /></p>
</td>
<td valign="top">
<p>Identify hate, abuse, and profanity</p>
</td>
</tr>
<!-- 4. Identify FAQ -->
<tr>
<td valign="top">
<p><b>4.&nbsp;Identify&nbsp;FAQ</b>&nbsp;(&nbsp;<a href="notebooks/04_faq.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/04_faq.png" width="150px" /></p>
</td>
<td valign="top">
<p>Match given question with frequently asked question</p>
</td>
</tr>
<!-- 5. Boost search -->
<tr>
<td valign="top">
<p><b>5.&nbsp;Boost&nbsp;search</b>&nbsp;(&nbsp;<a href="notebooks/05_search.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/05_search.png" width="150px" /></p>
</td>
<td valign="top">
<p>Improve search success using several techniques:
<ul>
<li>Add synonyms</li>
<li>Rewrite query</li>
</ul>
</p>
</td>
</tr>
<!-- 6. Prompt by question type -->
<tr>
<td valign="top">
<p><b>6.&nbsp;Prompt&nbsp;by&nbsp;question&nbsp;type</b>&nbsp;(&nbsp;<a href="notebooks/06_prompt.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/06_prompt.png" width="150px" /></p>
</td>
<td valign="top">
<p>Given relevant articles from a knowledge base, prompt a large language model to answer a question</p>
</td>
</tr>
<!-- 7. Select best answer -->
<tr>
<td valign="top">
<p><b>7.&nbsp;Select&nbsp;best&nbsp;answer</b>&nbsp;(&nbsp;<a href="notebooks/07_best-answer.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/07_best-answer.png" width="150px" /></p>
</td>
<td valign="top">
<p>Select the best of several generated answers</p>
</td>
</tr>
<!-- 08. Test topics -->
<tr>
<td valign="top">
<p><b>8.&nbsp;Test&nbsp;topics</b>&nbsp;(&nbsp;<a href="notebooks/08_testing-topics.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/08_testing-topics.png" width="150px" /></p>
</td>
<td valign="top">
<p>Test how well a topic can answer given user questions</p>
</td>
</tr>
<!-- 09. Answering Natural Questions benchmark -->
<tr>
<td valign="top">
<p><b>9.&nbsp;Answering&nbsp;Natural&nbsp;Questions</b>&nbsp;(&nbsp;<a href="notebooks/09_nq.ipynb">Link</a>&nbsp;)</p>
<p><img src="images/09_nq.png" width="150px" /></p>
</td>
<td valign="top">
<p>Answer a subset of questions from the <a href="https://research.google/pubs/natural-questions-a-benchmark-for-question-answering-research/">Natural Questions benchmark</a></p>
</td>
</tr>
</table>
