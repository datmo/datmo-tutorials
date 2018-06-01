# Otto Dataset Tutorial (XGBoost, R)

## Info
In this example, we'll walk through how to use Datmo to log your experiments and model versions while you work through a Kaggle competition problem. Whether it's continuing by using a fork of someone else's kernel, or trying to track your newest models, Datmo snapshots help you seamlessly revert between versions and visualize all of the results in one place.

All data needed for the tutorial is included in the `/input/` directory.

The example notebook (`notebook.Rmd`) will cover the following:

* Getting Started
    * Preface (background info)
    * Introduction (Explaining what XGBoost does)
    * Setup (Installation of packages/Datmo)
* Initial Model
    * Data Prep
    * Train original model
    * Create Snapshot
    * Model Understanding (optional)
        * Feature Importance
        * Interpretation
        * Tree Graph
* Improved Model
    * Search space setup
    * Perform grid search
    * Train second model using optimal params
    * Model validation
    * Create snapshot

## To begin:
* Open RStudio(if on MacOS, use `open -a RStudio` to avoid PATH issues).

* Follow the instructions and cells from top to bottom.

## Things to watch out for:
1. In the case the RStudio console/terminal cannot detect Datmo, it's likely a PATH issue. You can use `echo $PATH` from the console to see where it is currently pointed.

2. Try restarting RStudio if you installed Datmo after opening the app.
