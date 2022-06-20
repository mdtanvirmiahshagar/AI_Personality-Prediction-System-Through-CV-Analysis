# WeEmploy

The project aims to develop a prototype of a platform that eradicates the traditional way of employment which comes with the need to manually go through numerous applications and CVs to find out what suits the particular requirement of the job being offered. WeEmploy seeks a more efficient way to short-list submitted candidate CVs from a large number of applicant providing a consistent and fair CV ranking policy, which can be legally justifed. This system will help the HR department to easily short-list the candidate based on the CV ranking policy.

[![star this repo](https://githubbadges.com/star.svg?user=philkam&repo=AI_Personality-Prediction-System-Through-CV-Analysis&style=default&color=fff&background=4c3)](https://github.com/philkam/AI_Personality-Prediction-System-Through-CV-Analysis)
[![fork this repo](https://githubbadges.com/fork.svg?user=philkam&repo=AI_Personality-Prediction-System-Through-CV-Analysis&style=default&color=fff&background=4c3)](https://github.com/philkam/AI_Personality-Prediction-System-Through-CV-Analysis/fork)

## Table of Contents
* [Prerequisites & Development Libraries](#prerequisites-&-development-libraries)
* [Installation](#installation)
* [Instructions](#instructions)
* [Background](#background)
* [Components of the Application](#components-of-the-application)
* [Aptitude Assessment](#aptitude-assessment)
* [Personality Test](#personality-test)
* [CV Analysis](#cv-analysis)
* [Disclaimer](#disclaimer)



## Prerequisites & Development Libraries


To install WeEmploy you'll need pip and Git. It also uses a some Python packages (NumPy, SciPy and Matplotlib) but these should be taken care of by the installation process.

| Software | Version |
| ------ | ------ |
| Python 3 | 3.9.6 |
| Pandas | 0.25.1 |
| Snscrape | 0.4.3 |
| Flask | 2.1.2 |
| Google Chrome | 102.0.5005.115 |



## Installation

You can install WeEmploy by cloning the repository:

```sh
git clone https://github.com/philkam/AI_Personality-Prediction-System-Through-CV-Analysis.git
```

## Instructions

* Clone the [repository](#installation)

* Set up a virtual environment. See [here](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments) for more details. Don't forget to activate the virtual environment.

* Install all required libraries through requirements.txt

```sh
pip install requirements.txt
```

* Run your local server ( WAMP, XAMPP etc)

* Now run the Flask app app.py.

```sh
python app.py
```

* In your browser open http://localhost:5000 (or :{port-number} as specified by the Flask's development server)


## Background 

There are various tests that help to determine personality types such as the Big Five, Rorschach test, and MBTI test. In this project, prediction of personality is done by considering the MBTI test.

The MBTI personality classification system grew out of Jungian psychoanalytic psychology as a systematization of archetypal personality types used in clinical practice. The system is divided along four binary orthogonal personality dimensions, altogether comprising a total of 16 distinct person.

### The dimensions are as follows

* Extraversion (E) vs Introversion (I): a measure of how much an individual prefers their outer or inner world.

* Sensing (S) vs Intuition (N): a measure of how much an individual processes information through the five senses versus impressions through patterns.

* Thinking (T) vs Feeling (F): a measure of preference for objective principles and facts versus weighing the emotional perspectives of others.

* Judging (J) vs Perceiving (P): a measure of how much an individual prefers a planned and ordered life versus a flexible and spontaneous life

## Components of the Application
* Login and Registration
* Aptitude Assessment
* Personality test
* CV analysis


## Aptitude Assessment
The aptitude assessment helps understand the underlying patterns of candidates interest and predict the stream that the candidate is interested in.
Understanding a candidates inherent aptitude is very crucial for an organisation. Candidates can test their aptitude after which a report is generated which can assess a candidate's interest. Based on this, the Human Resource Manager can place a candidate in the right team and point out the right candidate for a particular job.

#### Assessment
This section of the application allows the registered candidates to attend the aptitude assessment. The candidate registers through a portal, fills in the compulsory profile information and logs on to the application. The student views the assessment report.  The application allows the human resource personnels to prepare the set of questions. Assigning of questions to the candidates is done automatically, though the question paper is prepared by a human resource personnel. It also allows the personnels to manage students and also to edit their own profile. The personnel is registered by the Human Resource Manager.

#### Question Structure
All the questions are MCQ. four types of questions are supported by this application.

* Normal MCQ questions
* Question with image and option
* Question and option with images.
* Question and option with images.


Questions can be from four main sections namely Science, Commerce, Humanities, and Aptitude. To prepare the question paper the human resource personnel chooses about fifteen questions from each section. Each  question paper contains sixty questions. The questions are given a weightage according to  the category that particular question falls. The weightage is made useful for the evaluation of candidate assessment.It is mandatory for the students to attempt all the sixty question.


#### Candidate View Process Flow
* Registration
* Login
* Answers questions
* Vews report 

#### Human Resource Team
* Only the Human Resource Manager can add a personnel to the Staffing team.
* The Human Resource personnels determines the questions a candidate should take.
* The Human Resource personnels sets the weight each question should carry

#### The Database
* Student profile
* Answers given by students
* Instructor details
* Question details
* Answer details which comprises of possible answers and the right answer 



## Personality Test
Social media establishes uninterrupted connectivity, between its users and external world through revealing personal details and their viewpoints in every aspect of life. The focal aim of this here is to analyze how twitter (dataset) can be used to predict personality.
We show processes of developing  Machine Learning models on textual data. With this candidates can see their predicted personality types  according to Myers-Briggs Personality Types Indicator using their twitter user names since twitter is the classic entry point for practicing machine learning. With Twitter data, you got an interesting blend of data (tweet contents) and meta-data (location,hashtags, users, re-tweets, etc.) that opened up paths for analysis.
This training contains following topics:
* Exploratory Data Analysis
* Handling Imbalanced Dataset
* Vectorization of Text Data
* Model Creation
* Model Training
* Model Evaluation


### Dataset Description
The publicly available Myers–Briggs personality type dataset from Kaggle, containing 8675 rows
of data, was used in this research. In this dataset, each row consists of two columns. The first column
is for the MBTI personality type of a given person, and the second column includes fifty posts obtained
from the individual’s social media. Each post has been separated by three pipe characters . This data
has been collected from the users of an online forum, where in the first step, users take a questionnaire
that recognises their MBTI type; and in the second step, communicate with other users.

### Proportionality in the Dataset
In this step, matplotlib which is a Python 2D plotting library were used for data preview and to determine the distribution of the MBTI personality types in the dataset. 
            \\\Insert image here
The image above show a non-uniform representation of MBTI types in the dataset that is not
commensurate with the actual proportions of MBTI types. As a result, it was clear that some cleaning in the dataset would be necessary in order to improve the
accuracy of the proportional representation of each MBTI type. 

### Categorization of Type Indicators in Four Dimensions

Four different categories were created for the type indicators in order to understand the distribution of types indicators in the dataset. 

The first category was for Introversion (I)/Extroversion (E), the second
category was for Intuition (N)/Sensing (S), the third was for Thinking (T)/Feeling (F)and the fourthcategory was for Judging (J)/Perceiving (P). As a result, for each category, one letter will return and at the end there will be four letters that represent one of the 16 personality types in the MBTI. For instance, if the first category is returning I, the second category is returning N, the third category is returning T and the fourth category is returning J, the relevant personality type would be INTJ.

\\Insert Image here



For the first category of Introversion (I)/Extroversion (E),
the distribution of Introversion (I)  is much greater than Extroversion (E). Similarly, for the second
category which is Intuition (N)/Sensing (S), the distribution of Intuition
(N)  is much higher than Sensing (S). for the third category which is Thinking (T)/Feeling (F),
the distribution of Feeling (F)  is slightly more than Thinking (T). Finally, for the fourth category which
is Judging (J)/ Perceiving (P), the distribution of Perceiving (P)  is greater than Judging (J).


### WordCloud of Frequently Used Words
Word Cloud is a data visualization technique used for representing text data in which the size of each word indicates its frequency or importance. Significant textual data points can be highlighted using a word cloud. Word clouds are widely used for analyzing data from social network websites. Word cloud was used to analyze the most frequently used words for each of the personalities.

\\Insert Image here


### Pre-Processing the Dataset
As discussed earlier, data in this dataset was collected from an Internet forum and after analysing the content of the dataset, it was clear that some word removal is necessary. Non-uniform representation of MBTI types in the dataset that is not commensurate with the actual proportions of MBTI types in the general population was the most important reason for this. It was determined that this is because the
data was collected from an Internet forum created for discussion about personality type and MBTI
types were repeated too many times in the posts. This may also affect the accuracy of the model. As a
result, NLTK was used to remove the MBTI types from the dataset. After this step, the distribution
of MBTI personality types in the dataset was determined again. In addition, all urls and stop words were removed from the dataset. Finally, in order to
make the dataset more meaningful, the text was lemmatised, i.e., inflected forms of the words were transformed into their root words. Imbalanced data was also handled where the random over sampler function was used. This ensured that the categoraization of type indicatores in four dimenstions were balanced.

\\Insett Image here



## CV Analysis


## Results


## Disclaimer

WeEmploy is still an experimental prototype however instances fit for specific use cases can be spawned and developed for your use. In order to contact us for such an endeavor please check out the contributors for this project.
