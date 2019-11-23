# Grakn utils: schema development toolkit
utility toolkit for developing a grakn schema.

## Why

Existing ontology languages like OWL have dedicated tools such as Protege that reduce the pain of building an ontology by letting the developer 
* include metadata such as definitions, elucidations, examples, references, revision history
* visualise the ontology as a graph 
* export the ontology to different formats

With Grakn there are two ways to develop a schema: writing a series of 'define' statements in a gql file or using the WorkBase GUI. Both fall short of the above requirements.

## How 

This toolkit uses Grakn as an environment for developing a Grakn schema. 

Specifically, the developer encodes the new schema classes as instances of classes of a 'meta-schema' through a script of `graql` `insert` statements. 

The developer visualises the ontology using the `WorkBase` data visualiser, enabling far more flexible queries and click-based interaction than the built-in schema visualiser.  

When the developer has written the schema in 'insert' form, the parser script compiles it to a series of `define` statements - the standard grakn schema format.

## Example

Inspect the `schema_meta.gql` file to understand how it models classes and their `relations` (e.g. class inheritance).
<example>.gql contains a simple schema in 'insert' data form. Use this as a template.
To compile the schema into a set of 'define' statements do
`<run compile script>`

## Questions and answers

* Why not just add schema metadata as attributes within the schema? 
	* It would be inappropriate for each data instance to include attributes with metadata about its ontology class as instances will already have attributes with instance metadata.
