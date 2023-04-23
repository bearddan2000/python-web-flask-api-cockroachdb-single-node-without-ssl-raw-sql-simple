# python-web-flask-api-cockroachdb-single-node-without-ssl-raw-sql-simple

## Description
Creates an api CRUD of `dog` for a flask project, using raw sql.

A python flask build, that connects to single node cluster
cockroach database without ssl.

If path is not found, will default to 404 error.

Remotely tested with *testify*.

## Tech stack
- python
  - flask
  - sqlalchemy
  - testify
  - requests
- bootstrap
- jquery
- dataTable
- cockroachdb

## Docker stack
- python:latest
- cockroachdb/cockroach:v19.2.4

## To run
`sudo ./install.sh -u`
- Get all dogs: http://localhost/dog
  - Schema id, breed, and color
- CRUD opperations
  - Create: curl -i -X PUT localhost/dog/<id>
  - Read: http://localhost/dog/<id>
  - Update: curl -i -X POST localhost/dog/<id>/<breed>/<color>
  - Delete: curl -i -X DELETE localhost/dog/<id>

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`
