# presto_template
This is a blank presto single server/laptop template using presto version 0.227
Sensitive Catalog/Connection credentials have been replaced with empty strings.

# Requirements
1. Presto has a few basic [requirements](https://prestodb.io/overview.html):
  * Linux or Mac OS X
  * Java 8, 64-bit -- this one was the trickiest req for me
  * Python 2.4+
  
# Deploying Single Presto Server 
0. Requirements above
1. Visit https://prestodb.io/download.html and download `presto-server-0.229.tar.gz` or latest version.
2. Extract the `presto-server-0.229.tar.gz` gzip file and move to a directory. You can delete the original gzip file after extrtacting.
  * This guide will depend on moving the extracted directory into the `~/presto/presto-server-0.229/` location
3. Download this repository
  * `git clone git@github.com:angelddaz/presto_template.git /tmp/presto`
4. Move /etc/ from this repository into your presto-server folder.
  * `mv /tmp/presto/etc ~/presto/presto-server-0.229/`
5. Run presto in the background from any directory in the command line with the following command
  * `~/presto/presto-server-0.229/bin/launcher start`
6. Visit http://localhost:8080/ in your browser will show you a UI for presto
7. Kill presto with
  * `~/presto/presto-server-0.229/bin/launcher kill`


# Running with Jupyter Notebook
0. Complete `Deploying Single Presto Server section`
1. Run `pip install -r /tmp/presto/requirements.txt` from the repository download above if you haven't yet.
2. The following bash command will run presto in port 8080
  * `~/presto/presto-server-0.227/bin/launcher run`
3. Move the template jupyter notebook from the temporary repository location and run it locally with the following commands
  * `mv ~/tmp/presto/cross-db-template.ipynb ~/presto/`
  * `jupyter notebook ~/presto/cross-db-template.ipynb &`
5. visiting `http://localhost:8888/` in your browser will show you a UI for Jupyter


# Deploying Presto CLI
0. Requirements specified above Single Presto Server installation
1. Visit https://prestodb.io/download.html and download `presto-cli-0.229-executable.jar`
2. Move this jar file into the home presto location while renaming it to `presto-cli`
   * `mv ~/Downloads/presto-cli-0.229-executable.jar ~/presto/presto-cli`
3. Make this jar file executable
   * `chmod +x ~/presto/presto-cli`
4. Run from any directory in the command line with the following command
   * `~/presto/presto-cli`
5. Check if it is running with following CLI command
   * `SHOW CATALOGS`
6. Kill with `exit`


# Catalogs Included
Database connections are named Catalogs in Presto.
There are two catalog templates included in this template; MySQL and Postgres.
They can be found in `etc/` directory

# Jupyter Notebook Template
There is a single jupyter notebook file in this repository which has all python code needed for a cross database join.
