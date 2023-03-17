# aas-core-works

We provide software tools and libraries to enable others to work with Asset Administration Shells (AAS).

Our main focus is on robust and correct **software building blocks**, which are then used to build greater stuff.

## Quickstart

* [aas-core-meta]: formalized meta-models
  * [Meta-models rendered as HTML] 
* [aas-core-codegen]: tool and library to generate code, schemas, *etc.*
* SDKs
  * V3
    * [aas-core3.0-csharp]
  * V3RC02
    * [aas-core3.0rc02-csharp]
    * [aas-core3.0rc02-python]
    * [aas-core3.0rc02-typescript]
* React editor
  * [aas-core3.0rc02-react-editor]
* Test data
  * [aas-core3.0rc02-testgen]
  * [aas-core3.0-testgen]

[aas-core-meta]: https://github.com/aas-core-works/aas-core-meta
[Meta-models rendered as HTML]: https://aas-core-works.github.io/aas-core-meta/
[aas-core-codegen]: https://github.com/aas-core-works/aas-core-codegen

[aas-core3.0rc02-csharp]: https://github.com/aas-core-works/aas-core3.0rc02-csharp
[aas-core3.0rc02-python]: https://github.com/aas-core-works/aas-core3.0rc02-python
[aas-core3.0rc02-typescript]: https://github.com/aas-core-works/aas-core3.0rc02-typescript

[aas-core3.0rc02-react-editor]: https://github.com/aas-core-works/aas-core3.0rc02-react-editor

[aas-core3.0rc02-testgen]: https://github.com/aas-core-works/aas-core3.0rc02-testgen
[aas-core3.0-testgen]: https://github.com/aas-core-works/aas-core3.0-testgen

## Building Block: Formalized Meta-models

We formalize different versions of AAS meta-models based on the publications by [Industrial Digital Twin Association] to a machine-readable form written in a subset of Python language.

[Industrial Digital Twin Association]: https://industrialdigitaltwin.org/

The formalized and machine-readable meta-models are available at: [aas-core-meta]

We continuously render the meta-models in HTML, which is available here: [Meta-models rendered as HTML] 

## Building Block: Generators

We develop different code and schema generators which take the formalized meta-model as input.

They operate on a single point of truth, the meta-model. 
This allows us to propagate any changes in the meta-models immediately and effortlessly to the generated libraries and schemas.

The project is available at: [aas-core-codegen].

The generators are usually used as command-line tools.
The project can also be used as a Python library, in case you want to develop your own generators.

## Building Block: SDKs

We maintain an array of Software Development Kits (SDKs) in different languages to de/serialize, verify and manipulate the AAS models.

Our goal is to provide well-tested, correct and robust SDKs which are easy to integrate into larger software projects.

The SDKs for different versions of AAS meta-model are available at:

* V3
  * [aas-core3.0-csharp]
* V3RC02
  * [aas-core3.0rc02-csharp]
  * [aas-core3.0rc02-python]
  * [aas-core3.0rc02-typescript]

## Building Block: Test Data

We generate a large set of test cases based on the formalized meta-models.

We use the test data internally, mainly to test our tools and SDKs.
However, it is also provided to the wider community so that other people can easily test their platforms, editors, downstream libraries *etc.*

The test data for different versions of AAS meta-model are available at:

* [aas-core3.0rc02-testgen]
* [aas-core3.0-testgen]
