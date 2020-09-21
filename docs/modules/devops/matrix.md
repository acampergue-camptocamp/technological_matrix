Liste outils et usage camptocamp

# draw.io & Google Slides
# gopass
implementation go du soft de gestion de password "pass", permet d'ecrire/lire des password dans une base partagee sur Git
https://github.com/gopasspw/gopass
https://github.com/gopasspw/gopass/blob/master/docs/features.md


# Summon
charge des variables d'environnement en utilisant un fichier secrets.yaml dans lequel on peut specifier ou aller chercher les valeurs correspondantes.
A l'aide du gopass provider, on peut aller chercher les valeurs directement dans la base de password gopass.
https://cyberark.github.io/summon/
https://github.com/gopasspw/gopass/blob/master/docs/summon-provider.md

# ArgoCD
Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.
https://argoproj.github.io/argo-cd/

# Tekton
Tekton Pipelines is a Kubernetes extension that installs and runs on your Kubernetes cluster. It defines a set of Kubernetes Custom Resources that act as building blocks from which you can assemble CI/CD pipelines. Once installed, Tekton Pipelines becomes available via the Kubernetes CLI (kubectl) and via API calls, just like pods and other resources. Tekton is open-source and part of the CD Foundation, a Linux Foundation project.
https://github.com/tektoncd/pipeline/tree/master/docs
Building%20images%20%20efficiently%20and%20securely%20on%20Kubernetes%20with%20BuildKit.pdf
https://docs.docker.com/develop/develop-images/build_enhancements/

# Skaffold
Skaffold is a command line tool that facilitates continuous development for Kubernetes applications. You can iterate on your application source code locally then deploy to local or remote Kubernetes clusters. Skaffold handles the workflow for building, pushing and deploying your application. It also provides building blocks and describe customizations for a CI/CD pipeline.
https://github.com/GoogleContainerTools/skaffold#install-skaffold

# Ksync
ksync speeds up developers who build applications for Kubernetes. It transparently updates containers running on the cluster from your local checkout. This enables developers to use their favorite IDEs, such as Atom or Sublime Text to work from inside a cluster instead of from outside it. There is no reason to wait minutes to test code changes when you can see the results in seconds.
https://github.com/ksync/ksync

# Flux
Flux is the operator that makes GitOps happen in your cluster. It ensures that the cluster config matches the one in git and automates your deployments.
Flux enables continuous delivery of container images, using version control for each step to ensure deployment is reproducible, auditable and revertible. Deploy code as fast as your team creates it, confident that you can easily revert if required.
https://www.weave.works/oss/flux/

# Kaniko
kaniko is a tool to build container images from a Dockerfile, inside a container or Kubernetes cluster.
kaniko doesn't depend on a Docker daemon and executes each command within a Dockerfile completely in userspace. This enables building container images in environments that can't easily or securely run a Docker daemon, such as a standard Kubernetes cluster.
https://github.com/GoogleContainerTools/kaniko#demo

# Builda (RH)
https://github.com/containers/buildah

# Podman (RH)
Podman (the POD MANager) is a tool for managing containers and images, volumes mounted into those containers, and pods made from groups of containers. Podman is based on libpod, a library for container lifecycle management that is also contained in this repository. The libpod library provides APIs for managing containers, pods, container images, and volumes.
https://github.com/containers/podman

# Skopeo (RH)
skopeo is a command line utility that performs various operations on container images and image repositories.
skopeo does not require the user to be running as root to do most of its operations.
skopeo does not require a daemon to be running to perform its operations.
skopeo can work with OCI images as well as the original Docker v2 images.
https://github.com/containers/skopeo

# Buildkit
BuildKit is a toolkit for converting source code to build artifacts in an efficient, expressive and repeatable manner.
Key features:
- Automatic garbage collection
- Extendable frontend formats
- Concurrent dependency resolution
- Efficient instruction caching
- Build cache import/export
- Nested build job invocations
- Distributable workers
- Multiple output formats
- Pluggable architecture
- Execution without root privileges
https://github.com/moby/buildkit
https://static.sched.com/hosted_files/kccnceu19/12/Building%20images%20%20efficiently%20and%20securely%20on%20Kubernetes%20with%20BuildKit.pdf
https://docs.docker.com/develop/develop-images/build_enhancements/

# Rancher
Rancher is an open source software platform that enables organizations to run and manage Docker and Kubernetes in production. With Rancher, organizations no longer have to build a container services platform from scratch using a distinct set of open source technologies. Rancher supplies the entire software stack needed to manage containers in production.
https://rancher.com/docs/rancher/v1.6/en/

# Rancher2
Rancher was originally built to work with multiple orchestrators, and it included its own orchestrator called Cattle. With the rise of Kubernetes in the marketplace, Rancher 2.x exclusively deploys and manages Kubernetes clusters running anywhere, on any provider.
Rancher can provision Kubernetes from a hosted provider, provision compute nodes and then install Kubernetes onto them, or import existing Kubernetes clusters running anywhere.
One Rancher server installation can manage thousands of Kubernetes clusters and thousands of nodes from the same user interface.
https://rancher.com/docs/rancher/v2.x/en/

# RKE
RKE is a CNCF-certified Kubernetes distribution that runs entirely within Docker containers. It solves the common frustration of installation complexity with Kubernetes by removing most host dependencies and presenting a stable path for deployment, upgrades, and rollbacks. 
https://rancher.com/products/rke/
https://rancher.com/docs/rke/latest/en/

# K3S 
Lightweight Kubernetes. Easy to install, half the memory, all in a binary of less than 100 MB.
https://k3s.io/
https://github.com/rancher/k3s
https://rancher.com/docs/k3s/latest/en/networking/
Upstream Kubernetes allows a Service of type LoadBalancer to be created, but doesn’t include the implementation of the LB. Some LB services require a cloud provider such as Amazon EC2 or Microsoft Azure. By contrast, the K3s service LB makes it possible to use an LB service without a cloud provider.
https://github.com/rancher/klipper-lb

# K3D
k3d is a lightweight wrapper to run k3s (Rancher Lab’s minimal Kubernetes distribution) in docker.
k3d makes it very easy to create single- and multi-node k3s clusters in docker, e.g. for local development on Kubernetes.
https://k3d.io/
https://github.com/rancher/k3d
https://felixwiedmann.de/k3d-manage-k3s-clusters/
https://dev.to/bufferings/tried-k8s-istio-in-my-local-machine-with-k3d-52gg
https://github.com/rancher/k3d/issues/219
https://forums.rancher.com/t/k3s-traefik-dashboard-activation/17142/9

# Kind - Kubernetes in Docker
Kind is a tool for running local Kubernetes clusters using Docker container "nodes".

https://kubernetes.io/docs/setup/learning-environment/kind/
https://github.com/kubernetes-sigs/kind
https://kind.sigs.k8s.io/docs/user/quick-start/

## Problems & solutions

can't access cluster after k3d restart
https://github.com/rancher/k3d/issues/262
https://k3d.io/faq/faq/#restarting-a-multi-server-cluster-or-the-initializing-server-node-fails

# Traefik
Traefik is a modern HTTP reverse proxy and load balancer made to deploy microservices with ease.
Traefik is an open-source Edge Router that makes publishing your services a fun and easy experience. It receives requests on behalf of your system and finds out which components are responsible for handling them.
What sets Traefik apart, besides its many features, is that it automatically discovers the right configuration for your services. The magic happens when Traefik inspects your infrastructure, where it finds relevant information and discovers which service serves which request.
https://github.com/helm/charts/tree/master/stable/traefik#configuration
https://docs.traefik.io/
https://docs.traefik.io/operations/dashboard/

# Istio
https://istio.io/latest/docs/setup/getting-started/
https://istio.io/latest/docs/setup/additional-setup/config-profiles/
https://istio.io/latest/docs/setup/install/istioctl/

# Openstack
https://www.openstack.org/

# Openshift
OKD : version Opensource https://www.okd.io/
OC ? : Version payante
inclus OCS : Gestionnaire de FS, anciennement Glusterfs dans Openshift3, puis Ceph dans Openshift4, backporte dans la version payante de Openshift 3

https://www.openshift.com/

# Gitlab Autodevops
Auto DevOps provides pre-defined CI/CD configuration allowing you to automatically detect, build, test, deploy, and monitor your applications. Leveraging CI/CD best practices and tools, Auto DevOps aims to simplify the setup and execution of a mature and modern software development lifecycle
https://docs.gitlab.com/ee/topics/autodevops/
https://youtu.be/0Tc0YYBxqi4

# Heroku buildpack
Buildpacks are responsible for transforming deployed code into a slug, which can then be executed on a dyno. Buildpacks are composed of a set of scripts, and depending on the programming language, the scripts will retrieve dependencies, output generated assets or compiled code, and more. This output is assembled into a slug by the slug compiler.
Heroku’s support for Ruby, Python, Java, Clojure, Node.js, Scala, Go and PHP is implemented via a set of open source buildpacks.
https://devcenter.heroku.com/articles/buildpacks

# Project Syn
Project Syn is a pre-integrated set of tools to provision, update, backup, observe and react/alert production applications on Kubernetes and in the cloud. It supports DevOps through full self-service and automation using containers, Kubernetes and GitOps.
https://syn.tools/syn/index.html
https://vshn.ch/en/syn/



# Helm controller
A simple way to manage helm charts with a Custom Resource Definitions in k8s.
allow for CRD-driven deployment of helm manifests
https://github.com/rancher/helm-controller

# Vitess
Vitess is a database solution for deploying, scaling and managing large clusters of open-source database instances. It currently supports MySQL and MariaDB. It’s architected to run as effectively in a public or private cloud architecture as it does on dedicated hardware. It combines and extends many important SQL features with the scalability of a NoSQL database.
https://vitess.io/docs/get-started/operator/


Marc Sutter:spiral_calendar_pad: ce ticket est intéressant. J’avais jouer avec des tools pour que les dev’s ouisse deployer des trucs en pre-commit. Pas besoin de git push pour deployer sur un env de dev. ça a jamais été implémenté et Tobias est tres intéressé par ce truc.
10:35
donc voici quelques os à ronger pour toi -->
10:35
aurelien.campergue:house_with_garden: ha, j'ai lu un truc hier a ce sujet
10:35
Marc Sutter:spiral_calendar_pad: https://tilt.dev/
tilt.devtilt.dev
Tilt
Kubernetes for Prod, Tilt for Dev
10:36
tilt c’est kubernetes et Openshift compatible
10:36
https://docs.openshift.com/container-platform/4.4/cli_reference/developer_cli_odo/understanding-odo.html
10:36
odo c’est la soluce de redhat pour Openshift only


https://tilt.dev/
https://docs.openshift.com/container-platform/4.4/cli_reference/developer_cli_odo/understanding-odo.html
https://www.bizety.com/2020/07/02/kubernetes-tools-helm-skaffold-tilt-draft-and-garden/

Marc Sutter:spiral_calendar_pad: Donc mau lieu d’utiliser les build openshift (https://docs.openshift.com/container-platform/4.5/builds/understanding-buildconfigs.html), l’idée c’est de se basé sur des trucs plus standart dans le monde kubernetes, genre postman, skopeo, etc….

# Tilt
Productivity for teams building Kubernetes apps.
Smart Rebuilds, Continuous Feedback, Live Updates, Snapshots, and a lot more. tilt up and grok your workflow.
https://tilt.dev/

# Kubernetes Tools: Helm, Skaffold, Tilt, Draft, and Garden
https://www.bizety.com/2020/07/02/kubernetes-tools-helm-skaffold-tilt-draft-and-garden/

# Kapitan
Generic templated configuration management for Kubernetes, Terraform and other things
Kapitan is a tool to manage complex deployments using jsonnet, kadet (alpha) and jinja2.
Use Kapitan to manage your Kubernetes manifests, your documentation, your Terraform configuration or even simplify your scripts.
https://kapitan.dev/

# BFG Repo-Cleaner
https://rtyley.github.io/bfg-repo-cleaner/

# Quay container Security integration
The Container Security Operator brings Quay and Clair metadata into OpenShift.
Installing this operator enables cluster administrators to monitor known container image vulnerabilities in pods running on their Kubernetes cluster.
https://www.openshift.com/blog/openshift-4-3-quay-container-security-integration


# Ingress controllers

https://medium.com/flant-com/comparing-ingress-controllers-for-kubernetes-9b397483b46b
https://medium.com/swlh/kubernetes-ingress-controller-overview-81abbaca19ec

## Ambassador
https://github.com/datawire/ambassador

## Nginx
## Contour 

## ISTIO controllers
https://istio.io/latest/docs/tasks/traffic-management/ingress/

# nip.io