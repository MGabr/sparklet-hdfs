# Sparklet-HDFS
> A small Spark cluster, running in standalone mode and a Hadoop cluster, running in pseudo distributed mode. 
Suitable for testing and development.

> [Sparklet](https://github.com/unchartedsoftware/sparklet) extended to support HDFS

## Usage

By default, this container will run a `spark-shell`.

```bash
$ docker build -t mgabr/sparklet-hdfs .
$ docker run -p 8080:8080 -p 50070:50070 -it mgabr/sparklet-hdfs
```

If you want to pass arguments to `spark-shell`:

```bash
$ docker run -it mgabr/sparklet-hdfs spark-shell --packages software.uncharted.sparkpipe:sparkpipe-core:1.1.0
```

It takes some time to start up, so consider using `sleep 30` when using it in scripts right away.