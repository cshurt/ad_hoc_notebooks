# ad_hoc_notebooks
Ad-hoc analyses performed in jupyter notebooks.

The jupyter environment I'm using is a jupyter server hosted in a docker container.
The dockerfile comes from Jupyter's [scipy-notebook docker stack](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html).
I initiate the file with the following shell command from my linux environment:

```
# Run a container
docker run --rm \
# Open the jupyter port
-p 8888:8888 \
# Mount a local clone of my git repo
--mount type=bind,source=$(echo ~)/ad_hoc_notebooks,target=/home/jovyan/ad_hoc_notebooks \
# Launch a specific notebook
jupyter/scipy-notebook \
# Start a jupyter lab server
start.sh jupyter lab
```
