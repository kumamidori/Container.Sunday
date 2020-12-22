# Cantainer.Sunday (2020, kumamidori version)

- PHP8, BEAR.Sunday and Mutagen environment performance records
- Based on the following contents by gamu1012:

- [Docker \+ BEAR\.Sundayで開発するときはdocker\-syncを使おう \- Qiita](https://qiita.com/gamu1012/items/a66781f9d25bfe4e9c3f)
- [hiroki\-saito/Container\.Sunday: BEAR\.SundayをDocker for Macで動かしたときの計測用リポジトリ](https://github.com/hiroki-saito/Container.Sunday)

## Usage

1. Default Docker

```
$ docker-compose build
$ docker-compose up
```

[http://localhost:1758/](http://localhost:1758/)

```
$ docker-compose down
```

2. Docker + Mutagen

```
$ mutagen compose -f docker-compose.mutagen.yml up -d
```

[http://localhost:1758/](http://localhost:1758/)

```
$ mutagen down
```

3. Docker + docker-sync

```
$ docker-sync start
$ docker-compose  -f docker-compose.docker_sync.yml up
```

[http://localhost:1758/](http://localhost:1758/)

```
$ docker-compose down
$ docker-sync end
```

## Performance records

Chrome developer tool [Network] tab results:

```
Default Docker         
Docker + Mutagen      
Docker + docker-sync
```

## Links

- ★TODO★

## License

These codes are licensed under CC0.

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png "CC0")](http://creativecommons.org/publicdomain/zero/1.0/deed.ja)
