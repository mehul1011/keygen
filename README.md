# KeyGen


Hi, this is an Angular 12 Example Project, which can be used as a frontend for
password manager when paired with a simple key-value backend
[KeyGen-API](https://github.com/mehul1011/keygen-api).

Its **main purpose** is to help learning different aspects of frontend development
using Angular 12, such as authentication, routing, unit testing, etc.

It's not a tutorial but rather a compilation of different ideas/components
I've found over the Internet which were incorporated into one project.

The **secondary goal** was to build free open source password manager which I
will use in everyday life and which can be deployed by anyone in minutes. It was
inspired by [keymemo](https://www.keymemo.com/) and
[padlock](https://github.com/MaKleSoft/padlock) and leverages the same idea of
master password which never leaves your computer because we decrypt/encrypt everything in 
browser and send already encrypted data to the server.

## Getting Started

### Prerequisites

Since this project is written using the latest Angular 12 it has the same
prerequisites as the Angular 12 itself (Angular-CLI in particular):
Node 12 or higher, together with NPM 6 or higher.

> Install [Node.js® and npm](https://nodejs.org/en/download/) if they are not
 already on your machine.

### Installation

```bash
git clone git@github.com:mehul1011/keygen.git
cd keygen
```

Install all dependencies

```bash
npm ci
```

You may also [check that tests are green](#running-the-tests) after installation

### Docker

Every project should have [Dockerfile](Dockerfile) nowadays, so we have it as well.
As you can see it's built on top of `node:latest` and installs [nginx](https://nginx.org/)
web-server which listens on 80 port. We use [nginx-default.conf](nginx-default.conf)
configuration file, which has a simple rule to serve our SPA (check
[Angular Docs](https://angular.io/guide/deployment#production-servers))

You can pull pre-built container using `maprox/keyholder-angular:latest` image
which is hosted on [Docker Hub](https://hub.docker.com/r/maprox/keyholder-angular/).

## Running the tests

This project does not have any e2e tests yet,
so running tests is as simple as running standard

```bash
ng test
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

