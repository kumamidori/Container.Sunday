# Cantainer.Sunday (Dec. 2020 version)

- Example of BEAR.Sunday application with Docker (PHP7.4, docker-sync, Mutagen)
- Based on the following contents by gamu1012:

[Docker \+ BEAR\.Sundayで開発するときはdocker\-syncを使おう \- Qiita](https://qiita.com/gamu1012/items/a66781f9d25bfe4e9c3f)

[hiroki\-saito/Container\.Sunday: BEAR\.SundayをDocker for Macで動かしたときの計測用リポジトリ](https://github.com/hiroki-saito/Container.Sunday)

## Usage

1. Default Docker

```
$ docker-compose build
$ docker-compose up
```

[http://localhost:1758/](http://localhost:1758/)

```
$ docker-compose down
$ rm -rf var/tmp/hal-app
```

2. Docker + docker-sync

```
$ docker-sync start
$ docker-compose -f docker-compose.docker_sync.yml up -d
```

[http://localhost:1758/](http://localhost:1758/)

```
$ docker-compose down
$ docker-sync stop
$ rm -rf var/tmp/hal-app
```

3. Docker + Mutagen

```
$ mutagen compose -f docker-compose.mutagen.yml up -d
```

[http://localhost:1758/](http://localhost:1758/)

```
$ mutagen compose -f docker-compose.mutagen.yml down
$ rm -rf var/tmp/hal-app
```

## Performance records

BEAR.Sunday application performance results by environment :

| Environment | Time [※] |
|---|---|
| Default Docker | 1.10 sec |
| Docker + docker-sync | 117 ms  |
| Docker + Mutagen | 162 ms |

[※] Mesured by Chrome DevTools [Network] tab

## Links

- TODO

## License

These codes are licensed under CC0.

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)
