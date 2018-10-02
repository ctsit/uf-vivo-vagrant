# UF Vivo Vagrant

This repo should contain all information needed to getting a vagrant box running with
all the customizations for the UF VIVO. We are currently using VIVO 1.9.

## Project

Thanks to Ted Lawless for maintaining vivo-vagrant. Most of the basic vivo work
is shamelessly copied from his vagrant. The goal here is to create a vagrant
with VIVO installed that will load all the UF triples and UF customizations. As
of 2-2016 their are about 22 million triples in the UF data set. People ask for
them and I think this is a better way to provide them as examples to some folks.
Your milage may vary.

## Prereqs

Step 1. Install the following
[Vagrant](http://www.vagrantup.com/)
[VirtualBox](https://www.virtualbox.org/)

## Install the VIVO Vagrant box

~~~
$ git clone https://github.com/senrabc/uf-vivo-vagrant.git uf-vivo-vagrant
$ cd uf-vivo-vagrant
$ make build_vivo_vagrant
~~~

OR

~~~
$ git clone https://github.com/senrabc/uf-vivo-vagrant.git uf-vivo-vagrant
$ cd uf-vivo-vagrant
$ vagrant up
~~~

If you encounter an error about host additions not being installed run these commands:

```
$ vagrant plugin install vagrant-vbguest
$ vagrant vbguest
```

When the Vagrant provisioning script is complete, the VIVO web application will be available in a browser on the host machine at `http://localhost:8080/vivo`.  You can log into your new VIVO with the default admin user (`vivo_root@school.edu`) and password (`rootPassword`), which are specified in the `/provision/vivo/deploy.properties` source file in this repository.

The source will be installed on the virtual machine at `/usr/local/vivo/`.

To login to the box:

~~~
$ vagrant ssh
~~~



## History

TODO: Write history

## Credits

TODO: Write credits

## References

https://github.com/lawlesst/vivo-vagrant
[Vagrant](http://www.vagrantup.com/) configuration and install scripts for running

## License

Apache 2:
http://www.apache.org/licenses/LICENSE-2.0
