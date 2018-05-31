# Datmo Tutorials

This repository is a running list of tutorials showcasing how Datmo can be used in quantitative modeling projects.

The features addressed in these tutorials are as follows:

  * **Experiment logging** 
    * `snapshot create` (Record fully comprehensive project state)
  
  * **Project visualization** 
    * `snapshot ls` - View all snapshots
    * `snapshot diff` - Compare differences between two snapshots
    * `snapshot inspect` - See all info about a single snapshot
  
  * **State recreation & reproducibility** 
    * `snapshot checkout` - Revert to a project state from a different snapshot
  

For smaller examples with more isolated datmo feature demonstration, you can view the official core repository [here](https://github.com/datmo/datmo/tree/master/examples).

---

## Tutorials

### Python Tutorials

| Project  | Tags | Datmo Features |
| ------------- |:-------------:| -----|
| Kaggle Titanic Survivor Prediction | AutoML, TPOT, SVM | `snapshot create`, `snapshot ls` |
| Kaggle Jigsaw Toxic Comment Identification | NLP, bag of words | `snapshot create`, `snapshot ls` |


### R Tutorials

| Project  | Tags | Datmo Features |
| ------------- |:-------------:| -----|
| Kaggle Otto Product Classification | grid search, XGBoost | `snapshot create`, `snapshot ls` |
