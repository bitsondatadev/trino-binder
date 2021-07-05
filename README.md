# trino-binder

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/bitsondatadev/trino-binder/HEAD)

The goal of this binder is to offer a quick and easy way to showcase Trino for those that are either not familiar with Docker to run examples in the [Trino Getting Started repository](https://github.com/bitsondatadev/trino-getting-started) or they don't have a computer that can support some of these examples, or simply just want the convenience of pushing a button to play with Trino and run these scenarios with data science examples.

This is a binder project that builds on the [Juptyer Project's](https://github.com/jupyter) [Docker stack](https://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html) image [`trino-notebook`](https://github.com/bitsondatadev/trino-notebook) which builds off of the jupyter project maintained [`scipy-notebook`](https://github.com/jupyter/docker-stacks/tree/master/scipy-notebook).

The Dockerfile was build acccording to the [documentation Binder provides](https://mybinder.readthedocs.io/en/latest/tutorials/dockerfile.html).
The repo2docker [config files](https://mybinder.readthedocs.io/en/latest/using/config_files.html) are used to generate the final docker image that is used by binder.

Although it would have been nice to use the Trino Docker image, there is no way for me to extend my own Dockerfile and start Trino with my own command as the [CMD/ENTRYPOINT calls](https://github.com/jupyterhub/binder/issues/87) are overridden based on Binder setup.

## TODO
* Make Docker Image more compact: https://discourse.jupyter.org/t/how-to-reduce-mybinder-org-repository-startup-time/4956
* May consider adding [IJava kernel](https://github.com/SpencerPark/IJava) at some point.
* Also may consider contributing to the [community stacks](https://jupyter-docker-stacks.readthedocs.io/en/latest/contributing/stacks.html) as well.
