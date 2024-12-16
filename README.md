# Hybrid quantum-classical unsupervised data clustering based on the Self-Organizing Feature Map

Quantum assisted Self-Organizing Feature Map

Unsupervised machine learning is one of the main techniques employed in artificial intelligence.
Quantum computers offer opportunities to speed up such machine learning techniques.
Here, we introduce an algorithm for  quantum assisted unsupervised data clustering using the self-organizing feature map, a type of artificial neural network.
We make a proof-of-concept realization of one of the central components on the IBM Q Experience
and show that it allows us to reduce the number of calculations in a number of clusters.
We compare the results with the classical algorithm on a toy example of unsupervised text clustering.

## Make PDF 

```
make -C manuscript
```

## Run notebooks

### Setup environment

```shell
python3.8 -m venv <path/to/venv>
source <path/to/venv>/bin/activate
```


### Install dependencies

```shell
pip install -r requirements.txt
```


### Download necessary data for [NLTK](https://www.nltk.org/install.html) 

```shell
python -m nltk.downloader punkt 
python -m nltk.downloader wordnet
```


### Create IPython Kernel

```shell
pip install ipykernel
python -m ipykernel install --name qasofm-py3.8 --user
```


### Set proxy configuration for Qiskit if necessary

```shell
$ cat ~/.qiskit/qiskit-ibm.json
{
    "default-ibm-quantum": {
        "channel": "ibm_quantum",
        "private_endpoint": false,
        "proxies": {
            "urls": {
                "https": "https://<username>:<password>@<endpoint>"
            }
        },
        "token": "<token>",
        "url": "https://auth.quantum-computing.ibm.com/api"
    }
}
```
