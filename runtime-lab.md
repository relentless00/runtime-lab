# Runtime Lab

## Overview

This project demonstrates the setup, configuration, and testing of modern JavaScript runtimes using Node.js and Bun within a TurboRepo monorepo environment. The purpose of this lab is to understand runtime environments, dependency management, security scanning, and version control using Git and GitHub.

---

## Project Structure

The project was organized using TurboRepo to manage multiple runtime applications in a single repository. The structure includes separate applications for Node.js and Bun runtimes.

Example structure:

my-turborepo/
├── apps/
│ ├── hello-node/
│ │ └── hello.js
│ ├── hello-bun/
│ │ └── hello.js
├── packages/
├── package.json
├── turbo.json
├── package-lock.json
└── runtime-lab.md

This structure allows modular and scalable application development.

---

## Runtime Installation and Verification

Both Node.js and Bun were installed and verified successfully.

Commands used:

```bash
node -v
bun -v