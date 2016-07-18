Coursera Swiftkey Word Prediction Capstone Project
========================================================
author: Shaaz Siddiqi
date: July 18, 2016

Introduction
========================================================

<small>The Coursera Data Science Specialization Capstone project from Johns Hopkins University (JHU) allows students to create a usable public data product that can show their skills to potential 
employers. For this iteration of the class, JHU partnered with SwiftKey 
(http://swiftkey.com/en/) to apply data science in the area of **natural language processing**.

The objective of this project was to build a working predictive text model. The data used in the 
model came from a **corpus** called HC Corpora (www.corpora.heliohost.org). A corpus is body of text, 
usually containing a large number of sentences. [1]

<small>[1] http://desilinguist.org/pdf/crossroads.pdf</small></small>

Algorithm Development
========================================================

<small>The algorithm developed to predict the next word in a user-entered text string was based on a 
classic **N-gram** model. [2] Using a subset of cleaned data from blogs, twitter, and news 
Internet files, **Maximum Likelihood Estimation** (MLE) of unigrams, bigrams, and trigrams were computed.

To improve accuracy, **Jelinek-Mercer smoothing** was used in the algorithm, combining 
trigram, bigram, and unigram probabilities. [3] Where interpolation failed, 
**part-of-speech tagging** (POST) was employed to provide default predictions by part of 
speech. [4] Suggested word completion was based on the unigrams. A profanity filter was also utilized 
on all output using Google's bad words list. [5]

<small>[2] http://en.wikipedia.org/wiki/N-gram</small>
<small>[3] http://www.ee.columbia.edu/~stanchen/papers/h015l.final.pdf</small>
<small>[4] http://en.wikipedia.org/wiki/Part-of-speech_tagging</small>
<small>[5] https://badwordslist.googlecode.com/files/badwords.txt</small></small>


The Shiny Application
========================================================

<medium>Using the algorithm, a Shiny <a href="http://desilinguist.org/pdf/crossroads.pdf"> Natural Language Processing</a>  application was developed that accepts a phrase as input, suggests word completion from the unigrams, and predicts the most likely next word based on the linear interpolation of trigrams, bigrams, and unigrams. The web-based application can be found 
<a href="https://sid101.shinyapps.io/Text_Predictor_Application/"> here</a>. The source files for this application, the data creation, and this presentation can be found 
<a href="https://github.com/sid111/Coursera-Swiftkey-Capstone-Project"> here</a>. 
</medium>


Using the Application
========================================================

<medium>Use of the application is straightforward and can be easily adapted to many educational and 
commercial uses. As depicted below, the user begins just by typing some text without punctuation in 
the supplied input box. As the user types, the algorithm analyzes the words and comes up with a suggested words list.The accuracy of the prediction depends on the continuity of the text entered. Flowing sentences are most accurate in this regard. For example, The president has said ... will give that/previously as two possible options. </medium>



