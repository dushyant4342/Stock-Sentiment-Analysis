# Natural Language Processing 
It is manipulation or understanding text or speech by any software or machine. An analogy is that humans interact, understand each other views, 
and respond with the appropriate answer.

# NLTK 
stands for Natural Language Toolkit. This toolkit is one of the most powerful NLP libraries which contains packages to make machines understand human language and reply to
it with an appropriate response. Tokenization, Stemming, Lemmatization, Punctuation, Character count, word count are some of these packages.

# Count vectorizer:
It is used to transform a given text into a vector on the basis of the frequency (count) of each word that occurs in the entire text.
https://www.geeksforgeeks.org/using-countvectorizer-to-extracting-features-from-text/

# TF-IDF in NLP 
It stands for Term Frequency – Inverse document frequency.During any text processing, cleaning the text (preprocessing) is vital. Further, the cleaned data needs to be 
converted into a numerical format where each word is represented by a matrix (word vectors). This is also known as word embedding Term Frequency (TF) = (Frequency of a term in the document)/(Total number of terms in documents)
Inverse Document Frequency(IDF) = log( (total number of documents)/(number of documents with term t))
TF.IDF = (TF).(IDF)
Bigrams: Bigram is 2 consecutive words in a sentence. E.g. “The boy is playing football”. The bigrams here are:

  The boy, 
  
  Boy is, 
  
  Is playing, 
  
  Playing football

Trigrams: Trigram is 3 consecutive words in a sentence. For the above example trigrams will be:

  The boy is, 
  
  Boy is playing, 
  
  Is playing football 
  
https://www.geeksforgeeks.org/tf-idf-for-bigrams-trigrams/

# Word Tokenize
With the help of nltk.tokenize.word_tokenize() method, we are able to extract the tokens from string of characters by using tokenize.word_tokenize() method. It actually returns 
the syllables from a single word. A single word can contain one or two syllables.
https://www.geeksforgeeks.org/python-nltk-nltk-tokenizer-word_tokenize/
      from nltk import word_tokenize 
      
      tk = SyllableTokenizer() 
      
      #Create a string input 
      
      gfg = "Antidisestablishmentarianism"  
      
      #Use tokenize method 
      
      geek = tk.tokenize(gfg)    
      
      print(geek)
      
      [‘An’, ‘ti’, ‘dis’, ‘es’, ‘ta’, ‘blish’, ‘men’, ‘ta’, ‘ria’, ‘nism’]

# Removing stop words

Stop Words: A stop word is a commonly used word (such as “the”, “a”, “an”, “in”) that a search engine has been programmed to ignore, both when indexing entries for searching 
and when retrieving them as the result of a search query.

import nltk

from nltk.corpus import stopwords

print(stopwords.words('english'))

{‘ourselves’, ‘hers’, ‘between’, ‘yourself’, ‘but’, ‘again’, ‘there’, ‘about’, ‘once’, ‘during’, ‘out’, ‘very’, ‘having’, ‘with’, ‘they’, ‘own’, ‘an’, ‘be’, ‘some’, ‘for’, ‘do’, ‘its’, ‘yours’, ‘such’, ‘into’, ‘of’, ‘most’, ‘itself’, ‘other’, ‘off’, ‘is’, ‘s’, ‘am’, ‘or’, ‘who’, ‘as’, ‘from’, ‘him’, ‘each’, ‘the’, ‘themselves’, ‘until’, ‘below’, ‘are’, ‘we’, ‘these’, ‘your’, ‘his’, ‘through’, ‘don’, ‘nor’, ‘me’, ‘were’, ‘her’, ‘more’, ‘himself’, ‘this’, ‘down’, ‘should’, ‘our’, ‘their’, ‘while’, ‘above’, ‘both’, ‘up’, ‘to’, ‘ours’, ‘had’, ‘she’, ‘all’, ‘no’, ‘when’, ‘at’, ‘any’, ‘before’, ‘them’, ‘same’, ‘and’, ‘been’, ‘have’, ‘in’, ‘will’, ‘on’, ‘does’, ‘yourselves’, ‘then’, ‘that’, ‘because’, ‘what’, ‘over’, ‘why’, ‘so’, ‘can’, ‘did’, ‘not’, ‘now’, ‘under’, ‘he’, ‘you’, ‘herself’, ‘has’, ‘just’, ‘where’, ‘too’, ‘only’, ‘myself’, ‘which’, ‘those’, ‘i’, ‘after’, ‘few’, ‘whom’, ‘t’, ‘being’, ‘if’, ‘theirs’, ‘my’, ‘against’, ‘a’, ‘by’, ‘doing’, ‘it’, ‘how’, ‘further’, ‘was’, ‘here’, ‘than’}



from nltk.corpus import stopwords 

from nltk.tokenize import word_tokenize 
  
example_sent = "This is a sample sentence, showing off the stop words filtration."
  
stop_words = set(stopwords.words('english')) 
  
word_tokens = word_tokenize(example_sent) 
  
filtered_sentence = [w for w in word_tokens if not w in stop_words] 
  
filtered_sentence = [] 
  
for w in word_tokens: 

    if w not in stop_words: 
    
        filtered_sentence.append(w) 
  
print(word_tokens) 

print(filtered_sentence) 

['This', 'is', 'a', 'sample', 'sentence', ',', 'showing', 'off', 'the', 'stop', 'words', 'filtration', '.']

['This', 'sample', 'sentence', ',', 'showing', 'stop','words', 'filtration', '.']
