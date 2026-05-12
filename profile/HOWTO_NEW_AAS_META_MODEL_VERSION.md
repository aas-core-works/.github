# How To Release for a New AAS Meta-model Version

This document describes the steps to undertake when a new meta-model version of the Asset Administration Shell (AAS) is released.
Each step corresponds to a repository in the [aas-core-works] GitHub organization.

[aas-core-works]: https://github.com/aas-core-works

## Formalize the Meta-model

The formalized meta-models live in [aas-core-meta].
Write a new meta-model corresponding to the specification book.

[aas-core-meta]: https://github.com/aas-core-works/aas-core-meta

A smoke-test transpilation runs as part of the continuous integration on [aas-core-meta], but make sure to also extend the test suite where necessary.
For example, see [test_v3_1.py] for the tests written for V3.1.

[test_v3_1.py]: https://github.com/aas-core-works/aas-core-meta/blob/main/dev/tests/test_v3_1.py

## Generation of Test Data

The repository [aas-core-testdatagen] holds all the test data for the different AAS meta-model versions.
The test data is sampled (fuzzed) using the code in the same repository, and published automatically *via* a GitHub workflow upon each new release.

[aas-core-testdatagen]: https://github.com/aas-core-works/aas-core-testdatagen

For a new version, download your formalized AAS meta-model from [aas-core-meta],
re-generate the test data, and verify that everything works by running
[update_all.py][testdatagen-update_all] (see the script for details).

[testdatagen-update_all]: https://github.com/aas-core-works/aas-core-testdatagen/blob/main/dev/dev_scripts/update_all.py

Once everything runs correctly and the changes are committed, release a new version of
[aas-core-testdatagen].
The test data will then be automatically published under [Releases][testdatagen-releases].

[testdatagen-releases]: https://github.com/aas-core-works/aas-core-testdatagen/releases

## JSON and XSD Schemas

Generate the JSON and XSD schemas using [aas-core-codegen] and send them to IDTA.
They will upload the schemas to the [aas-specs-metamodel] repository.

Right now, we do not have a dedicated repository where implementation-specific snippets for the schemas are kept -- this was the responsability of the schema maintainer (RWTH Aachen previously, and IDTA at the moment).

[aas-core-codegen]: https://github.com/aas-core-works/aas-core-codegen
[aas-specs-metamodel]: https://github.com/admin-shell-io/aas-specs-metamodel

## Language SDKs

Create an individual repository for the new SDK.

Copy, paste, and adapt the development scripts from the repository of the previous version.
For example, see the development scripts for the Golang V3.1 SDK in [_dev_scripts/].

[_dev_scripts/]: https://github.com/aas-core-works/aas-core3.1-golang/blob/main/_dev_scripts/

Copy, paste, and adapt the project specification (version, URL to the repository, *etc.*).

Generate the code using the development scripts you have just adapted.
This is typically done *via* [update_all.py][golang-update_all].

[golang-update_all]: https://github.com/aas-core-works/aas-core3.1-golang/blob/main/_dev_scripts/update_all.py

Release the language SDK using the language-specific release procedure (publish to npm.js, PyPI, *etc.*).

## Best Practices

### Local Development Workflow

Getting the meta-model formalized correctly is harder than one might expect.
The invariants (*i.e.*, constraints) are particularly difficult to get right.
We typically use a ping-pong development approach where the local copy of [aas-core-meta] is linked to [aas-core-testdatagen] as well as one or two language-specific SDK repositories.
For example, you can use soft or hard links in your filesystem so that changes in your local [aas-core-meta] repository are immediately visible in [aas-core-testdatagen] and in your local language-specific SDK repositories.

### Release Candidates

Errors are inevitable in practice.
While we have tried hard to introduce as many guard-rails and early-failure verifications as possible, errors are still commonly discovered only once the SDKs are released and tested in real production systems.

To avoid awkward situations where one patch version follows another in quick succession, it is best to release Release Candidate (RC) versions first and distribute them to a select few interested users.
Only once you receive confirmation that everything works correctly should you publish a proper release.
