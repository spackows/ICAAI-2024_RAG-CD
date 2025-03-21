# Analysis of results

**Files**
- [Notebook for extracting text from article HTML](../notebooks/10_html-text.ipynb)
- [Notebook with our simple RAG solution](../notebooks/11_answer-natural-questions.ipynb)
- [Results spreadsheet (Excel)](rewriting-experiment-results.xlsx)

**Quick links**
- [Initial results](#initial-results)
- [Content changes](#content-changes)
- [Final results](#final-results)
  
<p>&nbsp;</p>

## Initial results
Challenges with the sample questions:
- Of the 189 questions, 1 question was marked invalid because it's a crossword clue, not a question: "part of the earth's structure 6 letters"
- For 10 of the 189 questions, the expected answers were incorrect
- For 12 of the 189 questions, there were multiple right answers not included in the expected answer

Due to these challenges, we chose to evaluate the generated answers manually.  We evaluated for correctness, not how well the run-time answers match the expected answers.

With the original article text, our simple RAG notebook got 164 questions correct, out of 188.  (That's 24 questions wrong.)

<p>&nbsp;</p>


## Content changes

Here is a summary of updates made to the articles to improve results of our simple RAG notebook.

<table>
<tr>
<th>Article</th>
<th>Changes summary</th>
<th>Differences</th>
</tr>
<tr>
<td valign="top">Carbon&nbsp;dioxide&nbsp;in&nbsp;Earth's&nbsp;atmosphere<br/><a href="https://en.wikipedia.org//w/index.php?title=Carbon_dioxide_in_Earth%27s_atmosphere&oldid=856951315">Wikipedia link</a></td>
<td valign="top"><ul><li>Add "due in large part to the carbon dioxide we humans are putting there"</li></ul></td>
<td valign="top"><a href="images/diffs_Carbon-dioxide-in-Earths-atmosphere.png">diffs</a></td>
</tr>
<tr>
<td valign="top">Continent<br/><a href="https://en.wikipedia.org//w/index.php?title=Continent&oldid=808552023">Wikipedia link</a></td>
<td valign="top"><ul><li>Add hint about second smallest continent</li></ul></td>
<td valign="top"><a href="images/diffs_Continent.png">diffs</a></td>
</tr>
<tr>
<td valign="top">Crust (geology)<br/><a href="https://en.wikipedia.org//w/index.php?title=Crust_(geology)&oldid=818260704">Wikipedia link</a></td>
<td valign="top"><ul><li>Add "of Earth's crust" to some headings</li>
<li>Add "Teperature of Easrth's crust" heading</li>
<li>Add "what is found" terminology</li>
<li>Simplify the temperature information</li>
<li>Replace tables with lists</li></ul></td>
<td valign="top"><a href="images/diffs_Crust-geology.png">diffs</a></td>
</tr>
<tr>
<td valign="top">Earth<br/><a href="https://en.wikipedia.org//w/index.php?title=Earth&oldid=801344840">Wikipedia link</a></td>
<td valign="top"><ul><li>Add equatorial circumference</li>
<li>Simplify shape information</li>
<li>Add height of atmosphere</li></ul></td>
<td valign="top"><a href="images/diffs_Earth.png">diffs</a></td>
</tr>
<tr>
<td valign="top">Earth's orbit<br/><a href="https://en.wikipedia.org//w/index.php?title=Earth%27s_orbit&oldid=834440991">Wikipedia link</a></td>
<td valign="top"><ul><li>Simplify the introduction</li></ul></td>
<td valign="top"><a href="images/diffs_Earths-orbit.png">diffs</a></td>
</tr>
<tr>
<td valign="top">Earth's rotation<br/><a href="https://en.wikipedia.org//w/index.php?title=Earth%27s_rotation&oldid=836804207">Wikipedia link</a></td>
<td valign="top"><ul><li>Be more explicit about rotation of Earth - around its access and around the sun</li></ul></td>
<td valign="top"><a href="images/diffs_Earths-rotation.png">diffs</a></td>
</tr>
<tr>
<td valign="top">Inner core<br/><a href="https://en.wikipedia.org//w/index.php?title=Inner_core&oldid=838408961">Wikipedia link</a></td>
<td valign="top"><ul><li>Add "thickness" terminology</li>
<li>Boost search by adding mention that it makes up "a small amount of Earth's mass"</li></ul></td>
<td valign="top"><a href="images/diffs_Inner-core.png">diffs</a></td>
</tr>
<tr>
<td valign="top">Structure of the Earth<br/><a href="https://en.wikipedia.org//w/index.php?title=Structure_of_the_Earth&oldid=866111969">Wikipedia link</a></td>
<td valign="top"><ul><li>Emphasize the core has "two layers"</li>
<li>Boost search by changing the wording around the discovery of the inner core</li></ul></td>
<td valign="top"><a href="images/diffs_Structure-of-the-Earth.png">diffs</a></td>
</tr>
</table>

<p>&nbsp;</p>


## Final results
After updating the articles, our simple RAG notebook was able to answer all 188  valid questions correctly.

<table>
<tr>
<th>Question</th>
<th>Expected answer</th>
<th>Answer (before)<br/>[ Similarity score ]</th>
<th>Answer (after)<br/>[ Similarity score ]</th>
</tr>
<tr>
<td valign="top">most abundant non metal in the earth's crust</td>
<td valign="top">oxygen</td>
<td valign="top">I don't know<br/>[ 22 ]</td>
<td valign="top">O: 46.6% - Si: 27.7%<br/>[ 30 ]</td>
</tr>
<tr>
<td valign="top">how much carbon dioxide do we put in the atmosphere</td>
<td valign="top">approximately 2 ppm / year and accelerating</td>
<td valign="top">3200 gigatons<br/>[ 30 ]</td>
<td valign="top">The global mean CO2 concentration is currently rising at a rate of approximately 2 ppm/year and accelerating, due in large part to the carbon dioxide we humans are putting there.<br/>[ 39 ]</td>
</tr>
<tr>
<td valign="top">the second most abundant metal available on this earth crust is</td>
<td valign="top">silicon<p>*The correct answer is: iron (Fe)</p></td>
<td valign="top">Al<br/>[ 28 ]</td>
<td valign="top">Fe<br/>[ 39 ]</td>
</tr>
<tr>
<td valign="top">what is the diameter of the earth's orbit around the sun</td>
<td valign="top">The average distance between the Earth and the Sun is 149.60 million km ( 92.96 million mi )<p>*The correct answer is double this</p></td>
<td valign="top">150 million km (93 million mi)<br/>[ 59 ]</td>
<td valign="top">292 million km<br/>[ 49 ]</td>
</tr>
<tr>
<td valign="top">what is the average temperature of the crust</td>
<td valign="top">200 C ( 392 F ) to 400 C ( 752 F )</td>
<td valign="top">I don't know<br/>[ 9 ]</td>
<td valign="top">200 C (392 F) to 400 C (752 F)<br/>[ 56 ]</td>
</tr>
<tr>
<td valign="top">which is most abundant metal in earth crust</td>
<td valign="top">aluminium</td>
<td valign="top">iron<br/>[ 44 ]</td>
<td valign="top">Al<br/>[ 65 ]</td>
</tr>
<tr>
<td valign="top">the shape of the earth's path around the sun</td>
<td valign="top">elliptical</td>
<td valign="top">Earth's orbit<br/>[ 30 ]</td>
<td valign="top">an ellipse<br/>[ 69 ]</td>
</tr>
<tr>
<td valign="top">the shape of earth's orbit around the sun is</td>
<td valign="top">elliptical</td>
<td valign="top">Earth's orbit has an eccentricity of 0.0167.<br/>[ 40 ]</td>
<td valign="top">an ellipse<br/>[ 69 ]</td>
</tr>
<tr>
<td valign="top">what is the temperature at the center of earth</td>
<td valign="top">5,700 K ( 5,430 C ) or 9806 F</td>
<td valign="top">6,000 C (10,830 F)<br/>[ 50 ]</td>
<td valign="top">5,700 K (5,430 C)<br/>[ 70 ]</td>
</tr>
<tr>
<td valign="top">how far atmosphere extends from the surface of earth</td>
<td valign="top">within about 11 km ( 6.8 mi ; 36,000 ft ) of the surface</td>
<td valign="top">Thermosphere The thermosphere is the second-highest layer of Earth's atmosphere. It extends from the mesopause (which separates it from the mesosphere) at an altitude of about 80 km (50 mi; 260,000 ft) up to the thermopause at an altitude range of 500â€“1000 km (310â€“620 mi; 1,600,000â€“3,300,000 ft).<br/>[ 43 ]</td>
<td valign="top">11 km (6.8 mi; 36,000 ft)<br/>[ 81 ]</td>
</tr>
<tr>
<td valign="top">distance earth travels around the sun in miles</td>
<td valign="top">584 million mi</td>
<td valign="top">92.96 million<br/>[ 62 ]</td>
<td valign="top">584 million<br/>[ 82 ]</td>
</tr>
<tr>
<td valign="top">whats the composition of the earth's crust</td>
<td valign="top">an average composition similar to that of andesite</td>
<td valign="top">two distinct types: continental crust and oceanic crust<br/>[ 41 ]</td>
<td valign="top">The Earth's continental crust has an average composition similar to that of andesite.<br/>[ 84 ]</td>
</tr>
<tr>
<td valign="top">what is the thickness of earth's inner core</td>
<td valign="top">a radius of about 1,220 kilometres ( 760 miles )</td>
<td valign="top">250 to 400 km<br/>[ 74 ]</td>
<td valign="top">1,220 kilometres (760 miles)<br/>[ 92 ]</td>
</tr>
<tr>
<td valign="top">what is the distance the earth travels around the sun</td>
<td valign="top">940 million km ( 584 million mi )</td>
<td valign="top">149.60 million km (92.96 million mi)<br/>[ 93 ]</td>
<td valign="top">940 million km<br/>[ 92 ]</td>
</tr>
<tr>
<td valign="top">what is the shape of earth's orbit around the sun</td>
<td valign="top">ellipse</td>
<td valign="top">Earth's orbit has an eccentricity of 0.0167.<br/>[ 35 ]</td>
<td valign="top">an ellipse<br/>[ 97 ]</td>
</tr>
<tr>
<td valign="top">what is the true shape of earths orbit</td>
<td valign="top">ellipse</td>
<td valign="top">Earth's orbit has an eccentricity of 0.0167.<br/>[ 35 ]</td>
<td valign="top">an ellipse<br/>[ 97 ]</td>
</tr>
<tr>
<td valign="top">what is the shape of the earth's orbit around the sun</td>
<td valign="top">ellipse</td>
<td valign="top">Earth's orbit has an eccentricity of 0.0167.<br/>[ 35 ]</td>
<td valign="top">an ellipse<br/>[ 97 ]</td>
</tr>
<tr>
<td valign="top">what is the size of earth in km</td>
<td valign="top">40 075.017 km</td>
<td valign="top">5,150â€“6,360<br/>[ 25 ]</td>
<td valign="top">40,075.017 km<br/>[ 99 ]</td>
</tr>
<tr>
<td valign="top">distance of earth orbit around the sun in miles</td>
<td valign="top">584 million</td>
<td valign="top">92.96 million<br/>[ 67 ]</td>
<td valign="top">584 million<br/>[ 100 ]</td>
</tr>
<tr>
<td valign="top">when was the structure of the earth discovered</td>
<td valign="top">1936</td>
<td valign="top">I don't know<br/>[ 13 ]</td>
<td valign="top">1936<br/>[ 100 ]</td>
</tr>
<tr>
<td valign="top">earth's direction of rotation around the sun</td>
<td valign="top">counter clockwise</td>
<td valign="top">eastward<br/>[ 47 ]</td>
<td valign="top">counter clockwise<br/>[ 100 ]</td>
</tr>
<tr>
<td valign="top">smallest continent of world in terms of area other than australia is</td>
<td valign="top">Europe</td>
<td valign="top">Antarctica<br/>[ 48 ]</td>
<td valign="top">Europe<br/>[ 100 ]</td>
</tr>
<tr>
<td valign="top">how many layers in the earth's core</td>
<td valign="top">two</td>
<td valign="top">I don't know<br/>[ 25 ]</td>
<td valign="top">two<br/>[ 100 ]</td>
</tr>
<tr>
<td valign="top">who discovered that the earth rotates on an axis</td>
<td valign="top">Aryabhata</td>
<td valign="top">Among the ancient Greeks, several of the Pythagorean school believed in the rotation of the earth rather than the apparent diurnal rotation of the heavens. Perhaps the first was Philolaus (470â€“385 BCE), though his system was complicated, including a counter-earth rotating daily about a central fire.<br/>[ 9 ]</td>
<td valign="top">Aryabhata<br/>[ 100 ]</td>
</tr>
</table>
