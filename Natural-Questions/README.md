## Sample questions and answers

From the [Natural Questions data set and benchmark](https://ai.google.com/research/NaturalQuestions) a sample of 189 questions, expected answes, and grounding article titles about "the Earth" were manually extracted:

[questions-and-answers.jsonl](questions-and-answers.jsonl)

Example of contents of `questions-and-answers.json`:

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

Example, line 1394, of file `v1.0/dev/nq-dev-01.jsonl` (notice example ID, question text, and article title are easily available):

<pre>{
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

Example, line 1394, of file `v1.0/dev/nq-dev-01.jsonl`:

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

### Article HTML

The HTML of the `document_html` field was extracted into a separate HTML file for each article: 

[Article HTML files](./html)

### Article text

The text of each article was extracted from the HTML using a script:

- [Article text files](./text)
- [Extract-text script](./extract-text.js)

