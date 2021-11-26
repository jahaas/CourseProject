# CourseProject

My final project consisted of configuring a (rudimentary) question and answer "chatbot" using the Google Deepmind NarrativeQA Reading Comprehension project files (https://github.com/deepmind/narrativeqa) and native python libraries. Cornell University explained the challenge of the project this way, "Reading comprehension (RC)---in contrast to information retrieval---requires integrating information and reasoning about events, entities, and their relations across a full document ... These tasks are designed so that successfully answering their questions requires understanding the underlying narrative rather than relying on shallow pattern matching or salience. We show that although humans solve the tasks easily, standard RC models struggle on the tasks presented here." (https://arxiv.org/abs/1712.07040)

My approach included TF-IDF and cosine similarity. Although having an accuracy of 41% in predicting the correct answer to each question, this approach is clearly not sophisticated enough for a RC system. Additionally, the correctly predicted answers returned the entire sentence that included the answer, rather than curating the answer and returning only the portion of the sentence that answered the question most directly.



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

## Results
Out of the 1040 predicted answers, I manually QA’d 267 predicted answers with each respective annotated “right” answer as provided by Google. 95% of the predicted answers were generated from the correct Wikipedia article. 41% of the predicted answers were correct answers. 

Although having an accuracy of 41% in predicting the correct answer to each question, this approach is clearly not sophisticated enough for a RC system. Additionally, the correctly predicted answers returned the entire sentence that included the answer, rather than curating the answer and returning only the portion of the sentence that answered the question most directly.


