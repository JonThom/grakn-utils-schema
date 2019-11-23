# Grakn utils: schema development toolkit
utility toolkit for developing a grakn schema.

## Overview

What problem does this toolkit solve? Existing ontology languages like OWL have dedicated tools such as Protege that reduce the pain of building an ontology by letting the developer 
* include metadata such as definitions, elucidations, examples, references, revision history
* visualise the ontology as a graph 
* export the ontology to different formats
Grakn provides WorkBase but this doesn't meet the above requirements:
* no elegant way to attach metadata to a schema
* schema visualisation has limited user control and the layout currently doesn't work for larger schemas
* no way to the keyspace as a schema to gql or another format.
This toolkit provides an environment for developing a grakn schema. It uses a 'meta-schema' as a keyspace in which the developer models the new schema as a grakn dataset. The developer writes the new schema as a series of `graql` `insert` statements. To visualise the schema, the developer inspects the ontology using the `WorkBase` data visualiser. When the new schema is done, it is compiled to a series of `define` statements, i.e. the standard grakn schema form.

## Example

Inspect the `schema_meta.gql` file to understand how it models classes and their `relations` (e.g. class inheritance).
<example>.gql contains a simple schema in 'insert' data form. Use this as a template.
To compile the schema into a set of 'define' statements do
`<run compile script>`


