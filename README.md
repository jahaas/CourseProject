# CourseProject

My final project consisted of configuring a (rudimentary) question and answer "chatbot" using the Google Deepmind NarrativeQA Reading Comprehension project files (https://github.com/deepmind/narrativeqa) and native python libraries. 


## Group Name: Team Coco

Theme: Free Topics

Specific Topic: AllenNLP Chatbot (though shifted to using native python after not being able to install the allennlp library)

Captain/Project Leader (and sole team member): Joel Haas, joelah2@illinois.edu

**Proposal Task:** question-and-answer chatbot


## Initial AllenNLP Challenge

I was not able to successfully install the AllenNLP python library.  I spent 3 hours researching the AllenNLP capability.  I then tried to install the AllenNLP library so I could start learning the library.  However, after 2 hours troubleshooting and researching the installation challenges that others have also had trying to install the library, I decided I needed to move on.  So, I configured a question-and-answer “chatbot” using the Google Deepmind NarrativeQA Reading Comprehension project files and native python libraries rather than the AllenNLP python library.

## Files

Files provided by the Google Deepmind NarrativeQA Reading Comprehension project:
* qaps.csv: contains the questions and the annotated "right" answers to the questions; schema is document_id, set, question, answer1, answer2, question_tokenized, answer1_tokenized, answer2_tokenized.
* summaries.csv: contains the summary articles from Wikipedia that are to be searched for the answer to the question being asked; schema is document_id, set, summary, summary_tokenized (paragraphs of articles are separate rows in the CSV).

Files created as part of the project:
* summary_list.csv: Wrangled summaries.csv dataset so that one Wikipedia article was one row, rather than multiple rows; schema is document_id and entire wikipedia article (all sentences and paragraphs) 
* updatedSummaryList.csv: Reformatted the summaries in summary_list.csv so that each sentence of each Wikipedia article starts with the document_id (rather than just the first sentence of each Article); schema is document_id and one sentence from summary_list
* questions_list.csv: questions extracted and cleaned from qaps.csv; schema is document_id and question.
* answers_list.csv: annotated "right" answers extracted and cleaned from qaps.csv; schema is annotated "right" answer1 and answer2.
* AlgorithmicAnswers_to_Questions.csv: predicted answers to each question being asked
* AlgorithmicAnswers_to_Questions_QApredictedanswers.csv: manually compared the predicted chatbot answers to the annotated "right" answer1

Note: I cut down the records in the qaps.csv from 8029 questions to 1040 questions due to: 1) the time to predict answers to all 8029 questions would have taken 40+ hours; and 2) I would not be able to manually QA that many predicted answers. 



