# BigTravelData

Welcome to the Big Travel Data hackathon!


## Getting the SSH private key

`Note: This will only work at the HackReduce building`

In order to access the servers, you'll need to get the SSH keys. [Download it through your browser](http://10.101.49.148/hackreduce.pem) or with curl:

    $ curl -o ~/.ssh/hackreduce.pem -O http://10.101.49.148/hackreduce.pem
    $ chmod 600 ~/.ssh/hackreduce.pem

Now you can access the servers with the following command:

    $ ssh -i ~/.ssh/hackreduce.pem hackreduce@server

We'll be assigning each team/person a set of servers at the event.


## Accessing the datasets from the clusters

Every node has access to the datasets from the following directories:

    /mnt/hack_data_01
    /mnt/hack_data_02

These directories are read only. A scratch space is available under the following directory:

    /u01/teams

This is a globally writable directory, so be careful not to overwrite your competitor's data!

## Accessing the datasets from within HackReduce

`Note: This will only work at the HackReduce building`

While you're here at the HackReduce space, you can download the dataset files from the following server:

#### <http://10.101.49.148/>

Download them if you want/need to work with the data from your laptop.

## Some Goodies

Some goodies are provided if you need them: ElasticSearch cluster and a Redis instance.

### ElasticSearch

The elasticsearch cluster is publicly available on the following nodes (on the default ports):

    cluster-7-slave-[01-10].sl.hackreduce.net

The ElasticSearch Head plugin is available, so you can point your browser here <http://cluster-7-slave-01.sl.hackreduce.net:9200/_plugin/head>


### Redis

The Redis instance is available on the following node (on the default port):

    cluster-7-slave-11.sl.hackreduce.net

