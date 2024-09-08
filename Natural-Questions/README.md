## Sample questions and answers

From the [Natural Questions data set and benchmark](https://ai.google.com/research/NaturalQuestions) a sample of 189 questions, expected answes, and grounding article about "the Earth" were manually extracted:

[questions-and-answers.jsonl](questions-and-answers.jsonl)

Example contents of `questions-and-answers.json`:

<pre>
{
   "file_name" : "v1.0/dev/nq-dev-01.jsonl",
   "line_num" : 1394,
   "example_id" : "-1368633715963532113",
   "question_txt" : "where can carbon be found in the biosphere",
   "answers_arr" : [
      "in all land - living organisms , both alive and dead , as well as carbon stored in soils",
      ...
   ],
   "article_title" : "Carbon cycle"
}
</pre>

### `example_id`, `question_txt`, and `article_title`

Line 1394, of file `v1.0/dev/nq-dev-01.jsonl` (notice example ID, question text, and article title are easily available):

<pre>
{
   "annotations" : [ ... ],
   "document_html" : "<!DOCTYPE html>\\n<HTML class=\"client-js ve-not-available\" lang=\"en\" dir=\"ltr\"><HEAD>\\n\\n<TITLE>Carbon cycle - Wikipedia</TITLE>...",
   "document_title" : "Carbon cycle",
   "document_tokens" : [ ... ],
   "document_url" : "https://en.wikipedia.org//w/index.php?title=Carbon_cycle&amp;oldid=837879153",
   "example_id" : -1368633715963532113,
   "long_answer_candidates" : [ ... ]
   "question_text" : "where can carbon be found in the biosphere",
   "question_tokens" : [ ... ]
}</pre>

### `answers_arr`

The expected answer text was assembled by looking up the tokens in the `document_tokens` field listed in `short_answers` in the `annotations` list:

Line 1394, of file `v1.0/dev/nq-dev-01.jsonl`:

<pre>{
   "annotations" : [
      {
         "annotation_id" : 12715146547956222543,
         "long_answer" : { ... },
         "short_answers" : [
            {
               "end_byte" : 69407,
               "end_token" : 965,
               "start_byte" : 69289,
               "start_token" : 946
            }
         ],
         "yes_no_answer" : "NONE"
      },
      ...
   ],
   "document_html" : "<!DOCTYPE html>\\n<HTML class=\"client-js ve-not-available\" lang=\"en\" dir=\"ltr\"><HEAD>\\n\\n<TITLE>Carbon cycle - Wikipedia</TITLE>...",
   "document_title" : "Carbon cycle",
   "document_tokens" : [
      ...
      {"end_byte":69291,"html_token":false,"start_byte":69289,"token":"in"},
      {"end_byte":69295,"html_token":false,"start_byte":69292,"token":"all"},
      {"end_byte":69300,"html_token":false,"start_byte":69296,"token":"land"},
      {"end_byte":69301,"html_token":false,"start_byte":69300,"token":"-"},
      {"end_byte":69307,"html_token":false,"start_byte":69301,"token":"living"},
      {"end_byte":69317,"html_token":false,"start_byte":69308,"token":"organisms"},
      {"end_byte":69318,"html_token":false,"start_byte":69317,"token":","},
      {"end_byte":69323,"html_token":false,"start_byte":69319,"token":"both"},
      {"end_byte":69329,"html_token":false,"start_byte":69324,"token":"alive"},
      {"end_byte":69333,"html_token":false,"start_byte":69330,"token":"and"},
      {"end_byte":69338,"html_token":false,"start_byte":69334,"token":"dead"},
      {"end_byte":69339,"html_token":false,"start_byte":69338,"token":","},
      {"end_byte":69342,"html_token":false,"start_byte":69340,"token":"as"},
      {"end_byte":69347,"html_token":false,"start_byte":69343,"token":"well"},
      {"end_byte":69350,"html_token":false,"start_byte":69348,"token":"as"},
      {"end_byte":69357,"html_token":false,"start_byte":69351,"token":"carbon"},
      {"end_byte":69364,"html_token":false,"start_byte":69358,"token":"stored"},
      {"end_byte":69367,"html_token":false,"start_byte":69365,"token":"in"},
      {"end_byte":69407,"html_token":false,"start_byte":69402,"token":"soils"},
      ...
   ],
   "document_url" : "https://en.wikipedia.org//w/index.php?title=Carbon_cycle&amp;oldid=837879153",
   "example_id" : -1368633715963532113,
   "long_answer_candidates" : [ ... ]
   "question_text" : "where can carbon be found in the biosphere",
   "question_tokens" : [ ... ]
}</pre>

<p>&nbsp;</p>


### Article HTML

The HTML of the `document_html` field was extracted into a separate HTML file for each article: 

[Article HTML files](./html)

<p>&nbsp;</p>


### Article text

The text of each article was extracted from the HTML using [this notebook](../notebooks/10_html-text.ipynb)

[Article Text files](./txt_org)

<p>&nbsp;</p>


## Quick reference
The following table shows the articles that were extracted for this experiment, with links to:
- **Wikipedia link** : The URL of the exact version of the article on wikipedia, the `document_url` field from the NQ data set
- **HTML file** : The HTML in the `document_html` field from the NQ data set
- **Text file** : The text file generted by our team using [this notebook](../notebooks/10_html-text.ipynb)

<table>
<tr>
<th>Title</th>
<th>Reference</th>
<th>Wikipedia link</th>
<th>HTML file</th>
<th>Text file</th>
</tr>
<tr>
<td valign="top">Abundance of elements in Earth's crust</td>
<td valign="top">File: <tt>v1.0/train/nq-train-03.jsonl</tt><br/>Line: 3372</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Abundance_of_elements_in_Earth%27s_crust&oldid=801283417">Wikipedia link</a><br/><tt>oldid=801283417</tt></td>
<td valign="top"><a href="html/Abundance-of-elements-in-Earths-crust.html">HTML file</a></td><td valign="top"><a href="txt_org/Abundance-of-elements-in-Earths-crust.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Atmosphere of Earth</td>
<td valign="top">File: <tt>v1.0/train/nq-train-01.jsonl</tt><br/>Line: 3188</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Atmosphere_of_Earth&oldid=807367681">Wikipedia link</a><br/><tt>oldid=807367681</tt></td>
<td valign="top"><a href="html/Atmosphere-of-Earth.html">HTML file</a></td><td valign="top"><a href="txt_org/Atmosphere-of-Earth.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Axial precession</td>
<td valign="top">File: <tt>v1.0/dev/nq-dev-04.jsonl</tt><br/>Line: 135</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Axial_precession&oldid=821770845">Wikipedia link</a><br/><tt>oldid=821770845</tt></td>
<td valign="top"><a href="html/Axial-precession.html">HTML file</a></td><td valign="top"><a href="txt_org/Axial-precession.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Axial tilt</td>
<td valign="top">File: <tt>v1.0/train/nq-train-16.jsonl</tt><br/>Line: 816</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Axial_tilt&oldid=826622273">Wikipedia link</a><br/><tt>oldid=826622273</tt></td>
<td valign="top"><a href="html/Axial-tilt.html">HTML file</a></td><td valign="top"><a href="txt_org/Axial-tilt.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Carbon cycle</td>
<td valign="top">File: <tt>v1.0/dev/nq-dev-01.jsonl</tt><br/>Line: 1394</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Carbon_cycle&oldid=837879153">Wikipedia link</a><br/><tt>oldid=837879153</tt></td>
<td valign="top"><a href="html/Carbon-cycle.html">HTML file</a></td><td valign="top"><a href="txt_org/Carbon-cycle.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Carbon dioxide in Earth's atmosphere</td>
<td valign="top">File: <tt>v1.0/train/nq-train-14.jsonl</tt><br/>Line: 2690</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Carbon_dioxide_in_Earth%27s_atmosphere&oldid=856951315">Wikipedia link</a><br/><tt>oldid=856951315</tt></td>
<td valign="top"><a href="html/Carbon-dioxide-in-Earths-atmosphere.html">HTML file</a></td><td valign="top"><a href="txt_org/Carbon-dioxide-in-Earths-atmosphere.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Continent</td>
<td valign="top">File: <tt>v1.0/train/nq-train-02.jsonl</tt><br/>Line: 2384</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Continent&oldid=808552023">Wikipedia link</a><br/><tt>oldid=808552023</tt></td>
<td valign="top"><a href="html/Continent.html">HTML file</a></td><td valign="top"><a href="txt_org/Continent.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Crust (geology)</td>
<td valign="top">File: <tt>v1.0/train/nq-train-09.jsonl</tt><br/>Line: 2792</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Crust_(geology)&oldid=818260704">Wikipedia link</a><br/><tt>oldid=818260704</tt></td>
<td valign="top"><a href="html/Crust-geology.html">HTML file</a></td><td valign="top"><a href="txt_org/Crust-geology.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Earth</td>
<td valign="top">File: <tt>v1.0/train/nq-train-07.jsonl</tt><br/>Line: 1953</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Earth&oldid=801344840">Wikipedia link</a><br/><tt>oldid=801344840</tt></td>
<td valign="top"><a href="html/Earth.html">HTML file</a></td><td valign="top"><a href="txt_org/Earth.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Earth's energy budget</td>
<td valign="top">File: <tt>v1.0/train/nq-train-20.jsonl</tt><br/>Line: 1651</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Earth%27s_energy_budget&oldid=795644989">Wikipedia link</a><br/><tt>oldid=795644989</tt></td>
<td valign="top"><a href="html/Earths-energy-budget.html">HTML file</a></td><td valign="top"><a href="txt_org/Earths-energy-budget.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Earth's internal heat budget</td>
<td valign="top">File: <tt>v1.0/train/nq-train-08.jsonl</tt><br/>Line: 1498</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Earth%27s_internal_heat_budget&oldid=811248570">Wikipedia link</a><br/><tt>oldid=811248570</tt></td>
<td valign="top"><a href="html/Earths-internal-heat-budget.html">HTML file</a></td><td valign="top"><a href="txt_org/Earths-internal-heat-budget.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Earth's magnetic field</td>
<td valign="top">File: <tt>v1.0/train/nq-train-01.jsonl</tt><br/>Line: 2944</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Earth%27s_magnetic_field&oldid=814256351">Wikipedia link</a><br/><tt>oldid=814256351</tt></td>
<td valign="top"><a href="html/Earths-magnetic-field.html">HTML file</a></td><td valign="top"><a href="txt_org/Earths-magnetic-field.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Earth's orbit</td>
<td valign="top">File: <tt>v1.0/dev/nq-dev-04.jsonl</tt><br/>Line: 266</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Earth%27s_orbit&oldid=834440991">Wikipedia link</a><br/><tt>oldid=834440991</tt></td>
<td valign="top"><a href="html/Earths-orbit.html">HTML file</a></td><td valign="top"><a href="txt_org/Earths-orbit.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Earth's rotation</td>
<td valign="top">File: <tt>v1.0/dev/nq-dev-03.jsonl</tt><br/>Line: 1489</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Earth%27s_rotation&oldid=836804207">Wikipedia link</a><br/><tt>oldid=836804207</tt></td>
<td valign="top"><a href="html/Earths-rotation.html">HTML file</a></td><td valign="top"><a href="txt_org/Earths-rotation.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Inner core</td>
<td valign="top">File: <tt>v1.0/dev/nq-dev-02.jsonl</tt><br/>Line: 1073</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Inner_core&oldid=838408961">Wikipedia link</a><br/><tt>oldid=838408961</tt></td>
<td valign="top"><a href="html/Inner-core.html">HTML file</a></td><td valign="top"><a href="txt_org/Inner-core.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Mantle (geology)</td>
<td valign="top">File: <tt>v1.0/train/nq-train-13.jsonl</tt><br/>Line: 575</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Mantle_(geology)&oldid=814508368">Wikipedia link</a><br/><tt>oldid=814508368</tt></td>
<td valign="top"><a href="html/Mantle-geology.html">HTML file</a></td><td valign="top"><a href="txt_org/Mantle-geology.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Mantle convection</td>
<td valign="top">File: <tt>v1.0/train/nq-train-09.jsonl</tt><br/>Line: 2468</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Mantle_convection&oldid=827866500">Wikipedia link</a><br/><tt>oldid=827866500</tt></td>
<td valign="top"><a href="html/Mantle-convection.html">HTML file</a></td><td valign="top"><a href="txt_org/Mantle-convection.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Plate tectonics</td>
<td valign="top">File: <tt>v1.0/train/nq-train-10.jsonl</tt><br/>Line: 3044</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Plate_tectonics&oldid=800409264">Wikipedia link</a><br/><tt>oldid=800409264</tt></td>
<td valign="top"><a href="html/Plate-tectonics.html">HTML file</a></td><td valign="top"><a href="txt_org/Plate-tectonics.org.txt">Text file</a></td></tr>
<tr>
<td valign="top">Structure of the Earth</td>
<td valign="top">File: <tt>v1.0/train/nq-train-01.jsonl</tt><br/>Line: 5325</td>
<td valign="top"><a href="https://en.wikipedia.org//w/index.php?title=Structure_of_the_Earth&oldid=866111969">Wikipedia link</a><br/><tt>oldid=866111969</tt></td>
<td valign="top"><a href="html/Structure-of-the-Earth.html">HTML file</a></td><td valign="top"><a href="txt_org/Structure-of-the-Earth.org.txt">Text file</a></td></tr>
</table>

<p>&nbsp;</p>
