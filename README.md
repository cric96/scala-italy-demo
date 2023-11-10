# Scala Italy Demo
## Integrating Python Machine Learning with Scala using ScalaPy

Welcome to the Scala Italy Demo, 
where I'll demonstrate the integration of Python's machine learning capabilities within a Scala environment, 
leveraging the power of ScalaPy. 
This demonstration is an part of my [presentation](https://onedrive.live.com/edit.aspx?resid=33D32A898B88D984!134&ithint=file%2cpptx&wdo=2&authkey=!AM68koSgG4PPvkw), 
which covered the diverse applications of Scala in academia, from teaching to research.

[ScalaPy](https://scalapy.dev/) is a groundbreaking Scala library that bridges the gap between Scala and Python, 
offering seamless access to Python's extensive libraries and tools. 
In this session, I'll guide you through using [Almond](https://almond.sh/)—a Scala kernel for Jupyter notebooks—in conjunction with ScalaPy. 
This combination replicates a Python-like experience in the realms of data science and machine learning, but within the Scala ecosystem.

Stay tuned for a hands-on experience that showcases the synergy between Scala and Python in modern computing!

## Startup Instructions

Before beginning the installation process, ensure you have a suitable Python environment setup. 
We recommend using `pyenv` or another Python environment manager like `conda`. 
This will help manage dependencies and isolate your Python setup effectively.

Additionally, you need a functioning local Java installation, version 1.8 or higher.

### Python Version Compatibility
It's important to use a Python version that is compatible with ScalaPy. 
Please ensure your Python version is greater than 3.7 but less than 3.10. 
Versions outside this range might cause issues with ScalaPy recognizing Python libraries.

### Installing Jupyter Notebook
First, install [Jupyter Notebook](https://jupyter.org/) if you haven't already. This can be done via the following pip command:
```
pip install notebook
```

### Setting Up Almond
Next, install the local [Almond](https://almond.sh/) engine. 
Almond acts as a Scala kernel for Jupyter, 
allowing you to run Scala code within Jupyter notebooks. 
Run the following commands in your terminal:
```
curl -Lo coursier https://git.io/coursier-cli
chmod +x coursier
./coursier launch --fork almond -- --install
rm -f coursier
```
With these steps, you'll have set up the necessary environment to integrate Scala with Python machine learning tools.

If you don't want to install anything locally, you can exploit the Docker image that I've prepared:
```
docker run -p 8888:8888 gianlucaaguzzi/scalapy-almond-base
```

## Content
This repository primarily features two Jupyter notebooks demonstrating the capabilities of ScalaPy:

1. [scalapy-intro.ipynb](https://github.com/cric96/scala-italy-demo/blob/main/scalapy-intro.ipynb): This notebook introduces the fundamental concepts of ScalaPy, including types, facade creation, and utilization of Python modules within Scala. It provides a comprehensive guide to understanding the basics of ScalaPy integration.

2. [data-science-with-scalapy.ipynb](https://github.com/cric96/scala-italy-demo/blob/main/data-science-with-scalapy.ipynb): In this notebook, I present a practical example of creating a facade in ScalaPy. It showcases how ScalaPy enables a scripting language experience with the added benefits of a typed environment, ideal for data science applications.
