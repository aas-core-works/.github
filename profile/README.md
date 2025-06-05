# aas-core-works

We provide software tools and libraries to enable others to work with Asset Administration Shells (AAS).

Our main focus is on robust and correct **software building blocks**, which are then used to build greater stuff.

## Quickstart

* [aas-core-meta]: formalized meta-models
  * [Meta-models rendered as HTML] 
* [aas-core-codegen]: tool and library to generate code, schemas, *etc.*
* Schemas and definitions
  * [aas-core-protobuf]
  * [aas-core-opcua]
* SDKs
  * V3
    * [aas-core3.0-csharp]
    * [aas-core3.0-golang]
    * [aas-core3.0-python]
    * [aas-core3.0-micropython]
    * [aas-core3.0-typescript]
    * [aas-core3.0-cpp]
    * [aas-core3.0-java]
  * V3RC02
    * [aas-core3.0rc02-csharp]
    * [aas-core3.0rc02-python]
    * [aas-core3.0rc02-typescript]
* SDK extensions
  * [aas-core3.0-python-protobuf]
* Package libraries
  * [aas-package3-csharp]
* React editor
  * [aas-core3.0rc02-react-editor]
* Command-line Toolkit
  * [aas-core3.0-cli-swiss-knife]
* Test data
  * [aas-core3.0rc02-testgen]
  * [aas-core3.0-testgen]
* [Contributing Institutions](#contributing-institutions)

[aas-core-meta]: https://github.com/aas-core-works/aas-core-meta
[Meta-models rendered as HTML]: https://aas-core-works.github.io/aas-core-meta/
[aas-core-codegen]: https://github.com/aas-core-works/aas-core-codegen

[aas-core-protobuf]: https://github.com/aas-core-works/aas-core-protobuf
[aas-core-opcua]: https://github.com/aas-core-works/aas-core-opcua

[aas-core3.0rc02-csharp]: https://github.com/aas-core-works/aas-core3.0rc02-csharp
[aas-core3.0rc02-python]: https://github.com/aas-core-works/aas-core3.0rc02-python
[aas-core3.0rc02-typescript]: https://github.com/aas-core-works/aas-core3.0rc02-typescript

[aas-core3.0-csharp]: https://github.com/aas-core-works/aas-core3.0-csharp
[aas-core3.0-golang]: https://github.com/aas-core-works/aas-core3.0-golang
[aas-core3.0-python]: https://github.com/aas-core-works/aas-core3.0-python
[aas-core3.0-micropython]: https://github.com/aas-core-works/aas-core3.0-micropython

[aas-core3.0-typescript]: https://github.com/aas-core-works/aas-core3.0-typescript
[aas-core3.0-cpp]: https://github.com/aas-core-works/aas-core3.0-cpp
[aas-core3.0-java]: https://github.com/aas-core-works/aas-core3.0-java

[aas-core3.0-python-protobuf]: https://github.com/aas-core-works/aas-core3.0-python-protobuf

[aas-package3-csharp]: https://github.com/aas-core-works/aas-package3-csharp

[aas-core3.0rc02-react-editor]: https://github.com/aas-core-works/aas-core3.0rc02-react-editor

[aas-core3.0-cli-swiss-knife]: https://github.com/aas-core-works/aas-core3.0-cli-swiss-knife

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
  * [aas-core3.0-golang]
  * [aas-core3.0-python]
  * [aas-core3.0-typescript]
  * [aas-core-3.0-cpp]
  * [aas-core-3.0-java]
* V3RC02
  * [aas-core3.0rc02-csharp]
  * [aas-core3.0rc02-python]
  * [aas-core3.0rc02-typescript]

## Building Block: Tools

We generate a GUI editor and a command-line toolkit to facilitate work with the static AAS data.
The command-line toolkit should help you get "80%" of the work done, while you finish the remaining "20%" using the GUI editor.

The tools aim for correctness, robustness and simplicity rather than feature-richness.

The GUI editor is available here: [aas-core3.0rc02-react-editor].

The command-line toolkit is available at: [aas-core3.0-cli-swiss-knife].

## Building Block: Test Data

We generate a large set of test cases based on the formalized meta-models.

We use the test data internally, mainly to test our tools and SDKs.
However, it is also provided to the wider community so that other people can easily test their platforms, editors, downstream libraries *etc.*

The test data for different versions of AAS meta-model are available here:

* [aas-core3.0rc02-testgen]
* [aas-core3.0-testgen]

## Contributing Organizations

All this work has been supported either directly, with contributions in ideas, text or code, or indirectly, *i.e.*, financially, through the following institutions:

[<img alt="ZHAW" src="https://github.com/aas-core-works/.github/assets/5072771/76d675a5-c6a7-43e7-b6ed-ca304238498d" width=100 />](https://www.zhaw.ch/en/engineering/institutes-centres/ims/)&nbsp;
[Zurich University of Applied Sciences - Institute of Mechatronic Systems (IMS)](https://www.zhaw.ch/en/engineering/institutes-centres/ims/)<br/><br/>

[<img alt="TU Dresden" src="https://github.com/aas-core-works/.github/assets/5072771/e2cfbb3f-581c-4b98-a0ea-81c617811c67" width=100 />](https://tu-dresden.de/ing/informatik/ai/professur-fuer-prozesskommunikation/)&nbsp;
[TU Dresden - Chair of Industrial Communications](https://tu-dresden.de/ing/informatik/ai/professur-fuer-prozesskommunikation/)<br/><br/>

[<img alt="RWTH Aachen" src="https://github.com/aas-core-works/.github/assets/5072771/4148dc68-f0c7-4df2-b495-e0bae0833ad1" width=100 />](https://www.iat.rwth-aachen.de/cms/~eety/iat/?lidx=1)&nbsp;
[RWTH Aachen - Chair of Information and Automation Systems for Process and Material Technology](https://www.iat.rwth-aachen.de/cms/~eety/iat/?lidx=1)<br/><br/>

[<img alt="IDTA" src="https://github.com/aas-core-works/.github/assets/5072771/bce7288d-3bac-40cc-aa05-c6136666fc3b" width=100/>](https://industrialdigitaltwin.org/)&nbsp;
[Industrial Digital Twin Association](https://industrialdigitaltwin.org/)

[<img alt="conplement AG" src="https://github.com/aas-core-works/.github/assets/5072771/276bfe63-3597-4d3f-914b-24d9f58dae9f" width=100/>](https://www.conplement.de/digital-twin)&nbsp;
[conplement AG](https://www.conplement.de/digital-twin)
