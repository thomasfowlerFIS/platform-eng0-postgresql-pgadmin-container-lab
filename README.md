# Lab - PostgreSQL with PGAdmin and Containers

## **Objectives**

1. Utilize Docker's network capabilities to create a custom network.
1. Practice using different commands to instruct the container to
1. Demonstrate the use of port forwarding to allow PGAdmin to connect to PostgreSQL.

-------------------------------------------------

### **Requirements**

1. Docker container runtime

1. Latest version of `PostgreSQL` installed (e.g. via brew or installed via
source.)

1. Latest version of `PGAdmin` installed (e.g. via brew or installed via
source.)

1. Text editor to edit the `dockerfiles` containing the `PostgreSQL` database
and `PGAdmin` application.

-------------------------------------------------

### **Steps**

1. Run the following command from your terminal:
  `$ git clone https://github.com/thomasfowlerFIS/platform-eng0-postgresql-pgadmin-container-lab`

1. Change directories to the directory created in step 1. by
running:
  `$ cd [name of the directory in which the repository was cloned]`

1. Create 2 separate Dockerfiles: one to run `PostgreSQL` and the other to run `PGAdmin`

-------------------------------------------------

### **Deliverables**

In order to successfully complete this lab you must:

* Author a container image using a `dockerfile` that includes an instance
of `PostgreSQL`.
* Author a container image using a `dockerfile` that includes `PGAdmin`.
* The `PGAdmin` container automatically starts and connects to the
`PostgreSQL` instance.

-------------------------------------------------

### **Containerizing the Application**

> and the open source community at large. When in doubt, it's best to
> select the container image either from the source or officially endorsed
> by the organization.

For this lab we'll use Node's official `17-alpine3.15` container image. Your
objective is to use the resources provided to package the node application
so that it runs when the container is launched.

This lab is somewhat open-ended in that you must research on your *own* how
to containerize both `PostgreSQL` and `PGAdmin`.

#### **Stretch Goals**

* Try using a different base container image
  * What differences do you see?
  * Is the container image larger or smaller than before?

-------------------------------------------------

### **A Word on Port Forwarding**

To make the application behave as if it were running on the host you will
need to ensure that port forwarding from the host to the container is
established.

For example, if I wanted to run an NGINX container that serves content on
port 80, I would port forward port 80 on the host to port 80 on the container
with the following flag when using `docker run`:

`$ docker run -p 80:80 some-nginx-container:0.0.1`

-------------------------------------------------

### **Resources**

* [Dockerizing a Node.js Web App](https://nodejs.org/en/docs/guides/nodejs-docker-webapp/)

* [Docker's Container Networking Documentation](https://docs.docker.com/config/containers/container-networking/)

* [PostgreSQL's Official Docker Hub](https://hub.docker.com/_/postgres)

* [PGAdmin Container Information](https://www.pgadmin.org/download/pgadmin-4-container/)

-------------------------------------------------
