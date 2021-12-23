# Add self-hosted Runner to Github Actions on Ubuntu

## Provision a cloud server

## Install docker

```bash
curl -fsSL https://raw.githubusercontent.com/ycio/docker-installer/main/ubuntu.sh | bash
```

## Add user `ci` to run the runner

```
adduser ci
# ...
usermod usermod -aG sudo ci
usermod -aG docker ci
newgrp docker
```

## Adding self-hosted runners

Swich to user `ci` with the following command:

```
su ci
cd
```


Following [the document](https://docs.github.com/en/actions/hosting-your-own-runners/adding-self-hosted-runners) to add the self-hosted runner 

## Configuring the self-hosted runner application as a service

https://docs.github.com/en/actions/hosting-your-own-runners/configuring-the-self-hosted-runner-application-as-a-service
