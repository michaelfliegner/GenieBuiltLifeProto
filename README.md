# What is it?

This is initial scaffolding for a 
* reactive Webapp for Life Insurance Contracts
* sporting bitemporal data management and
* pluggable product data

It is built with GenieBuilder, which at the moment cannot be used in GITPOD. But the app can be run as shown below.
To run it under GenieBuilder You have to use a non-cloud computer. This app is not runnable in Genie Cloud, as it builds on postgres
and cannot be run with mysql.

## MVVM Architecture 
This app leverages the great [Genie Framework](https://genieframework.com/)
### Transactions

Transaction data are persistent. 

Transactions are started 
* implicitly on creation of entities
* explicitly on existing entities

Once a transaction is open
* mutations can be savepointed.
* mutations can be persisted, Persising deletes prior savepoints and makes the persisted state a savepoint.
* it can be 
    * committed - provided data integrity rules are complied.
    * rolled back.


# Getting ready

after firing up the workspace do the following (not yet done automatically):

## Starting the web server

- on julia command line enter:
- include("app.jl")
- using GenieFramework
- Server.up()
- and then You open the ports view clicking Ports at the lower right corner of the editor window and open the browser

BE PATIENT! Intialization takes some time. It gets reactive then!

Three contracts are preloaded: pension, SingleLifeRisk, JointLifeRisk