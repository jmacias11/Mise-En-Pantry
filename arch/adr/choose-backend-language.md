# Choosing the Backend Language

## Status

Initial ADR

## Context

The language will access a postgresql database server in the backend as well as handle requests on a hosted webserver. Since there is a significant of data retrieval at times, the language should be somewhat performant, but more importantly not too complex such that development is more complicated than it needs to be. This effectively rules out a language such as C++ since it is very performant, but quite complicated for the use-case.

## Decision

I am deciding between Python3 or NodeJS. I am extremely proficient in Python3, however after some research, I have become aware that NodeJS would perform better in this use case and has better library and documentation for web development applications. Therefore I will be using NodeJS as the backend.

## Consequences

I need to determine what web server library, postgressql interface I will use, as well as my options for using LLMs and other APIs.
