cloud-costs README
==================

![Travis CI](https://travis-ci.org/blentz/cloud-costs.svg?branch=master "Travis CI")
[![Licensed under Apache License version
2.0](https://img.shields.io/badge/license-Apache%202-blue.svg)](https://raw.githubusercontent.com/openshift/cloud-costs/master/LICENSE)

This is a project using the Pyramid framework (http://www.pylonsproject.org/).

The purpose is to develop a set of utilities and tools that provides meaningful
information for tracking costs and usage associated with running infrastructure
on top of cloud services.

Getting Started
---------------

```
cd <directory containing this file>

$VENV/bin/python setup.py develop

$VENV/bin/initialize_budget_db development.ini

$VENV/bin/pserve --reload development.ini
```

Data Ingestion Scripts
----------------------

There are several scripts used for managing ingesting data into the database.
These scripts can be found in `<this directory>/budget/scripts`.

Most of them can be run from the command line using this syntax:

`python -m 'budget.scripts.<module name>' /path/to/development.ini`

There are also some shell scripts in `<this directory>/cron` aimed at enabling
scheduled automatic data ingestion via cron.
