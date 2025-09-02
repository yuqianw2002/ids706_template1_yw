[![Python Template for IDS706](https://github.com/yuqianw2002/ids706_template1_yw/actions/workflows/main.yml/badge.svg)](https://github.com/yuqianw2002/ids706_template1_yw/actions/workflows/main.yml)

# IDS706_template1_yw
- A template for IDS706 project
- Clone/Start the repository locally or use GitHub Codespaces without a container.
- add the README.md file

## Setup Python Environment
```bash
python3 -m venv ~/.IDS706_python_template
source ~/.IDS706_python_template/bin/activate
```

## Create a Makefile
```makefile
install:
	pip install --upgrade pip &&\
		pip install -r requirements.txt

format:
	black *.py

lint:
	flake8 hello.py

test:
	python -m pytest -vv --cov=hello test_hello.py

clean:
    rm -rf __pycache__ .pytest_cache .coverage

all: install format lint test

```
## Create a requirements.txt file
```text
pylint
flake8
pytest
click
black
pytest-cov
```

## Run the Makefile 
```bash 
make install
```

## Create Python script
```python
def function_name():
    """Return the result that need """
    pass

def function_b():
    pass
```

## Create a test file
```python
from hello import function_name, function_b

def test_a():
    pass

def test_b():
    pass
```

## Run the tests
```bash 
make test
``` 
## Format the code
```bash 
make format
```
## Lint the code
```bash
make lint
```
## Clean up the environment
```bash
make clean
```

## Commit and push your changes via commands or User Interface
```bash
git add .
git commit -m "Initial commit with Python template setup"   
git push origin main
