# Memorization App
[![Actions Status](https://github.com/dolong2110/memorization-apps/workflows/Build%20and%20Test/badge.svg)](https://github.com/dolong2110/memorization-apps/actions)
[![CI](https://github.com/dolong2110/memorization-apps/workflows/Continuous-Integration/badge.svg)](https://github.com/dolong2110/memorization-apps/actions?query=workflow%3CI)
[![codecov](https://codecov.io/gh/dolong2110/memorization-apps/branch/master/graph/badge.svg?token=9262a659-d559-4fe9-acbf-959af9a6c8fa)](https://codecov.io/gh/dolong2110/memorization-apps)
[![Go Report Card](https://goreportcard.com/badge/github.com/dolong2110/memorization-apps/account)](https://goreportcard.com/report/github.com/dolong2110/memorization-apps/account)

## Application Overview

A chart of the tools and applications used is given below.

![App Overview](pictures/application_overview.png)

## Use Makefile to generate rsa256 keys

````
make create-keypair ENV=test
````

## Using Docker

each time change the code we should re-initialize the docker again at the root.

````
docker-compose up
````

can run a container that does not depend on other

````
docker-compose up postgres-account
````

## Migrate DB

````
make migrate-create NAME=add_users_table
make migrate-up // update table
make migrate-down // revert table
````