# Graduate-Admission-Predictions

Every stduent aiming to pursue master's in some STEM degree has to go through the tedious process of listing out possbile colleges accoring to his/her profile. So naturally the question arises what kind of factors does the committee takes into account in giving possible admits to student. Mainly factors such as SOP , LOR's , Resume's , GRE scores and some other factors are looked upon when the admission's committee is looking at a profile.

## The Question

Now this era is data driven and everyone is using ML and DL tech in varied ways. So can we use the same techniques to tackle this problem ?
The answer's complicated mainly because the content in SOP ,LOR ,Resume's ,etc is subjective and GRE,TOEFL score ,CGPA ,etc are numeric.
So an approach would be to use the strength of SOP , LOR's on scale of 0-5 which will very sparsely represent the features of SOP and LOR's. Yet some of NLP must be done SOP and LOR's to extract the info and to eventually understand some kind of sentiment behind it i.e the **"WHY?"** behind the SOP's. This may guve us some strong indicators about SOP.

## Analysis on the collected data

The dataset has features viz GRE scores  , TOEFL scores , University Ranking , Research Exp , CGPA , SOP and LOR strength and the target variable is chance of admit i.e the probability that given these features an individual can get an admit.

There are some interesting trends observed , I will share the plots and insights below..

* **Gre Scores**

![Gre](https://github.com/Atharva-Phatak/Graduate-Admission-Predictions/blob/master/images/GRE_scores.png)

So the average GRE scores are in range between 310 - 320.

* **Toefl Scores**

![Toefl](https://github.com/Atharva-Phatak/Graduate-Admission-Predictions/blob/master/images/Toefl.png)

The average TOEFL scores are above a 100.

* **CGPA vs GRE && CGPA vs TOEFL**

Can this be possible that a student who as a highr CGPA will also score good in GRE and TOEFL ?
![cgpa](https://github.com/Atharva-Phatak/Graduate-Admission-Predictions/blob/master/images/CGPA%20vs%20GRE.png)
![cgpa vs toefl](https://github.com/Atharva-Phatak/Graduate-Admission-Predictions/blob/master/images/CGPA%20vs%20TOEFL.png)

Yes our hunch was right , one can see a positive correlation between the CGPA , GRE and the TOEFL i.e as the CGPA increases the scores do increase too.

* **CGPA vs University Rating** 

Can students with a better university rating have better CGPA than lower rated ones ?

![univ](https://github.com/Atharva-Phatak/Graduate-Admission-Predictions/blob/master/images/CGPA%20vs%20UNIV%20Rating.png)

Indeed it is true , there's a positive correlation between CGPA and Univ Rating too.

* **Correlation Plot**
Here's the Correlation plot , I used SNS for this visualization.

![corr](https://github.com/Atharva-Phatak/Graduate-Admission-Predictions/blob/master/images/correlation.png)


## Results 

The models used for prediciton were Ridge Regression , SVR , Random Forest Regression , AdaBoost Regression , a simple ANN and a stacked Generalization.
The metrics used were RMSE , MSE , Log MSE , R2-score

Here's the results of what scores were obtained for relative models

![results](https://github.com/Atharva-Phatak/Graduate-Admission-Predictions/blob/master/output/results.JPG)

## To - Do

- [ ] Gather more data and gather university related like prefrences , the applied university ranking , fees , etc
- [ ] Create a GUI and make it user friendly
- [ ] Get actual SOP's , LOR's and extract the important features using NLP techniques

## Requirements

* Python 3.6
* Sklearn
* Matplotlib
* Seaborn
* Pandas
* Numpy
