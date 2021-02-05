# Ketamine project

> scRNA-seq analyses

[![](/readme.png)]()

## Structure
```
ketamine_reproducibility
|-- README.md
|   
|-- docker
|   |-- Dockerfile
|   \-- python-packages.txt
\-- notebooks
    |-- 01-qc_preprocessing.ipynb
    |-- 02-annotation.ipynb
    |-- 03-differential_testing.ipynb
    |-- 04-figures.ipynb
    \-- gini.py
```

## Installation

We provide a Dockerfile with all the packages required to run the analyses. To build the Docker image use the command:
```shell
docker build docker -t ketamine:final
```

After the image is compiled, you can run it interactively using:

```shell
docker run --interactive --tty --name ketamine --publish 8888:8888 --volume $HOME:/root/host_home --workdir /root ketamine:final  /bin/bash
```

This will start a container, in order to start a JupyterLab session use the alias:

```shell
jl
```

## License

[![License](http://img.shields.io/:license-mit-blue.svg?style=flat-square)](http://badges.mit-license.org)

- **[MIT license](http://opensource.org/licenses/mit-license.php)**
