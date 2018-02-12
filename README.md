# Repo manifest for OP-TEE development

In the OP-TEE project we try to gather all documentation under the
[optee_os](https://github.com/OP-TEE/optee_os) git, therefore we recommend that
you read the instructions at
[this](https://github.com/OP-TEE/optee_os/blob/master/README.md) page which
describes how to setup OP-TEE on various platforms.

**Note** that this branch, fr-dev, is used for development only and should not be pulled back into master.

Here are some commands that will get you up and running for a build :

```bash
mkdir OPTEE
cd $_
git clone https://github.com/ForgeRock/open-platform-trusted-exe-environment.git
cp open-platform-trusted-exe-environment/get_repo.sh .
./get_repo.sh 
git clone -bfr-dev https://github.com/ForgeRock/optee-manifest.git 
./repo init -u https://github.com/ForgeRock/optee-manifest.git -bfr-dev -martik530.xml
mkdir .repo/local_manifests
cp optee-manifest/local_manifests/dev.xml .repo/local_manifests/.
./repo sync
```
