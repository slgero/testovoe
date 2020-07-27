# Image Classifier for Tiny ImageNet
## Introduction
You are presented with an opportunity to implement an Image Classifier for Tiny ImageNet dataset [same as used in CS231N](LINK). Tiny ImageNet contains 200 classes for training. Each class has 500 images. The test set contains 10,000 images. All images are 64x64 colored ones.

Your final goal is to demonstrate solid performance on the test split of the Tiny ImageNet dataset. We encourage you to show your thinking and demonstrate as many best practices along the way as you find appropriate.

We are looking for good analysis and presentation of the results, good problem decomposition and enough structure to allow for future foreseeable improvements. 

# Development
For your convenience, the team has created the environment using [Neuro Platform](https://neu.ro), so you can jump into problem-solving right away.

## Neuro Platform 
If you don’t have an account already, sign up at https://neu.ro
* Install neuro CLI: `pip install -U neuromation`
* Log in: `neuro login`
* Setup your project: `make setup`

## Directory Structure
| Mount Point              | Description                       | Storage URI                       |
|:------------------------ |:--------------------------------- |:--------------------------------- |
|`/project/data/`          | Dataset of interest               | `storage:test-task/data/`         |
|`/project/notebooks/`     | Jupyter notebooks                 | `storage:test-task/notebooks/`    |
|`/project/requirements/`  | pip and apt-get packages required | `storage:test-task/requirements/` |
|`/project/results/`       | Logs and results                  | `storage:test-task/results/`      |

## Developing in GPU Environment
* Setup development environment `make setup`
* Run Jupyter with GPU: `make jupyter`
* Kill Jupyter: `make kill_jupyter`
* Run tensorboard: `make tensorboard`

## Developing Locally

```shell
docker run \
    -p 8888:8888 \
    -v $(pwd)/data:/project/data \
    -v $(pwd)/code:/project/code \
    -v $(pwd)/notebooks:/project/notebooks \
    -v $(pwd)/results:/project/results \
    neuromation/base \
    'jupyter notebook --no-browser --ip=0.0.0.0 --allow-root --NotebookApp.token= --notebook-dir=/project/notebooks'
```

# References

* [Recipe for Training Neural Networks, A. Karpathy](https://karpathy.github.io/2019/04/25/recipe/)
