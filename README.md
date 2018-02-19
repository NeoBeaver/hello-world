
## System Setup

Install [python3.5] (https://www.python.org/downloads/mac-osx/)


```
$ python --version
(make sure it is at least python 3.5)

```

## Initializing a git client

We use `venv` for depedency management. 

```
# clone this repo
$ git clone https://github.com/LEAP-ai/brain
$ cd brain/

# create a virtual environment
$ python -m venv brain_env

# activate the virtual environment
$ source brain_env/bin/activate

# now, you will see the environment name in the console
(brain_env) $ pip install -r requirements.txt

# (optiionall, if you plan to export a decision tree)
(brain_env) $ brew install graphviz

# run demo
(brain_env) $ python -m brain.magic8.demo

```


## Local server (auto recompile)

```
$ python -m brain.app.flask_server
```


## Test basic config

```
$ pytest brain
```

## Environments

```
$ LEAPMIND_CONFIG_NAME=dev

$ LEAPMIND_CONFIG_NAME=release

$ LEAPMIND_CONFIG_NAME=prod
```

## Deploy to appengine
 	
```
$ ./deploy-brain-dev.sh
$ ./deploy-brain-release.sh
$ ./deploy-brain-prod.sh

```


## System Setup

Install [python2.7](https://www.python.org/download/releases/2.7/)

We use `virtualenv` for dependency management.
```
$ pip install virtualenv
```

## Initializing a git client

```
# clone this repo
$ git clone https://github.com/LEAP-ai/brain
$ cd brain/

# create a virtual environment
$ virtualenv --no-site-packages brain_env

# activate the virtual environment
$ source brain_env/bin/activate

# now, you will see the environment name in the console
(brain_env) $ pip install -r requirements.txt

# run demo
(brain_env) $ python -m brain.magic8.demo

...
[skipped many lines]
...
<brain.magic8.algorithm.RandomAlgo object at 0x7fc6e2eb1ed0>
INFO 23:52:56.181  pull.py: 34 Load from cache alpha_source.1.0.pkl
INFO 23:52:56.401 __init__.py: 81 Running split: 0
INFO 23:52:56.403 __init__.py: 81 Running split: 1
INFO 23:52:56.405 __init__.py: 81 Running split: 2
INFO 23:52:56.407 __init__.py: 81 Running split: 3
precision@k: 0.3799 (0.0000, 0.8750) len: 24

# when you are done, deactivate the environment
(brain_env) $ deactivate
$
```

## Typical development cycle

```
# Go to repo
$ cd brain/

# activate the virtual environment
$ source brain_env/bin/activate

# run things...
(brain_env) $ ./b train brain.magic8.algorithm:IndustriesBayesianAlgo
# or
(brain_env) $ ./b eval brain.magic8.algorithm:IndustriesBayesianAlgo
# or
(brain_env) $ ./b train brain.exp.yipjsutin.strengthbased:variant

# when done, either close your terminal or deactivate
(brain_env) $ deactivate
$

```

## Environments

```
$ LEAPMIND_CONFIG_NAME=dev

$ LEAPMIND_CONFIG_NAME=release

$ LEAPMIND_CONFIG_NAME=prod
```

## Local server (auto recompile)

```
$ python -m brain.app.flask_server
```

## Deploy to appengine
 	
```
$ ./deploy-brain-dev.sh
$ ./deploy-brain-release.sh
$ ./deploy-brain-prod.sh

```


How to Install
--------------

 * Install Python 2.6 or newer and pip
    
 * Get Dependency:
 	$ pip install pdfminer   
 
 * To parse linkedin resume:
 	
 	$ python linkedin_parser/parser.py "<linkedinResumeFilePath>"

 * To start service on localhost:

 	$ python main.py
 	
 	```
 	POST http://localhost:5000/resumeParser
 	```
 	
 	```
 	{
 		"resumeUrl": "<linkedinResumeUrl>"
 	}
 	```

 	

## To run

```
[ you are at repo root]
$ cd ..
$ python -m brain.test2
```

