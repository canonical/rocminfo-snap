# Preface

This repository packages the upstream [ROCmInfo](https://github.com/ROCm/rocm-systems/tree/develop/projects/rocminfo) as a strict-mode snap. The content in this file and directory is relevant only to tasks about building, packaging, releasing, or maintaining this snap, and to this repository's CI, documentation, and knowledge base. It is not relevant to changes in the upstream ROCmInfo source code.

Read the top-level `.kb/agents.md` file before continuing below.

# Overview

Snap packaging of the upstream ROCmInfo, a system information and GPU enumerator tool. It ships a single strict-mode snap (`rocminfo`) built from the upstream git tag via snapcraft.

# Architecture

The snap is built from a single cmake part that fetches the upstream ROCmInfo source at the `therock-${SNAPCRAFT_PROJECT_VERSION}` git tag and installs it under `/opt/rocminfo` inside the snap. The ROCm libraries are pulled in from the `rocm-inference` content snap.

# Directory

- `.kb/` - Agent knowledge base (see Documents).
- `.pre-commit-config.yaml` - Pre-commit hooks.
- `AGENTS.md` - This file; top-level agent guidance.
- `CONTRIBUTING.md` - Prerequisites and contribution instructions.
- `README.md` - Project introduction and install/usage pointers.
- `snap/` - Snapcraft source directory; contains the full snap definition.

# Documents

- `.kb/agents.md` - General rules for the knowledge base reading and writing.
