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
      summary: Search Repositories
      description: Searches across repositories.
      operationId: searchRepositories
      x-api-path-slug: searchrepositories-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: order
        description: The sort field
      - in: query
        name: q
        description: The search terms
        default: React
      - in: query
        name: sort
        description: If not provided, results are sorted by best match
      responses:
        200:
          description: OK
      tags:
      - Search
      - Repositories
---
