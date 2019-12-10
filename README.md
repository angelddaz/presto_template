# presto_template
This is a blank presto single server/laptop template using presto version 0.227
Sensitive Catalog/Connection credentials have been replaced with empty strings.

# Requirements
1. Presto has a few basic [requirements](https://prestodb.io/overview.html):
  * Linux or Mac OS X
  * Java 8, 64-bit
  * Python 2.4+
  
  
# Installation
0. Requirements above
1. inside a terminal: `git clone git@github.com:angelddaz/presto_template.git ~/presto/`
2. Run `pip install -r requirements.txt` inside of this repository

# Running
1. The following bash command will run presto in port 8080
`~/presto/presto-server-0.227/bin/launcher run`
2. The following bash command will stop presto
`~/presto/presto-server-0.227/bin/launcher kill`
3. Jupyter notebook can be run with
`jupyter notebook ~/presto/cross-db-template.ipynb`
This notebook assumes you are running presto locally in port 8080


# Catalogs Included
Database connections are named Catalogs in Presto.
There are two catalog templates included in this template; MySQL and Postgres.
They can be found in `./presto-server-0.227/etc/catalog/`

# Jupyter Notebook Template
There is a single jupyter notebook file in this repository which has all python code needed for a cross database join.
