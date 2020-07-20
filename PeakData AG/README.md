# Data science hiring

[This is an intro data science task for candidates. Source](https://gitlab.com/PeakData/hiring_assignments/datascience_hiring/datasciene_hiring/-/tree/master)

## Instructions

### Task

Your task is to create an algorithm, that takes html page as input and infers if the page contains the information about `cancer tumorbaord` or not. 
What is a tumor board? Tumor Board is a consilium of doctors (usually from diferent disciplines) discussing cancer cases in their deprtments. If you want to know more please read this [article](https://www.cancer.net/blog/2017-07/what-tumor-board-expert-qa)


We expect from you `submission.csv` file for test data with columns [`doc_id` and `prediction`] and jupyter notebook with code and next documentation:
* How did you decide to handle this amount of data
* How did you decide to do feature engineering
* How did you decide which models to try (if you decide to train any models)
* How did you perform validation of your model
* What metrics did you measure
* How do you expect your model to perform on test data (in terms of your metrics)
* How fast will your algorithm performs and how could you improve its performance if you would have more time
* How do you think you would be able to improve your algorithm if you would have more data
* What potential issues do you see with your algorithm
* 

`Note`: if you would like to go an extra mile in this task try to identify  tumor board types `interdisciplinary`, `breast` and any third type of tumor board up to you. 
For these tumor boards please try to identify their schedule: Day (e.g. Friday), frequency (e.g. weekly, bi-weekly, monthly) and time when they start.

### Data

You have [train.csv](https://gitlab.com/PeakData/hiring_assignments/datascience_hiring/datasciene_hiring/-/blob/master/train.csv) and [test.csv](https://gitlab.com/PeakData/hiring_assignments/datascience_hiring/datasciene_hiring/-/blob/master/test.csv) files and folder with corresponding [.html](https://gitlab.com/PeakData/hiring_assignments/datascience_hiring/datasciene_hiring/-/tree/master/htmls) files.

Files:
* `train.csv` contains next columns: `url`, `doc_id` and `label`
* `test.csv` contains next columns: `url` and `doc_id`
* `htmls` contains files with names `{doc_id}.html`
* [keyword2tumor_type.csv](https://gitlab.com/PeakData/hiring_assignments/datascience_hiring/datasciene_hiring/-/blob/master/keyword2tumor_type.csv) contains useful keywords for types of tumorboards

Description of tumorboard labels:
* 1 (no evidence): tumorboards are not mentioned on the page
* 2 (medium confidence): tumorboards are mentioned, but the page is not completely dedicated to tumorboard description
* 3 (high confidence): page is completely dedicated to description of tumorboardd types and dates

You are asked to prepare a model using htmls, referred in `train.csv` and make predictions for htmls from `test.csv`

### Tips

* to extract clean text from the page you can use BeautifulSoup module like this
```python
from bs import BeautifulSoup

content = read_html()
soup = BeautifulSoup(content)
clean_text = soup.get_text(' ')
```

* If you decide that you don't need, for example tags `<p>` in your document, you can do this:

```python
from bs import BeautifulSoup

content = read_html()
soup = BeautifulSoup(content)
for tag in soup.find_all('p'):
    tag.decompose()

```
