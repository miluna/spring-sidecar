# Spring Sidecar Project
Project using Netflix Sidecar with Spring boot

It's important to note that Sidecar requires the NodeJs/Python/whatever server port included in the application.yml in order to work and register the service properly within Zuul. It is advised to set the homepage and also the health uri.

## application.yml
```yml
server:
  port: 5678

sidecar:
  port: 3000
  home-page-uri: http://localhost:${sidecar.port}/welcome
  health-uri: http://localhost:${sidecar.port}/health
  ```
