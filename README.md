# errors

[![Source Code](https://img.shields.io/badge/github-source%20code-blue?logo=github&logoColor=white)](https://github.com/rolehippie/errors) [![Testing Build](https://github.com/rolehippie/errors/workflows/testing/badge.svg)](https://github.com/rolehippie/errors/actions?query=workflow%3Atesting) [![Readme Build](https://github.com/rolehippie/errors/workflows/readme/badge.svg)](https://github.com/rolehippie/errors/actions?query=workflow%3Areadme) [![Galaxy Build](https://github.com/rolehippie/errors/workflows/galaxy/badge.svg)](https://github.com/rolehippie/errors/actions?query=workflow%3Agalaxy) [![License: Apache-2.0](https://img.shields.io/github/license/rolehippie/errors)](https://github.com/rolehippie/errors/blob/master/LICENSE)

Ansible role to install a templateable HTTP errors service

## Sponsor

Building and improving this Ansible role have been sponsored by my current and previous employers like **[Cloudpunks GmbH](https://cloudpunks.de)** and **[Proact Deutschland GmbH](https://www.proact.eu)**.

## Table of content

- [Default Variables](#default-variables)
  - [errors_cert_resolver](#errors_cert_resolver)
  - [errors_image](#errors_image)
  - [errors_insecure_middlewares](#errors_insecure_middlewares)
  - [errors_network](#errors_network)
  - [errors_priority](#errors_priority)
  - [errors_publish_server](#errors_publish_server)
  - [errors_secure_middlewares](#errors_secure_middlewares)
- [Discovered Tags](#discovered-tags)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### errors_cert_resolver

Cert resolver within traefik

#### Default value

```YAML
errors_cert_resolver:
```

#### Example usage

```YAML
errors_cert_resolver: default
```

### errors_image

Docker image to use

#### Default value

```YAML
errors_image: tboerger/errors:latest
```

### errors_insecure_middlewares

Insecure middlewares for traefik

#### Default value

```YAML
errors_insecure_middlewares:
  - https@file
  - errors@file
```

### errors_network

Docker network to connect to

#### Default value

```YAML
errors_network:
```

#### Example usage

```YAML
errors_network: traefik
```

### errors_priority

Priority within Traefik routing

#### Default value

```YAML
errors_priority: '1'
```

### errors_publish_server

Publish the service on that binding

#### Default value

```YAML
errors_publish_server:
```

### errors_secure_middlewares

Secure middlewares for traefik

#### Default value

```YAML
errors_secure_middlewares:
  - secure@file
  - errors@file
```

## Discovered Tags

**_errors_**


## Dependencies

- [rolehippie.docker](https://github.com/rolehippie/docker)
- [rolehippie.traefik](https://github.com/rolehippie/traefik)

## License

Apache-2.0

## Author

[Thomas Boerger](https://github.com/tboerger)
