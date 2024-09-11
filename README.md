# Syllabus

## Introduction

We will cover best practices when developing Node.js programs including API design, package definition, NPM interaction, test coverages and TypeScript. Each unit of the course is designed to complement each other in the building of a real-life application. We propose to build an API enabling to store and retrieve timeseries data with a complementary web UI. For example, the result could be used to collect system metrics from a cluster.

## Requirements

This course is requiring familiarity with the JavaScript language and general knowledges in Web technologies. Prior experience with server side environment such as Lamp is a plus. A reminder of basic web and UNIX knowledge will be done during first class.

## Outline

1.  Node.js
2.  Dependency management & ExpressJS framework
3.  Transpilation & embedded datastore with unit testing
4.  Middlewares & authentication
5.  Real-time communication with Socket.io & production considerations

## Bibliography/webography

No book is used nor required. Reliable information is gathered from wikis, GitHub, source codes and various blogs.

## About those presentations

Every presentation uses [reveal.js](https://github.com/hakimel/reveal.js/)

To export to pdf, use [decktape](https://github.com/astefanutti/decktape) :

```
git clone --depth 1 https://github.com/astefanutti/decktape.git
cd decktape
curl -L http://astefanutti.github.io/decktape/downloads/phantomjs-[platform] -o bin/phantomjs
chmod +x bin/phantomjs
./bin/phantomjs decktape.js generic --keycode=Space file://path/to/prez.html /path/to/dest.pdf
```
