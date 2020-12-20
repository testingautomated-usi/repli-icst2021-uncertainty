# Fail-Safe Execution of Deep Learning based Systems through Uncertainty Monitoring (Replication-Package)

This folder contains the source code for the reproduction of our empirical studies.

Limitations and notes:

- These exeperiments were executed using a very early version of `uncertainty-wizard`,
  pre-dating public releases. The dependency is thus not pip-downloadable.
  However, the code should be mostly compatible with `uncertainty-wizard v0.1.0`.
  We are happy to provide the sources of the (non-public) early version 0.0.14 upon request.
- Some of the used datasets (Traffic and ImageNet) need to be downloaded directly from their original sources
(copyright reasons). 
- Make sure to mount a drive `root/assets` to save the results and datasets
- For windows, install a venv according to the requirements.txt
- For linux, we recommend building a docker container according to the docker file in `docker/gpu/env/Dockerfile`.
  Optionally, this can be used to automatically create the docker container:
  > bash ./scripts/docker_build.sh -g emp_uncertainty.                                                                                                                                                                                       
- Some paths and system config (e.g. gpu selection) are workstation specific and you may have to change them.
                                                                                                                                                                                       
