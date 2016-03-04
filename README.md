# angular-swagger-ui-material

![work: in progress](https://img.shields.io/badge/work-in%20progress-orange.svg?style=flat)

Material Design ~~template~~ Swagger UI ~~for~~ based on [angular-swagger-ui](https://github.com/Orange-OpenSource/angular-swagger-ui).

## Demo

*Chrome browser should work.*

### Main demos

| Demo  | Server | Notes |
| --- | --- | --- |
| [Pet Store](http://darosh.github.io/angular-swagger-ui-material) | [petstore.swagger.io](http://petstore.swagger.io) | Markdown in API info |
| [Hub](http://darosh.github.io/angular-swagger-ui-material/hub.html) | | powered by [APIs.guru](http://APIs.guru) |
| [Theming Demo](http://darosh.github.io/angular-swagger-ui-material/?primary=blue-grey&accent=grey&warn=pink) | [petstore.swagger.io](http://petstore.swagger.io) | *primary:* blue-grey, *accent:* grey, *warn:* pink |

### Development demos

| Demo  | Server | Notes |
| --- | --- | --- |
| [Uber](http://darosh.github.io/angular-swagger-ui-material/#?url=https://cdn.rawgit.com/OAI/OpenAPI-Specification/master/examples/v2.0/json/uber.json) | no | from [OpenAPI-Specification/examples](https://github.com/OAI/OpenAPI-Specification/blob/master/examples/v2.0/json/uber.json), Markdown in operation info |
| [LoopBack Drupal](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-drupal.json) | no | [Drupal](https://www.drupal.org/) database discovered + [LoopBack](http://loopback.io/) default models, <br> large: 900+ operations |
| [Minimal Swagger 2.0](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-minimal.json) | no | |
| [GiHub Flavored Markdown](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-gfm.json) | no | generated from [test/fixtures/markdown/README.md](https://github.com/darosh/angular-swagger-ui-material/blob/master/test/fixtures/markdown/README.md) |
| [Swashbuckle](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-swashbuckle.json) | no | generated by [Swashbuckle](https://github.com/domaindrivendev/Swashbuckle) |
| [Swashbuckle.OData](http://darosh.github.io/angular-swagger-ui-material/#?url=http://darosh.github.io/angular-swagger-ui-material/swagger-swashbuckle-odata.json) | no | example from [Swashbuckle.OData](https://github.com/rbeauchamp/Swashbuckle.OData) |
| [YAML](http://darosh.github.io/angular-swagger-ui-material/#?url=https://apis-guru.github.io/api-models/bbc.com/1.0.0/swagger.yaml) | no | example for [swagger-yaml.js](./src/plugins/before-load/yaml.js) module |

## Features

* [x] Compatible with [angular-swagger-ui](https://github.com/Orange-OpenSource/angular-swagger-ui) 0.3.0 (2016-02-22)
* [x] [Material Design](https://www.google.com/design/spec/material-design/introduction.html)
* [x] Responsible layout
* [x] Configurable [angular-material](https://material.angularjs.org) theme colors
* [x] Highlight deprecated methods
* [x] Render [GFM](https://help.github.com/articles/working-with-advanced-formatting/) descriptions
* [x] Download de-referenced standalone JSON or YAML
* [x] YAML Swagger format support
* [x] Standard HTTP *methods*, *status codes* and *headers* reference thanks to [know-your-http-well](https://github.com/for-GET/know-your-http-well)
* [x] Grouped and ungrouped views
* [x] Open response body in new window
* [x] Search

## Search

| Filter | Matches | Notes |
| --- | --- | --- |
| log | POST /user/login <br> POST /user/login| path |
| get | GET /user <br> GET /pet | method |
| ge | N/A | single word, not full method |
| get pet | GET /pet | method + path |
| de pet | DELETE /pet | method + path |

## Plugins

See [src/plugins](./src/plugins).

## Reference

* [angular-swagger-ui](https://github.com/Orange-OpenSource/angular-swagger-ui)
* [Swagger RESTful API documentation specification](http://swagger.io/specification/)
* [OpenAPI specification](https://github.com/OAI/OpenAPI-Specification)

## Development

**Install**

```shell
npm install -g bower gulp
bower install
npm install
```

**Rebuild** [http-data.js](./src/services/http-data.js)

```
gulp info
```

**Rebuild** [swagger-gfm.json](./test/fixtures/markdown/swagger-gfm.json)

```
gulp info
```

**Build dist**

```shell
gulp
```

**Build demo**

```shell
gulp demo
```

**Deploy demo**

```shell
gulp deploy
```

## TODOs

* [angular-swagger-ui-material](https://github.com/darosh/angular-swagger-ui-material/search?q=TODO&type=Code&utf8=%E2%9C%93)
* [ ] Alternative layout in "documentation" style
* [ ] Operation permalinks
* [ ] Scripts tab with examples
* [ ] Cross-browser compatibility (unknown)
* [ ] Optimization (one-time binding, &hellip;)
* [ ] Hot keys (search, submit)
* [ ] XML example support
* [ ] Swagger 1.2
* [ ] E2E tests
* [ ] [Security Requirement Object](http://swagger.io/specification/#securityRequirementObject) support
