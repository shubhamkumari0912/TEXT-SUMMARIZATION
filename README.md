# TEXT-SUMMARIZATION
One method of natural language processing (NLP) that is used to reduce long documents or text data into more manageable summaries is text summarisation.
Summarization can be divided into two main types:
1. Extractive Summarization-Extractive summarization involves selecting key sentences or phrases directly from the original text to create a summary. This method doesn’t alter the structure or words; it simply identifies and extracts the most relevant portions
  
2. Abstractive Summarization-Abstractive summarization generates a summary by interpreting and rephrasing the content, similar to how a human would summarize text. This approach is more challenging but often provides a more natural and coherent summary.
Here we are creating a text summarization system for live news data requires setting up an efficient pipeline that can collect, process, and summarize incoming news articles or updates in real-time.

How it works:

	This code fetches live news articles from a specified news API, then summarizes each article using a transformer model which uses Hugging Face’s pipeline with the distilbart-cnn-12-6 model to create a summarizer for text summarization.

	The fetch_live_data function sends a request to the news API endpoint.If successful, it extracts the content from each article and filters out any articles without content.

	The summarize_texts function takes a list of article texts and generates a summary for each.

	It sets max_length and min_length dynamically based on each article’s length, ensuring the summary is concise yet informative.

	The code fetches and summarizes new articles every 10 minutes, then prints each article's summary.

	If no new articles are found, it waits for the next cycle.

	The code continuously retrieves and summarizes live news articles every 10 minutes. 

