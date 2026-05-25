<H3>ENTER YOUR NAME: JAYADEV PALLINTI</H3>
<H3>ENTER YOUR REGISTER NO: 212223240058</H3>
<H3>EX. NO.6</H3>
<H3>DATE:24-05-2026</H3>
<H1 ALIGN =CENTER>Implementation of Semantic ANalysis</H1>
<H3>Aim: to perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques. </H3> 
 <BR>
<h3>Algorithm:</h3>
Step 1: Import the nltk library.<br>
Step 2: Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.<br>
Step 3:Accept user input for the text.<br>
Step 4:Tokenize the input text into words using the word_tokenize function.<br>
Step 5:Iterate through each word in the tokenized text.<br>
•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.<br>
•	Print each word along with its corresponding part-of-speech tag.<br>
•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).<br>
•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.<br>
•	Print the unique sets of synonyms and antonyms.
<H3>Program:</H3>

```py
!pip install nltk

import nltk
#import wordnet
nltk.download( 'punkt_tab' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger_eng' )

sentence=input ()

words = sentence.split()

# POS tagging
pos_tags = nltk.pos_tag(words)

# Print the parts of speech
for word, tag in pos_tags:
    print(word, tag)

from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print("POS Tags:", pos_tags)
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )

```
<H3>Output</H3>

<img width="1748" height="80" alt="image" src="https://github.com/user-attachments/assets/cc9f6ef3-4e98-45a6-b608-02c1ce0e7a03" />

<H3>Result:</H3>
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
