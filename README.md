# Web Scraping and Classification

The objective of this project is to:

* **web scrape** a corpus of news articles from a set of web pages,
* **pre-process** the corpus, and
* **evaluate the performance** of **automated classification** of these articles in a **supervised learning context**.

For this project I have used following third-party packages: 
* NumPy, 
* Pandas,
* Scikit-learn, 
* NLTK, 
* SciPy, 
* BeautifulSoup (bs4),
* Matplotlib,
* Seaborn,
* urllib.requests.

## Part 1. Data Collection
Collecting a **labelled news** corpus. Tasks completed:
1. Identifing the **URLs** and **category labels** for all news articles listed on the website:   http://mlg.ucd.ie/modules/COMP41680/archive/index.html 
2. Retrieving **all web pages** corresponding to these **article URLs**. From the web pages, extracting the **main body text** containing the content of each news article. Saving the **body** of each article as **plain text**.
3. Saving the **category labels** for all articles in a **separate file**. <br>

<i> Note: There are many ways to parse HTML pages in Python. I have used third-party <a href="https://www.crummy.com/software/BeautifulSoup/">Beautiful Soup</a> package that is useful when working with badly written HTML pages. BeautifulSoup can be used to find all the tags needed and retrieve the text between them.</i>

## Part 2. Text Classification
Analysing the corpus of documents from Part 1 in a *text classification* context. Tasks completed:
1. From the files created in Part 1, **loading** the **set of raw documents** into the **notebook**. Ensuring that **each document** has a **class label**, based on the **original category label**.
2. From the raw documents, creating a **document-term matrix**, using appropriate **text pre-processing** and **term weighting** steps.
3. Building two **multi-class classification models** using **two different classifiers**: **k-Nearest Neighbors Classifier** and **Support Vector Machines**.
4. **Comparing the predictions** of the **two classification models** using an **appropriate evaluation strategy.** 
<br>


<ul>
  <li><b><u>Document Term Matrix</u></b><br>
In the bag-of-words model (document-term matrix, each document is represented by a vector in an m-dimensional coordinate space, where m is number of unique terms across all documents. This set of terms is called the corpus vocabulary. 
Bag of words model (document-term matrix) does not preserve sequence in formation, so the order of words in a sentence is lost.<br> 
Solution: Adjacent tokens<br>
Term Bigrams - build terms from every pair of adjacent tokens (N-GRAMS - N adjacent tokens)<br>
<i> Note: For this <b>project</b> I have used <b>bigrams</b> and <b>threegrams</b>.</i></li> <br>
  <li><b><u>Text Preprocessing</u></b><br>
    A range of steps can be used to process <b>text input files</b> to <b>reduce the number of terms</b> used to <b>represent the text</b> and to <b>improve</b> the resulting <b>bag-of-words model</b>. For this <b>project</b> I have preformed following <b>text preprocessing techniques</b>:<br>
    <ul>
      <li><b>Minimum term length:</b> Excluding terms of length < 2. </li>
      <li><b>Case conversion:</b> Converting all terms to lowercase. </li>
      <li><b>Stop-word filtering:</b> Removing terms that appear on a pre-defined "blacklist" of terms that are highly frequent and do- not convey useful information.</li>
      <li><b>Low frequency filtering:</b> Removing terms that appear in very few documents. </li>
      <li><b>Lemmatization:</b> Reducing a term to its canonical form (more advanced from stemming that reduces words to their stems (or base forms)) </li>
      <li> <b>Term Weighting:</b> Improving the usefulness of the document-term matrix by giving more weight to the more "important" terms. For this <b>project</b> I have used the most common normalisation - term frequency–inverse document frequency (TF-IDF).</li>
    </ul>
  <li>using **two different classifiers**: **k-Nearest Neighbors Classifier** and **Support Vector Machines**.</li>
</ul>







There are 1408 web pages from which we need to extract the main body text containing the content of each news article, and 1408 category labels
From the plot we can see that labels do not have balanced distribution, hence we should apply the random under-sampling later on. Oversampling and undersampling in data analysis are techniques used to adjust the class distribution of a data set (i.e. the ratio between the different classes/categories represented).
