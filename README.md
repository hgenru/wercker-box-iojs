# io.js wercker box

[![wercker status](https://app.wercker.com/status/dc9652b1c8b05dc5d487d0ad88a1dfb8/m "wercker status")](https://app.wercker.com/project/bykey/dc9652b1c8b05dc5d487d0ad88a1dfb8)

This [wercker](http://wercker.com) box installs [io.js](https://iojs.org) using [nvm](https://github.com/creationix/nvm).

### Installed io.js versions

* 1.3.x
* 1.4.x
* 1.5.x
* 1.6.x

## Basic Usage

```yaml
box: zhevron/iojs
build:
  steps:
    - npm-install
    - npm-test
```

## Advanced Usage (Use a different version)

```yaml
box: zhevron/iojs
build:
  steps:
    - script:
        name: Use io.js 1.5.x
        code: nvm use iojs-v1.5
    - npm-install
    - npm-test
```

## Advanced Usage (Install a different version)

```yaml
box: zhevron/iojs
build:
  steps:
    - script:
        name: Use io.js 1.0.x
        code: |
          nvm install iojs-v1.0
          nvm use iojs-v1.0
    - npm-install
    - npm-test
```

## Changelog

### 1.1.0

- Upgrade to Ubuntu 14.04

### 1.0.0

- Initial release

## License

**wercker-box-iojs** is licensed under the [MIT license](http://opensource.org/licenses/MIT). See `LICENSE.md` for the full license.
