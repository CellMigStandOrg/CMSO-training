Training material for the CMSO formats and API
==============================================

This repository contains training material for the formats and API developed by the [Cell Migration Standardisation Organisation](http://cmso.science/).

Run using Binder
----------------

[Binder](https://mybinder.org/) (see [their documentation](https://mybinder.readthedocs.io/en/latest/)) allows you to run [Jupyter notebooks](http://jupyter.org/) hosted on Github 
in an online executable environment. Thus, you do not need to install any libraries if you use this route. Just click in the logo below.  

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/CellMigStandOrg/CMSO-training/master)

Run locally using Docker
------------------------

In order to execute the notebooks locally, you can build the Dockerfile stored in the
top-level of this repository:


    docker build -t cmso-jupyter .
    docker run --rm -it -p 8888:8888 cmso-jupyter

Use the URL shown in the startup message, including the token, to access the
notebook server from your browser.

For persistence, and to use existing notebooks, you can mount a host directory
to `/home/jupyter/notebooks` in the container:

    docker run --rm -it -p 8888:8888 -v $(pwd):/home/jupyter/notebooks cmso-jupyter



