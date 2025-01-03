# Readme for coral

Coral is the name of my personal project for experimenting with different programming languages and technologies for manipulating and serving information on biological taxonomies and names, as well as different solutions for creating checklists and reporting observations. Especially for birds. This has been an ongoing project, with very varying commitment for around 25 years. A lot of older code is not in this repository

Coral will have an HTTP API that serves information on biological taxonomies and species names. It also comprises a few command line tools for importing taxonomical data to the system from different sources.

Copyright (C) 1998-2024 Paul Cohen. This software is licensed under the GNU Affero General Public License version 3. See the file [agpl.md](agpl.md) in this directory.

## Development

### Requirements

 * Python 3 & virtualenv.
 * Flask
 * Docker for running the HTTP API server.

### Setup development

Set up a Python virtualenv in the top directory of this project:
```bash
$ virtualenv env
```

Jump into to the virtualenv and install required Python modules:
```bash
$ source env/bin/activate
(env) $ pip install -r requirements.txt
```

### Build

TBD.

### Run locally

TBD.

### Tests

There exists a pytest-based test script `test_readers-py` for the tools scripts in the `tools/` directory. It can be run from the root directory with:
```
$ pytest -v
```
It will create a `testdata/` directory, as a result of running the tests.

### Directory structure

 * 'data' contains taxonomic data files from external data sources.
 * 'api' contains source code for the HTTP API server.
 * 'tools' contains source code for various data import and transformation scripts.

## Data sources

The two data sources used, are [IOC Master lists](https://www.worldbirdnames.org/new/ioc-lists/master-list-2/) and [Birdlife Sweden's official list of Swedish names of birds](https://birdlife.se/tk/svenska-namn-pa-varldens-faglar/).

## References

Websites:
* [IOU Working Group Avian Checklists](https://www.internationalornithology.org/working-group-avian-checklists).
* [IOC World Bird List](https://www.worldbirdnames.org/new/).
* [Birdlife Sweden Taxonomic Committee (Taxonomikommittén)](https://birdlife.se/tk/).

Books:
* [Describing Species, by Judith E. Winston, 1999, Columbia University Press](https://cup.columbia.edu/book/describing-species/9780231068246).
* [Species: The Evolution of the Idea, by John S. Wilkins, 2021, Routledge](https://www.routledge.com/Species-The-Evolution-of-the-Idea-Second-Edition/Wilkins/p/book/9780367657369).
