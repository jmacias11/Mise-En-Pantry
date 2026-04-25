# Choose Authentication Service

## Status

Initial ADR

## Context

Users will be required to create accounts in order to manage their subscriptions and have their data sync across devices. Therefore a third party authentication service will be utilized for maximum security regarding people's accounts and passwords.

## Decision

I am not too familiar with the options available to me, but after some brief research, the choice I'm making will be Firebase. I have some experience with Firebase from nearly a decade ago, but it provides a very generous free tier, and is powered by Google. Meaning it should have good integration with the other Google services I am using.

## Consequences

A large negative consequence at this point is that I am becoming heavily reliant on the Google Ecosystem. This can be a downside if they decide to raise prices or terminate certain services. I should make sure to make the design modular such that services can be easily swapped out if needed.