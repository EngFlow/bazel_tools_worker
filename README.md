# Bazel Worker Tools for JVM based Rules

This repository exports common tools for rule sets that use a jvm based runtime (java, kotlin, android, etc.)
from the Bazel repository.

## Motivation
Bazel requires rules to manage their own worker implementation for action execution. This results in
code duplication and increased maintenance for every rule set wishing to provide non-trivial action
execution.

Luckily, Bazel includes a fully featured base worker implementation that runs in the JVM. As part of an 
effort to standardize and reduce rule set maintenance, the `bazel_tools_worker` repository exports a
full "deploy" jar of the worker implementation.

[Guidance from the Bazel team](https://github.com/bazelbuild/bazel/issues/19544) is for community
supported tooling on for these resources.

## Release Cadence
Unless there are immediate bugfixes or necessary patches to the worker code, a release will be cut 
on major bazel version increments.

## Patches And Support
Please direct any patches/bugfixes to the [official Bazel repository](https://github.com/bazlebuild/bazel).
EngFlow current maintains this repository as a strict subset of the Bazel source tree.