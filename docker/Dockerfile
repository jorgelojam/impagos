FROM jupyter/minimal-notebook

USER root
COPY binder /home/$NB_USER/binder
RUN fix-permissions /home/$NB_USER/binder

USER $NB_USER
RUN conda env update -q -n base -f /home/$NB_USER/binder/requirements.yml && \
    conda clean --all && \
    pip install --requirement /home/$NB_USER/binder/requirements.txt && \
    fix-permissions $CONDA_DIR && \
    fix-permissions /home/$NB_USER

USER root
COPY src /home/$NB_USER/src
COPY data /home/$NB_USER/data
RUN fix-permissions /home/$NB_USER

USER $NB_USER
