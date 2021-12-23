# Add self-hosted Runner to Github Actions on Ubuntu

## Provision a cloud server (ubuntu)

Provision a ubuntu server. 

The next steps will be running on the ubuntu server.

## Install neccessary packages

```bash
curl -fsSL https://raw.githubusercontent.com/ycio/add-self-hosted-runner-to-github-actions/main/install-packages.sh | bash
```

## Install docker

```bash
https://raw.githubusercontent.com/ycio/add-self-hosted-runner-to-github-actions/main/install-docker.sh | bash
```

## Add user `ci` to run the runner

```
adduser ci
# ...
usermod -aG sudo ci
usermod -aG docker ci
newgrp docker
```

## Adding self-hosted runners

Swich to user `ci` with the following command:

```
su ci
cd
```


Follow [the document](https://docs.github.com/en/actions/hosting-your-own-runners/adding-self-hosted-runners) to add the self-hosted runner.

## Configuring the self-hosted runner application as a service

Follow the [instructions](https://docs.github.com/en/actions/hosting-your-own-runners/configuring-the-self-hosted-runner-application-as-a-service) to run the runner as a service.
