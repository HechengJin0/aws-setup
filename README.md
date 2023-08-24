# aws-setup

login: pi.tt/awslogin

@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command " [System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"


$ CURRENT_VERSION=2.26.1

$ wget https://github.com/Versent/saml2aws/releases/download/v${CURRENT_VERSION}/saml2aws_${CURRENT_VERSION}_linux_amd64.tar.gz

$ tar -xzvf saml2aws_${CURRENT_VERSION}_linux_amd64.tar.gz -C ~/.local/bin

$ chmod u+x ~/.local/bin/saml2aws

$ saml2aws --version

saml2aws configure : click shibboleth

https://github.com/Versent/saml2aws


https://www.hpcworkshops.com/05-create-cluster/01-create-cluster.html


export SINGULARITY_DOCKER_USERNAME=AWS 
export SINGULARITY_DOCKER_PASSWORD=$(aws ecr get-login-password)

