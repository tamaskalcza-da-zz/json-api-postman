# Postman for the JSON API

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [User Guide](#user-guide)
  - [Importing](#importing)
  - [Variables](#variables)
    - [`ledgerId` and `applicationId`](#ledgerid-and-applicationid)
    - [`jwtToken` and `usedTokenValues`](#jwttoken-and-usedtokenvalues)

## Overview

This repository contains a simple Postman collection that can be used with the DAML JSON API.

The collection is also capable of basic authentication using JWT tokens.

## Prerequisites

Install [Postman](https://www.postman.com/downloads/) appropriate for your platform.

## User Guide

### Importing

The [json_api.postman_collection.json](json_api.postman_collection.json) is the actual Postman API collection. It contains the most used endpoints of the JSON API.

The collection is configured using environment variables. For that import the [json_api.postman_environment.json](json_api.postman_environment.json).

### Variables

| Variable        | Default Value         | Description                                |
| --------------- | --------------------- | ------------------------------------------ |
| jsonApiHost     | localhost             | Host of the JSON API.                      |
| jsonApiPort     | 7575                  | Port of the JSON API.                      |
| ledgerId        | postman               | The ledger ID.                             |
| applicationId   | HTTP-JSON-API-Gateway | The application ID.                        |
| party           |                       | Name of the party who issues the requests. |
| secret          | secret                | The JWT token secret.                      |
| logEnabled      | false                 | Enables script logs in Postman console.    |
| jwtToken        |                       | **NOT** for users.                         |
| usedTokenValues |                       | **NOT** for users.                         |

#### `ledgerId` and `applicationId`
Either configure the ledger or set these values appropriately.

#### `jwtToken` and `usedTokenValues`
Not meant for end users. The script that handles the JWT token uses these for optimization.
