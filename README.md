# MuShop Storefront

Responsive eCommerce storefront single page application built on microservices
architecture.

- Built using [UIkit](https://getuikit.com)

## Overview

### Technologies

The project leverages:

- [UIkit](https://getuikit.com) UI components
- [axios](https://www.npmjs.com/package/axios) Http client
- [core-js](https://www.npmjs.com/package/core-js) ESNext features
- [Pug](https://pugjs.org)
- [Less](http://lesscss.org)
- [Gulp](https://gulpjs.com)

## Quick start

### Dependencies

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Version</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="https://docker.com">Docker</a></td>
      <td>>= 1.12</td>
    </tr>
    <tr>
      <td><a href="http://www.gnu.org/s/make">Make</a></td>
      <td>>= 3.81</td>
    </tr>
  </tbody>
</table>

### Local

```shell
# start dependent microservices
make services

# start storefront
npm install
npm start
```

### Docker

```shell
# start storefront and all service layers
make up
```

### Shutdown

```shell
# stop all services
make down
```

## Build

Standard build

```shell
docker build -t mushop/storefront .
```

The storefront also supports **BETA** build option where an override to the
service semver can be provided as a build argument. When the supplied version
matches `/beta/i`, a banner is shown in the storefront UI. This is used for the
purpose of demonstrating service mesh

```shell
docker build --build-arg version=2.x-beta -t mushop/storefront .
```

## Credits

- Storefront based on templates by [Roman Chekurov](https://github.com/chekromul/uikit-ecommerce-template)

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.
