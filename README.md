# AWS cli

## Versions
* [1.16.16, latest](https://github.com/inserteffect/docker-awscli/tree/master/1.16.16) available as ```inserteffect/aws-cli:latest``` at [Docker Hub](https://hub.docker.com/r/inserteffect/aws-cli/)

## Environment Variables
* ```AWS_DEFAULT_REGION``` (Default: eu-central-1)
* ```AWS_DEFAULT_OUTPUT``` (Default: json)
* ```AWS_ACCESS_KEY_ID```
* ```AWS_SECRET_ACCESS_KEY```

## Usage

```
docker run -e AWS_ACCESS_KEY_ID=******** -e AWS_SECRET_ACCESS_KEY=********* inserteffect/aws-cli aws iam list-users
```
