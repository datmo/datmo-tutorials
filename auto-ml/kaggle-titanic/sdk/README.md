# auto-ml 

## CLI

#### 1. Kaggle Titanic Competition

##### a. Introduction

This tutorial is using the "Getting Started" competition from Kaggle [Titanic competition](https://www.kaggle.com/c/titanic) to showcase how we can use Auto-ML along with datmo, in order to track our work and make machine learning workflow reprocible and reusable. Some part of data analysis is inspired from this [kernel](https://www.kaggle.com/sinakhorami/titanic-best-working-classifier)

##### b. Installation
To use `datmo`, you can install it using `pip install datmo` after having the prerequisites as in this [README](https://github.com/datmo/datmo)

To run the `experimentation.ipynb` file, install the following libraries,

* [NumPy](http://www.numpy.org/)
* [SciPy](https://www.scipy.org/)
* [scikit-learn](http://www.scikit-learn.org/)
* [pandas](http://pandas.pydata.org)
* [xgboost](http://xgboost.readthedocs.io/en/latest/build.html)
* [tpot](http://epistasislab.github.io/tpot/installing/)
* [jupyter notebook](http://jupyter.readthedocs.io/en/latest/install.html)

We can look into the benefit in running the task using `datmo task run` which uses docker containers to encapsulate the environment. This will be done in a different tutorial.

##### c. Solution

After the installation, we run the `experimentation.ipynb` notebook and perform following steps,

1. Exploratory Data Analysis (EDA)
2. Data Cleaning
3. Using Auto-ML to figure out the best algorithm and hyperparameter

For auto-ml, we use the tpot algorithm, which works as follows,
![](./images/usage_auto-ml.png)

##### d. Creating versions or snapshots

During the process of EDA, data cleaning and algorithm selection, we would be using datmo to create versions of work by creating datmo snapshots. As you see below, we created three snapshots at the end of the notebook tutorial. More information about the flow can be found in the notebook file.  

```bash
home:~/datmo-tutorials/auto-ml$ datmo snapshot ls
+---------+-------------+-------------------------------------------+-----------------+---------------+-------+
|    id   |  created at |                 config                    |   stats         |      message  | label |
+---------+-------------+-------------------------------------------+-----------------+---------------+-------+
| 30f8366b|  2018-05-16 | {u'selected features': [u'Sex', u'Pclass',|{u'accuracy':    |   auto-ml-2   |  None |
|         |   03:04:06  |  u'Age', u'Fare', u'Embarked', u'Title',  |   0.8295964}    |               |       |
|         |             |   u'FarePerPerson', u'FamilySize']}       |                 |               |       |
| adf76fa7|  2018-05-16 | {u'selected features': [u'Sex', u'Pclass',|{u'accuracy':    |   auto-ml-1   |  None |
|         |   01:24:53  |  u'Age', u'Fare', u'Embarked',            |   0.8206278}    |               |       |
|         |             |   u'Fare', u'IsAlone', u'Title']}         |                 |               |       |
| 30803662|  2018-05-15 | {u'features analyzed': [u'Sex',           |    {}           |     EDA       |  None |
|         |   23:15:44  |  u'Pclass', u'FamilySize', u'IsAlone',    |                 |               |       |
|         |             |  u'Embarked', u'Fare', u'Age', u'Title']} |                 |               |       |
+---------+-------------+-------------------------------------------+-----------------+---------------+-------+
```
Now after the creation of snapshots, we can perform checkout to a different version with the following command,
```bash
home:~/datmo-tutorials/auto-ml$ datmo snapshot checkout --id adf76fa7
```
This gives me all files present in that specific version providing reproducibility
