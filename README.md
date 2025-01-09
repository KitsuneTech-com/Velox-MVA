# Velox MVA Framework

## Introduction to Velox
The Velox MVA framework is built to serve as a streamlined client/server data retrieval and communication platform for
websites and progressive web apps. This framework is divided into three primary components: Velox Server, Velox API,
and Velox Client. Each of these controls a different aspect of the data flow between a data source and front-end client;
by themselves, each component simplifies the data flow within its scope, but when used together they bridge the gap
between client and server in such a way that the developer using them needs not think about data formatting and protocols
over the wire and needs only use the methods of the component they're working with.

## Overview of Components
The following is a brief summary of each Velox component. For more details, including how to install and use each
component, or to create or view issues for the component in question, click on the component's title to visit the
appropriate repository.

### [Velox Server](https://github.com/KitsuneTech-com/Velox-Server)
Velox Server is a PHP library that abstracts away the various database drivers and libraries and presents a
platform-agnostic interface by which tocommunicate with any of the supported database engines without having to know the
differences between the functions used for each engine. It can also be used to facilitate ETL operations or even perform
joins between disparate databases, and to easily export queried data in several common formats.

### [Velox API](https://github.com/KitsuneTech-com/Velox-API)
Velox API is built on top of Velox Server, and provides a standard JSON-formatted interface for making web-based queries
against Velox "query definition" files. By using Velox Server as an intermediary, the client need not know the specific
details of the underlying schema, but can still perform complex SQL-equivalent operations (SELECT, INSERT, UPDATE, DELETE)
as permitted by the query definition. This allows for robust client-server interactions with a minimum of coding, yet with
a server-side translation layer that automatically sanitizes input and inhibits injection and other malicious actions.

### [Velox Client](https://github.com/KitsuneTech-com/Velox-Client)
Velox Client is a JavaScript/ECMAScript library that provides classes that facilitate communication with Velox API
endpoints, building and sending requests and receiving and parsing the responses. This eliminates the need to build Fetch
API or XMLHttpRequest calls directly; these are built into and invoked by the Velox Client classes themselves. Used in
combination with Velox API and Velox Server, queries to the underlying data source can be handled simplyby writing a short
query definition on the backend, and a JavaScript routine on the front end referencing the endpoint created.

## Licensing
Velox and its components are released under the Mozilla Public License 2.0. This license allows the free and unrestricted
use of any or all of the components described here, with certain conditions if the code is modified and redistributed. See
[here](https://www.mozilla.org/en-US/MPL/2.0/) for more details.
