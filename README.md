# Docker Installation on Mac

# Install Docker
$ brew cask install docker

# Launch Docker

Press ⌘ + Space to bring up Spotlight Search and enter Docker to launch Docker.  

In the Docker needs privileged access dialog box, click OK.  

Enter password and click OK.  

When Docker is launched in this manner, a Docker whale icon appears in the status menu. As soon as the whale icon appears, the symbolic links for docker, docker-compose, docker-credential-osxkeychain and docker-machine are created in /usr/local/bin.

$ ls -l /usr/local/bin/docker* 

lrwxr-xr-x  1 root     admin  54 14 Jun 12:46 /usr/local/bin/docker -> /Applications/Docker.app/Contents/Resources/bin/docker
lrwxr-xr-x  1 root     admin  77 14 Jun 12:46 /usr/local/bin/docker-compose -> /Applications/Docker.app/Contents/Resources/bin/docker-compose/docker-compose
lrwxr-xr-x  1 root     admin  73 14 Jun 12:46 /usr/local/bin/docker-credential-desktop -> /Applications/Docker.app/Contents/Resources/bin/docker-credential-desktop
lrwxr-xr-x  1 root     admin  77 14 Jun 12:46 /usr/local/bin/docker-credential-osxkeychain -> /Applications/Docker.app/Contents/Resources/bin/docker-credential-osxkeychain
lrwxr-xr-x  1 debasis  admin  50  5 Feb 10:47 /usr/local/bin/docker-machine -> ../Cellar/docker-machine/0.16.2/bin/docker-machine


# Start Docker  
Click on the docker whale icon in the status menu and wait for it to show Docker is running.

# Test Docker  

$ docker container run hello-world

$ docker container run -it ubuntu bash

$ docker version


 # Install Virtual Box (if using docker-machine)

 $ brew cask install virtualbox

 $ docker-machine create manager  

 To see how to connect your Docker Client to the Docker Engine running on this virtual machine, run: 
 
 $ docker-machine env manager  


 # Install command line completion  

$ brew install bash-completion
$ brew install docker-completion
$ brew install docker-compose-completion

# List of Docker commands  

$ docker --help

A self-sufficient runtime for containers

Options:
      --config string      Location of client config files (default
                           "/Users/debasis/.docker")
  -c, --context string     Name of the context to use to connect to the
                           daemon (overrides DOCKER_HOST env var and
                           default context set with "docker context use")
  -D, --debug              Enable debug mode
  -H, --host list          Daemon socket(s) to connect to
  -l, --log-level string   Set the logging level
                           ("debug"|"info"|"warn"|"error"|"fatal")
                           (default "info")
      --tls                Use TLS; implied by --tlsverify
      --tlscacert string   Trust certs signed only by this CA (default
                           "/Users/debasis/.docker/ca.pem")
      --tlscert string     Path to TLS certificate file (default
                           "/Users/debasis/.docker/cert.pem")
      --tlskey string      Path to TLS key file (default
                           "/Users/debasis/.docker/key.pem")
      --tlsverify          Use TLS and verify the remote
  -v, --version            Print version information and quit

Management Commands:
  builder     Manage builds
  config      Manage Docker configs
  container   Manage containers
  context     Manage contexts
  image       Manage images
  network     Manage networks
  node        Manage Swarm nodes
  plugin      Manage plugins
  secret      Manage Docker secrets
  service     Manage services
  stack       Manage Docker stacks
  swarm       Manage Swarm
  system      Manage Docker
  trust       Manage trust on Docker images
  volume      Manage volumes

Commands:
  attach      Attach local standard input, output, and error streams to a running container
  build       Build an image from a Dockerfile
  commit      Create a new image from a container's changes
  cp          Copy files/folders between a container and the local filesystem
  create      Create a new container
  diff        Inspect changes to files or directories on a container's filesystem
  events      Get real time events from the server
  exec        Run a command in a running container
  export      Export a container's filesystem as a tar archive
  history     Show the history of an image
  images      List images
  import      Import the contents from a tarball to create a filesystem image
  info        Display system-wide information
  inspect     Return low-level information on Docker objects
  kill        Kill one or more running containers
  load        Load an image from a tar archive or STDIN
  login       Log in to a Docker registry
  logout      Log out from a Docker registry
  logs        Fetch the logs of a container
  pause       Pause all processes within one or more containers
  port        List port mappings or a specific mapping for the container
  ps          List containers
  pull        Pull an image or a repository from a registry
  push        Push an image or a repository to a registry
  rename      Rename a container
  restart     Restart one or more containers
  rm          Remove one or more containers
  rmi         Remove one or more images
  run         Run a command in a new container
  save        Save one or more images to a tar archive (streamed to STDOUT by default)
  search      Search the Docker Hub for images
  start       Start one or more stopped containers
  stats       Display a live stream of container(s) resource usage statistics
  stop        Stop one or more running containers
  tag         Create a tag TARGET_IMAGE that refers to SOURCE_IMAGE
  top         Display the running processes of a container
  unpause     Unpause all processes within one or more containers
  update      Update configuration of one or more containers
  version     Show the Docker version information
  wait        Block until one or more containers stop, then print their exit codes

