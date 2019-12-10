# presto_template

This is a blank presto single server/laptop template using presto version 0.227
Sensitive Catalog/Connection credentials have been replaced with empty strings.

# Requirements
1. you need to run `pip install -r requirements.txt` inside of this repository
2. Presto has a few basic [requirements](https://prestodb.io/overview.html):
  * Linux or Mac OS X
  * Java 8, 64-bit
  * Python 2.4+

# Catalogs Included
Database connections are named Catalogs in Presto.
There are two catalog templates included in this template; MySQL and Postgres.
