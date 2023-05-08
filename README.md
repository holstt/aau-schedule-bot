
> :warning: Currently, this repo serves as documentation. Code will follow eventually :-) 

# Aau Schedule Scraping
![dotnet](https://img.shields.io/badge/asp--net--core-3.1-blue)
![csharp](https://img.shields.io/badge/C%23-8-blue)
![ide](https://img.shields.io/badge/IDE-vs2019-blue)

Scrapes schedules from Aalborg University (AAU) and notifies subscribers of any changes. 

The schedules are stored in a Postgres database and can be retrieved through its' REST API.

## About

The scraper is part of the [DiscordBot](https://github.com/roedebaron/DiscordBot) microservice architecture. 

> TODO: 
> - Describe layers

## Getting Started

It is possible to run the application independently of the other services in the microservice architecture (except the postgres database), however, the scraper is currently set up to call the endpoint of the DiscordBot when any changes occur. Simply replace the URL in order to integrate with your own service. 

Either run the project natively or use the provided Dockerfile to run it in Docker.

Clone the project: 
1. `git clone https://github.com/roedebaron/aau-schedule-scraping.git`
2. `cd aau-schedule-scraping/AauScheduleScraping.Api`

#### Native
3. Run `dotnet run`. This will automatically download all dependencies, build the project and then run the service. 
4. If no other port has been specified in the configuration, the service is now running on port 5000. 

#### Using Docker 🐳
3. Run `docker build -t aau-schedule-scraping .` to build the image with name `drive-service`
4. Run `docker run -dp 5000:5000 aau-schedule-scraping ` to start a container from the image. This will map your local port (e.g. 5000) to the port that the service is listening on (default is 5000). 

> TODO: 
> - Setting own config/env values. db, webhook url etc
> - Native + Docker command
 
## Usage 

> TODO:
> - Request schedule endpoint
> - Callback request format (when changes are detected)
> - Insert screenshot, demo gif, code examples... 
> - Swagger endpoint

## Project TODO
- [ ] Push code to repo
- [ ] Migrate to .NET 5
- [ ] Consider seperating in background service and REST API. Or use Hangfire? 
