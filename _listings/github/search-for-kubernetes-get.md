---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: GitHub Repository Search
  description: Allows for the streaming of GitHub searches.
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- https
produces:
- application/json
consumes:
- application/json
paths:
  /search/repositories:
    get:
      summary: Search for Kubernetes
      description: Searches for Kubernetes across repositories.
      operationId: searchRepositories
      x-api-path-slug: searchrepositories-get
      parameters:
      - in: query
        name: q
        description: The search terms
        default: Kubernetes
      responses:
        200:
          description: OK
      tags:
      - Search
      - Repositories
---
