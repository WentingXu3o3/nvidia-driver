# nvidia-driver

```
dpkg -l | grep nvidia-driver
```
```
sudo apt-get purge nvidia*
```

check your driver version if it is installed properly
```
cat /proc/driver/nvidia/version
```
Inside docker container:
```
sudo vim /etc/nvidia-container-runtime/config.toml, then changed no-cgroups = false, save

Restart docker daemon: sudo systemctl restart docker, then you can test by running sudo docker run --rm --runtime=nvidia --gpus all ubuntu nvidia-smi 
```
