# daux-gen

[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/grahamrb/daux-gen/master/LICENSE) [![Docker Automated Build](https://img.shields.io/badge/docker-automated-blue.svg)](https://hub.docker.com/r/grahamrb/daux-gen/)

Simple Docker image to generate documentation from Markdown using the [DAUX.io](http://daux.io) documentation generation application. Documentation is written in Markdown.

Using this docker image is straightforward, two volumes are passed to the container, the source Markdown documents need to be mounted at `/var/docs` and the location the static html files should be output to is mounted to `/var/static`. 

```
docker run -v /user/grahamrb/my-markdown-docs:/var/docs -v /user/grahamrb/my-generated-docs:/var/static grahamrb/daux-gen
```

In the above example the markdown documentation is located at `/user/grahamrb/my-markdown-docs`, when the above command is exected static html documentation will be created in `/user/grahamrb/my-generated-docs`.

See the [Daux.io Getting Started](http://daux.io/Getting_Started) documentation for more information on how to write documents to be generated.

Docker image is located here: https://hub.docker.com/r/grahamrb/daux-gen/