# singularity-docker-centos7-brave
centos7 container to run brave (https://brave.com/)


Running without installation:
```
singularity run shub://truatpasteurdotfr/singularity-docker-centos7-brave
```
Building:
```
sudo singularity build singularity-docker-centos7-brave.simg  Singularity
```
Download and rename:
```
singularity pull --name "singularity-docker-centos7-brave" shub://truatpasteurdotfr/singularity-docker-centos7-brave
```
Running with a separate $HOME 
```
mkdir -p  ~/singularity.d/home/singularity-docker-centos7-brave
singularity run -H  ~/singularity.d/home/singularity-docker-centos7-brave singularity-docker-centos7-brave.simg
```
