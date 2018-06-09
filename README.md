# Datmo Tutorials

This repository is a running list of tutorials showcasing how [Datmo](https://github.com/datmo/datmo) helps users working with quantitative modeling projects (data science, machine learning, and artificial intelligence).

Prominent features addressed in the tutorials are as follows:

  * **Experiment logging** 
    * `snapshot create` - Record fully comprehensive project state as a single unit
  
  * **Project visualization** 
    * `snapshot ls` - View all snapshots in the project
    * `snapshot diff` - Compare differences/changes between two snapshots
    * `snapshot inspect` - See in-depth info about a single snapshot
  
  * **State recreation & reproducibility** 
    * `snapshot checkout` - Revert the project state to the version from a different snapshot
    * `datmo task run` - Run a containerized task for easy environment handling
  

For smaller examples with more isolated datmo feature demonstration, you can view the official core repository [here](https://github.com/datmo/datmo/tree/master/examples).

---

## Tutorials

### Python Tutorials

| Project  | Tags | Datmo Features |
| ------------- |:-------------:| -----|
| Kaggle Titanic Survivor Prediction <br> ([CLI](https://github.com/datmo/datmo-tutorials/tree/master/kaggle-titanic/cli) / [SDK in Jupyter Notebook](https://github.com/datmo/datmo-tutorials/tree/master/kaggle-titanic/sdk)) | AutoML, TPOT, SVM | `task run`, `snapshot create`, `snapshot ls` |
| Face Recognition (CLI in Jupyter Notebook) | CV, dlib, face_recognition | `task run`, `snapshot create`, `snapshot ls` |
| Keras Fashion MNIST (CLI in Jupyter Notebook) | CV, keras, tensorflow | `task run`, `snapshot create`, `snapshot ls` |
| Kaggle Jigsaw Toxic Comment Identification <br> ([CLI in Jupyter Notebook]()) | NLP, capsule net, Keras | `snapshot create`, `snapshot ls`, `env setup`, `notebook` |


### R Tutorials

| Project  | Tags | Datmo Features |
| ------------- |:-------------:| -----|
| Kaggle Otto Product Classification <br> ([CLI via R Notebook](https://github.com/datmo/datmo-tutorials/tree/master/otto-xgboost-R)) | grid search, XGBoost | `snapshot create`, `snapshot ls` |
