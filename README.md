# cntsim
Chiplet Network Thermal co-simulation


## Docker usage
Mount repo folder with the docker file system 
```docker run -it -u houy4 -v [repo path on host]:[repo path on docker] [image]```

'''
docker run -it -u $(id -u):$(id -g) -v /home/houy4/workspace/envs/chipSim/gem5:/opt/gem5 -v /home/houy4/workspace/chipSim:/tmp/chipSim -e PATH=/opt/gem5/build/ALL:$PATH  gem5sim:ubuntu-24.04
'''
