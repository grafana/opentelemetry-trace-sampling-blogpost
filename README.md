# opentelemetry-trace-sampling-blogpost
This is a repository which acts as a companion to the Grafana blog post on Grafana Agent's tail sampling functionality. Please see that blog post for details on using this repository.

The repository includes:
* A simple application that mimics a service receiving and responding to API requests, which sends logs directly to a local Loki instance.
* A configuration for Grafana Agent that receives traces in OTLP format and sends them to a local Tempo instance.
* Two pre-provisioned data sources for Grafana.
* A Docker Compose file used to stand up a local demonstration environment, comprised of:
  * Demo application
  * Grafana Agent
  * Grafana
  * Tempo
  * Loki

## Running

Ensure you have both Docker and Docker Compose installed, and then in a terminal simply run:
```bash
docker-compose up
```
This will stand up all the required components and allow you to login to the local Grafana instance at [http://localhost:3000/](http://localhost:3000/).

If you already have something running on port 3000, ensure that you change the relevant port in the `docker-compose.yml` file first to a free port.
