# cntsim
Chiplet Network Thermal co-simulation


## Docker usage
A docker has been built for the simulator which can be pulled by
```
docker pull langleyhou/epic-cntsim-gem5:latest
```
When using the docker, the mount of this repo folder and the 
Mount repo folder with the docker ```/tmp``` folder is recommanded. The compiled Gem5 will be kept in local file system, hence it is ok the file on docker been cleared after the system has been terminated. With ```/tmp``` folder, you will not encounter the permission problem. 

Set the environment of ```$PATH``` so that ```gem5.opt``` command can work properly without using full build path. 
```
docker run -it -u $(id -u):$(id -g) -v [PATH-OF-CNTSIM]:/tmp/cntcim -e PATH=/opt/gem5/build/ALL:$PATH [IMAGE NAME]
```
```[IMAGE NAME]``` is supposed to be ```langleyhou/epic-cntsim-gem5:latest``` up to now.
