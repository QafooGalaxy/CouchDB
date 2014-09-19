# CouchDB

## Description

Install and configure an [Apache CouchDB]().

## Usage

```yaml
- role: CouchDB
```

## Configuration

*optional* `url`: Url to fetch CouchDB archive from (Default:
`http://artfiles.org/apache.org/couchdb/source/1.6.0/apache-couchdb-1.6.0.tar.gz`).

*optional* `path`: Path inside the archive where the CouchDB resides. (Default:
`apache-couchdb-1.6.0`).

**Note:** *Usually those configuration options do not need to be changed.
Utilize the different tagged versions of this repository instead to install
different couchdb versions*

## Implicit Dependencies

- BuildEnvironment
- Erlang
- Spidermonkey
- ICU
