# Overview
- doc: contains documentation
- docker: contains the build files for Docker
- iopenscad: the python module for this project
- openscad: Jupyter Kernel Specification

# Publish Project to PyPi
Here are the steps that are necessary to publish a new version

## Update Github
```
git add .
git tag V1.0.X
git commit -m "message"
git push origin master --tags
```

## Build wheel
```
python setup.py sdist bdist_wheel
```

## Publish
```
twine upload dist/*
```
