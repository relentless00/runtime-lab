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
    node -v
    bun -v


Both runtimes responded correctly, confirming proper installation and functionality.

## Application Testing

Two simple applications were created:

### Node.js Application

    File:
        apps/hello-node/hello.js

    Example code:
        console.log("Hello from Node.js runtime");


    Executed using:
        node hello.js


### Bun Application

    File:
        apps/hello-bun/hello.js

    Example code:
        console.log("Hello from Bun runtime");


    Executed using:
        bun run hello.js

Both applications executed successfully without errors.


## Security Testing

Security testing was performed using both npm audit and Snyk CLI.

### npm audit

    Command used:
        npm audit

    Result:
    npm audit reported vulnerabilities related to development dependencies such as ESLint and minimatch. These vulnerabilities are associated with development tools and do not directly affect the runtime execution of the application.


### Snyk CLI

    Commands used:
        snyk auth
        snyk test --all-projects

    Result:
    Snyk successfully scanned the project and reported:
    No vulnerable paths found
    This confirms that there are no exploitable security vulnerabilities affecting the application runtime.



## Runtime Comparison: Node.js vs Bun

### Node.js

    Advantages:
        Mature and stable runtime
        Large ecosystem and community support
        Widely used in production environments
        Strong support for real-time applications using WebSockets

    Disadvantages:
        Slower package installation compared to Bun


### Bun

    Advantages:
        Faster startup and execution
        Built-in package manager
        Modern runtime with improved performance

    Disadvantages:
        Smaller ecosystem
        Less mature compared to Node.js
        Limited production adoption


## Runtime Recommendation for Real-Time Chat Application

For a real-time chat application, Node.js is the recommended runtime environment. Node.js uses a non-blocking, event-driven architecture, which makes it efficient for handling multiple simultaneous connections. It has strong support for WebSockets and real-time communication libraries such as Socket.IO.

Although Bun offers better performance, Node.js is currently the better choice due to its stability, mature ecosystem, and proven reliability in production environments.