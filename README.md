# AdaptiveRandomForestRegressor
This repository includes the adaptive random forest algorithm adaptation for regression tasks (AKA ARF-Reg). It uses as the base learner the FIMTDD decision tree algorithm. Look up the publication for more details.  Initially, ARF-Reg was implemented in a previous version of MOA, but this repository is based on MOA 2018.06. 

## Citing AdaptiveRandomForestRegressor
To cite this ARF-Reg in a publication, please cite the following paper: 
> Heitor Murilo Gomes, Jean Paul Barddal, Luis Eduardo Boiko Ferreira, Albert Bifet.
> Adaptive random forests for data stream regression.
> In European Symposium on Artificial Neural Networks, Computational Intelligence and Machine Learning (ESANN), 2018.
> PDF: https://www.elen.ucl.ac.be/Proceedings/esann/esannpdf/es2018-183.pdf

## Important source files
If you are here, then you are probably looking for the implementations used in the original AdaptiveRandomForestRegressor paper, which are:
* AdaptiveRandomForestRegressor.java: The ensemble learner AdaptiveRandomForestRegressor
* ARFFIMTDD.java: The base tree learner used by AdaptiveRandomForest

All the other classes are from [MOA](https://github.com/Waikato/moa). Notice that this repository is based on MOA 2018.06. In the future, these classes (AdaptiveRandomForestRegressor.java and ARFFIMTDD.java) might need some adaptation to work in future versions (as of 2018 they are working just fine). 

## How to execute it 
You can copy and paste the following command in the interface (right click the configuration text edit and select "Enter configuration”).
Sample command: 

`EvaluatePrequentialRegression -l (meta.AdaptiveRandomForestRegressor -l (ARFFIMTDD -k 4 -s VarianceReductionSplitCriterion)) -i 1000000`
