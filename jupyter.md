# Jupyter

## Locally
* if not done yet, install conda https://www.continuum.io/downloads
* jupyter is already installed with anaconda2 distribution
* run jupyter-notebook, it will open a window in your browser

## On meolkerg, with outputs locally
* create a directory notebooks on meolkerg
* run jupyter-notebook on meolkerg with this command : jupyter-notebook --port=8888 --ip=* --no-browser --notebook-dir notebooks
* launch locally this ssh command : ssh -L 8888:localhost:9999 -N -t -x youridmeolkerg@meolkerg.hmg.inpg.fr
* finally in your local browser, open localhost:9999 

## Do not forget to shut down the scripts in the the front page after closing them, or you will have to kill the processor
