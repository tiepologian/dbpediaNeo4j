dbpediaNeo4j
============

Python script for importing DBpedia nodes and relationships into Neo4j.  
This script uses Redland Raptor's Python bindings to parse a dbpedia dump (ntriples format) and the neo4j-embedded Python library to create the graph db. You can download the latest DBpedia dump in nt format [here](http://downloads.dbpedia.org/3.9/en/mappingbased_properties_cleaned_en.nt.bz2) *(3.3GB unpacked)*.


## Installation
```
# Install dependencies
sudo apt-get install libraptor2-0 python-librdf python-jpype
sudo pip install neo4j-embedded

# Set the JAVA_HOME path it isn't set
export JAVA_HOME=/usr/lib/jvm/java-7-oracle/jre/

# Clone this git repository
git clone git@github.com:tiepologian/dbpediaNeo4j.git
```


## Usage
```
python dbpediaNeo4j.py /path/to/dbpedia/dump.nt
...wait a few hours...
Progress: 100%
Finished - 25,850,000 relationships imported in 39,820 seconds
Move dbpedia-graph.db to your Neo4j data directory ;-)
```
