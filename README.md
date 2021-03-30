# AauScheduleScraping
![dotnet](https://img.shields.io/badge/asp--net--core-3.1-blue)

Scrapes schedules from Aalborg University (AAU) and notifies subscribers of any changes. 

The schedules are stored in a Postgres database and can be retrieved through its' REST API.

## About

The scraper is part of the [DiscordBot](https://github.com/roedebaron/DiscordBot) microservice architecture. 

> TODO: 
> - Describe layers

## Getting Started

It is possible to run the application independently of the other services in the microservice architecture (except the postgres database), however, the scraper is currently set up to call the endpoint of the DiscordBot when any changes occur. Simply replace the URL in order to integrate with your own service. 

Either run the project natively or use the provided Dockerfile.

> TODO: 
> - Setting own config/env values. db etc
> - Native + Docker command
 
## Usage 

> TODO:
> - Insert screenshot, demo gif, code examples... 

## Project TODO
- [ ] Push code to repo
- [ ] Migrate to .NET 5
