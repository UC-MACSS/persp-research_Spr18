# MACS 30200 - Perspectives on Computational Research (Spring 2018)

|  | [Dr. Richard Evans](https://sites.google.com/site/rickecon/) | [Dr. Benjamin Soltoff](http://www.bensoltoff.com/) |
|--------------|--------------------------------------------------------------|----------------------------------------------------|
| Email | rwevans@uchicago.edu | soltoffbc@uchicago.edu |
| Office | 208 McGiffert House | 209 McGiffert House |
| Office Hours | W 2:30-4:30pm | Th 2-4pm |
| GitHub | [rickecon](https://github.com/rickecon) | [bensoltoff](https://github.com/bensoltoff) |

* **Meeting day/time**: MW 11:30am-1:20pm, Saieh Hall, Room 247
* Graders: Sushmita V. Gopalan & Xingyun Wu
* Office hours also available by appointment

## Course description

This course focuses on applying computational methods to conducting social scientific research through a student-developed research project. Students will identify a research question of their own interest that involves a direct reference to social scientific theory, use of data, and a significant computational component. The students will collect data, develop, apply, and interpret statistical learning models, and generate a fully reproducible research paper. We will identify how computational methods can be used throughout the research process, from data collection and tidying, to exploration, visualization and modeling, to the final communication of results. The course will include modules on theoretical and practical considerations, including topics such as epistemological questions about research design, writing and critiquing papers, and additional computational tools for analysis.

## Grades

|     Assignment              | Points | Quantity | Total points |
|-----------------------------|--------|----------|--------------|
| Proposal                    |    10  |      1   |        10    |
| Literature review           |    15  |      1   |        15    |
| Methods/initial results     |    15  |      1   |        15    |
| Peer evaluations of posters |     2  |      5   |        10    |
| Poster presentation         |    30  |      1   |        30    |
| Final paper                 |    40  |      1   |        40    |
| Problem set                 |    10  |      4   |        40    |
| **Total Points**            |        |          |       160    |

Students will turn assignments in via their own public GitHub repository named `MACS30200proj`. The directory structure of this repository should be the following.

* `github.com/YourGithubHandle/MACS30200proj`
  * ProblemSets
    * PS1
    * PS2
    * PS3
    * PS4
  * Proposal
  * LitReview
  * MethodsResults
  * Poster
  * FinalPaper


## Late Problem Sets

Late problem sets will be penalized 2 points for every hour they are late. For example, if an assignment is due on Monday at 11:30am, the following points will be deducted based on the time stamp of the last commit.

| Example PR last commit | points deducted |
| ---------------------- | --------------- |
| 11:31am to 12:30pm     | -2 points       |
| 12:31pm to 1:30pm      | -4 points       |
| 1:31pm to 2:30pm       | -6 points       |
| 2:31pm to 3:30pm       | -8 points       |
| 3:30pm and beyond      | -10 points (no credit) |


## Disability services

If you need any special accommodations, please provide us with a copy of your Accommodation Determination Letter (provided to you by the Student Disability Services office) as soon as possible so that you may discuss with me how your accommodations may be implemented in this course.


## Course schedule (lite)

| Date | Day | Topic | Reading | Assignment due dates |
|--------|-----|---------------------------|-------------|---------------------------------|
| Mar 26 | M | Overview/reproducibility in science | [Slides](slides/fundamentals-slides.html) |  |
| Mar 28 | W | Abstract/intro/conclusion | [Slides](slides/IntroAbsConcl_slides.pdf) |  |
| Apr  2 | M | Theory section of paper | [Slides](slides/TheorySection_slides.pdf) |  |
| Apr  4 | W | Proposal presentations |  | [Proposal slides & present](assignments/project-proposal.md) |
| Apr  9 | M | Data/methods section of paper | [Slides](slides/data-methods-slides.html) |  |
| Apr 11 | W | Computational results section of paper | [Slides](slides/results-slides.html) |  |
| Apr 16 | M | Kernel density estimation | [Notes_a](notebooks/KDE/KDE.ipynb) | [PS1](assignments/ps1.md) |
|        |   |                           | [Notes_b](notebooks/KDE/05.13-Kernel-Density-Estimation.ipynb) |   |
| Apr 18 | W | Interaction terms | [Notes](http://cfss.uchicago.edu/persp013_interaction_terms.html) |  |
| Apr 23 | M | Parallel computing | [Notes](notebooks/Parallel/parallel.ipynb) | [Literature review section](assignments/lit-review.md) |
| Apr 25 | W | Workshop papers/office visits |  |  |
| Apr 30 | M | Missing data | [Notes](http://cfss.uchicago.edu/persp014_missing_data.html) | [PS2](assignments/PS2/PS2.pdf) |
| May  2 | W | Deep learning with Python/R | DL ch. 1-2 |  |
| May  7 | M | Deep learning with Python/R | DL ch. 3-4  |  |
| May  9 | W | Deep learning with Python/R |  | [Methods/initial results section](assignments/methods-results.md) |
| May 14 | M | Workshop papers/office visits |  |  |
| May 16 | W | Effective presentations, poster,slides | [Notes](http://cfss.uchicago.edu/persp018_presenting_research.html)  | [PS3](assignments/ps3.md) |
| May 21 | M | Markov and hidden Markov models | [Notes](https://github.com/UC-MACSS/persp-research_Spr18/blob/master/notebooks/Markov/Markov.ipynb) |  |
| May 23 | W | Markov and hidden Markov models |  |  |
| May 28 | M | **No class (Memorial Day Holiday)** |  | [PS4](assignments/PS4/PS4.pdf) |
| May 30 | W | In-class poster presentations |  | Poster |
| Jun  6 | W | Final papers due at 5:00pm |  | Papers due |

## References and Readings ##

All readings are required unless otherwise noted. Adjustments can be made throughout the quarter. Be sure to check this repository frequently to make sure you know all the assigned readings.

* Data/methods section
    * [Broockman, D. E., & Skovron, C. (2018). Bias in Perceptions of Public Opinion among Political Elites. *American Political Science Review*, 1-22.](https://www.cambridge.org/core/journals/american-political-science-review/article/bias-in-perceptions-of-public-opinion-among-political-elites/2EF080E04D3AAE6AC1C894F52642E706/share/1bd83a8a05b6ac177c51e7a19aee1c55f3ef4b97)
    * [Kalla, J. L., & Broockman, D. E. (2016). Campaign contributions facilitate access to congressional officials: A randomized field experiment. *American Journal of Political Science*, 60(3), 545-558.](https://onlinelibrary.wiley.com/doi/full/10.1111/ajps.12180)
* Interaction terms
    * [Brambor, T., Clark, W. R., & Golder, M. (2006). Understanding interaction models: Improving empirical analyses. *Political analysis*, 63-82.](http://www.jstor.org.proxy.uchicago.edu/stable/25791835)
* Deep learning with Python/R
    * [Chollet, F. (2017). *Deep learning with Python*. Manning Publications.](https://www.manning.com/books/deep-learning-with-python)
    * [Chollet, F. with J.J. Allaire (2018). *Deep learning with R*. Manning Publications.](https://www.manning.com/books/deep-learning-with-r)
