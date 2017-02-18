# Blazegraph Vagrant
This repository creates a Vagrant VM that bundles the [Blazegraph](https://www.blazegraph.com/) triplestore and related dependencies.

See also https://github.com/blazegraph/database/tree/master/src/resources/deployment/vagrant/samples/VirtualBox

## Requirements

* [Vagrant](https://www.vagrantup.com/)
* [VirtualBox](https://www.virtualbox.org/)

## Usage

1. clone this repository
2. `cd blazegraph-vagrant`
3. `vagrant up` (and be patient)


The [Blazegraph 2.1.4](https://github.com/blazegraph/database/tree/BLAZEGRAPH_RELEASE_2_1_4) should be running and available
at [http://localhost:9999/bigdata/](http://localhost:9999/bigdata/)

To login:

```
$ vagrant ssh
```

## Loading RDF data

Place RDF data into the `./rdf` directory.  It can be accessed from the VM on the `/vagrant/rdf` directory. See the blazegrph documentation on loading data at https://wiki.blazegraph.com/wiki/index.php/Bulk_Data_Load

## Environment

* Ubuntu 16.04 64-bit machine
* [Blazegraph 2.1.4](https://github.com/blazegraph/database.git) at [http://localhost:9999/bigdata/](http://localhost:9999/bigdata/)

## Thanks

* This VM setup was heavily influenced (read: stolen) from [Fedora 4 Vagrant](https://github.com/fcrepo4-exts/fcrepo4-vagrant).
* The initial content and inspiration for this repository is taken from the [SPARQL Workshop](https://github.com/LODLAM/DLF15LODLAM/tree/master/SPARQL) given by [Tom Johnson](https://github.com/no-reply) at the DLF LODLAM meeting in 2015.
