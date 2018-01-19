# cityofnewyork-addressparser
Dockerize [NYC 5 Boroughs address extractor][cityofnewyork-addressparser]

# Build

An image tagged with `warenix/addressparser-docker` will be built.
```sh
cd script
sh build.sh
```

# Usage

Refer to official addressparser's [Readme](addressparser/README.md) how to apply *APP\_ID* and *APP\_KEY*.

```sh
docker run -ti --rm -p 5000:5000 \
	-e DOITT_CROL_APP_ID={{APP_ID}}\
	-e DOITT_CROL_APP_KEY={{APP_KEY}}\
	warenix/addressparser-docker python /app/webserver.py
```

On success you should see console output like this:

```sh
 * Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
```

[Explore the api](http://localhost:5000/api)

[cityofnewyork-addressparser]:https://github.com/CityOfNewYork/addressparser
