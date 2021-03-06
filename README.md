# README FIRST
Collection of docker-compose files for randome containers running on QNAP Container Station and rough guides to build usable virtualized images, workbench and homelab environments running on QNAP Virtualization Station. These are used various personal projects I am working on my free time.

My current environment is based on QNAP firmware release QTS 4.4.2. I consider Virtualization Station being a modern and feature rich experience to manage virtual machines. However Container Station station is based heavily outdated docker release 17.09.1-ce which somehow limits what you can experiment with containers and docker-compose. 

About virtual machines:
---
So far all VM images are baselined to Ubuntu 18.04 LTS Server ... simply because I have personally learned to like Debian based Ubuntu Linux distributions. This may change as Ubuntu is pushing snap, instead of 'apt' as the package manager in future releases.

About containers (and docker-compose files):
---
**[Portainer CE](https://portainer.io)**  
This is my choise as a Container Manager in QNAP environment. 

How to deploy using 'portainer-docker-compose.yaml' file:  
In QNAP WebUI Open 'Container Station' -> click 'Create' -> click '+Create Application' (top right corner of 'Create' page) and paste yaml-file content into the 'Create Application' editor window. To deploy the container type name of application to 'Application name' field -> click 'Validate YAML' (optional but always useful) -> and click 'Create'. As the result 'portainer' should be running and you may create and manager other containers via portainer.  

Post installation steps:
- Create admin user as part of the first login
- Define 'Public IP' under Settings -> Endpoints -> primary (name of endpoint which was created)

Accessing portainer WebUI: [http://nas-webui-ip-addr:9000](http://nas-webui-ip-addr:9000)

Notes related to 'portainer-docker-compose.yaml': 
- I use 'host' networking for portainer, as I want to have portainer accessable from same IP address than my NAS WebUI
- Only port 9000 is exposed and mapped for portainer WebUI
- I am well aware that mounting '/var/run/docker.sock' is security risk but in my closed environment I consider that risk managable.



TO DO:
---
Brief description and direct link to guides.
