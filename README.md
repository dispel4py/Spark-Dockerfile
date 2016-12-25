[![Docker Automated build](https://img.shields.io/docker/automated/reetawwsum/spark.svg)](https://hub.docker.com/r/reetawwsum/spark)

# Spark-Dockerfile
Dockerfile for Spark

## Features

1. CentOS 7
2. Java SE Development Kit 8u111
3. Hadoop 2.7.3
4. Spark 2.0.2

## Usage

Pull docker image from [DockerHub](https://hub.docker.com/r/reetawwsum/spark)

	$ docker pull reetawwsum/spark

To launch Spark

	$ docker run --rm -t -i --name spark -p 8888:8888 -p 50070:50070 -p 8088:8088 -p 8042:8042 -p 4040:4040 reetawwsum/spark --ip=0.0.0.0

To view Hadoop process status

	$ jps

To run Spark application in client mode

	$ spark-shell --master yarn --deploy-mode client --driver-memory 1g --executor-memory 1g --executor-cores 1

Clone this repo and

	$ git clone https://github.com/reetawwsum/Spark-Dockerfile.git
	$ cd Spark-Dockerfile

to build image from Dockerfile:

	$ docker build -t spark .

## License
[The MIT License (MIT)](LICENSE)
