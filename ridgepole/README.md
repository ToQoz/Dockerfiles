## ridgepole

docker container for [ridgepole](https://github.com/winebarrel/ridgepole)

```
docker run --rm -v Schemafile:/Schemafile toqoz/ridgepole -c '{adapter: "mysql2", database: "db"}' --apply --dry-run
```
