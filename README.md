# QEMU IN A CONTAINER PLAYABLE THROUGH A BROWSER

Now, you can run DOS, Windows 95, Windows 98, Windows 98 SE, and Windows XP in a container!


The implementation is pretty straightforward. You can run it locally, or run it on a cloud-hosted service, like Azure Container Instances or Azure Kubernetes Services. In any case, you'll probably want to allocate at least 2 Gigs of RAM and 2 CPUs to make things run smoothly -- more for more graphic-intense emulators.

If you want to build it, simply clone the repo and run Docker Build.

`docker build -t qemu . ` 

Alternately, you can pull the image from Docker Hub.

`docker pull blaize/qemu-docker`

To run this locally, run a Docker command:

`docker run -v /path/to/your/isos:/isos -p 80:80 blaize/qemu-docker`

Once the container is running, point your browser to the IP address or host name of your Docker environment. Retroarch has a basic install here.

Build your oldschool PC and run your favorite OSs in the cloud!
