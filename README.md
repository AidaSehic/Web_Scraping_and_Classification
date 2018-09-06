# Web Scraping and Classification

The objective of this project is to:

* **web scrape** a corpus of news articles from a set of web pages,
* **pre-process** the corpus, and
* **evaluate the performance** of **automated classification** of these articles in a **supervised learning context**.


## Part 1. Data Collection
Collecting a **labelled news** corpus. Tasks completed:
1. Identifing the **URLs** and **category labels** for all news articles listed on the website:   http://mlg.ucd.ie/modules/COMP41680/archive/index.html 
2. Retrieving **all web pages** corresponding to these **article URLs**. From the web pages, extracting the **main body text** containing the content of each news article. Saving the **body** of each article as **plain text**.
3. Saving the **category labels** for all articles in a **separate file**.
*Note: There are many ways to parse HTML pages in Python. I have used third-party <a href="https://www.crummy.com/software/BeautifulSoup/">Beautiful Soup</a>Beautiful Soup package that is useful when working with badly written HTML pages. BeautifulSoup can be used to find all the tags needed and retrieve the text between them.

## Part 2. Text Classification
Analysing the corpus of documents from Part 1 in a text classification context. Tasks to be completed:
1. From the files created in Part 1, load the set of raw documents into your notebook. Ensure that each document has a class label, based on the original category label that you identified.
2. From the raw documents, create a document-term matrix, using appropriate text pre-processing and term weighting steps.
3. Build two multi-class classification models using two different classifiers of your choice.
4. Compare the predictions of the two classification models using an appropriate evaluation strategy. Report and discuss the evaluation results in your notebook.
Guidelines:
- For the assignment, only these third-party packages can be used: NumPy, Pandas,
Scikit-learn, NLTK, SciPy, Requests, BeautifulSoup, Matplotlib, Seaborn.
- Submit your assignment via the COMP41680 Moodle page. Your submission should clearly state your full name and student ID number. Include your full dataset with your submission. Your submission should be in the form of a single ZIP file containing the IPython notebook and the data.
