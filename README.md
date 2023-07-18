# Text Summariser
This project aims to build a text summarizer using NLTK libraries. The project involves data scraping from Wikipedia articles, preprocessing, tokenization and sentence scoring. The weighted frequency of each word is calculated and scores are assigned to each sentence. Finally, the project extracts the top 7 sentences with the highest scores and prints them on the console.

Simple text summeriser using only 'nltk' libraries(no machine learning models used)
In the context of text summarization, the algorithm is used to rank sentences in a document based on their importance.

following steps are carried out to achieve this:

* Fetching Articles from Wikipedia by data scraping
* Preprocessing 
* Tokenisation
* Find Weighted Frequency of Occurrence

Next we need to find the weighted frequency of occurrences of all the words. We can find the weighted frequency of each word by dividing its frequency by the frequency of the most occurring word. The following table contains the weighted frequencies for each word


To find the weighted frequency, we can simply divide the number of occurances of all the words by the frequency of the most occurring word

# Calculating Sentence Scores

We have now calculated the weighted frequencies for all the words. Now is the time to calculate the scores for each sentence by adding weighted frequencies of the words that occur in that particular sentence. We do not want very long sentences in the summary, therefore, we calculate the score for only sentences with less than 20 words 

# Getting the Summary

Now we have the sentence_scores dictionary that contains sentences with their corresponding score. To summarize the article, we can take top N sentences with the highest scores. The following script retrieves top 7 sentences and prints them on the screen.

we use the heapq library and call its nlargest function to retrieve the top 7 sentences with the highest scores.
