# Whats My Ip?

Really straight forward project, it will... display your IP address.

YAY!

See it online: <https://whatsmyip.s6l.fr/>

![preview](https://github.com/thomas-leroy/whatsMyIp/blob/master/screenshot.png?raw=true)

## Requirements

To launch this project, you need :

- node 8+
- yarn
- docker
- docker-compose

## Project setup

```bash
yarn install
```

### Compiles and hot-reloads for development

Launch API stack :

```bash
docker-compose up
```

Note : API is served through <http://localhost:8000>.

Serve front for Dev :

```bash
yarn serve
```

Front is now accessible via <http://localhost:8080>.

### Compiles and minifies for production

```bash
yarn build
```

### Lints and fixes files

```bash
yarn lint
```
