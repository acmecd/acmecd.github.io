---
title: On Premise Service Docs
tags: 
 - ACME-oPS
 - docker
description: OPS info
---

# ACME-oPS

{% include alert.html type="info" title="Content" content="How to work with it and what it offers." %}

## How do I work with it?

- The ACME on premise service (ACME-oPS) is distributed by ACME Corp as a [Docker container via Docker Hub](linktothecontainer). 
- To learn how to deploy the container, see the [How to Deploy](deploy) page.<br>
- Once deployed, the service is to be updated manually by the User, see the [How to Update](update) page.<br>

## What can it do?

Main functionality:
- Parses the call, extracts the payload structure
- From individual fields and groups of fields, constructs / suggests high level objects of different types (subtypes). For example:<br>
    - person (name, address, phone number etc)
    - goods of various types (apples / oranges etc)
    - agreement (type, objective, conditions etc)
    - order (client — essentially a person, goods, amounts, prices etc)
- For this, the ACME-oPS executes custom-made algorithms based on pattern matching, machine learning and rules configurable by the Customer

## What do I need it for?

Integration purposes:

- [For data taxonomy / map building](datamap)<br>
    The recommended integration option is that ACME-oPS is called by some composite service which in turn acts as a proxy for inter-company traffic. This composite service should use the universal ACME-oPS ingestion API, wrapping the
initial request into the standardized format.

>ACME provides **hints** as to which services act as actual master data sources, what information should be included in the combined "golden" record if there are several services involved.

- [For the extended master data management option](masterds)<br>
    The ACME-oPS should be called directly by interested services through relevant APIs 

>ACME provides and keeps **"golden" records** with verified and cleaned data to all services.

## How can it be integrated?

Technical integration options:
- [Protocols](protocols): direct HTTP, gRPC, Kafka, RabbitMQ
- [Formats / content types](formats): JSON and XML

