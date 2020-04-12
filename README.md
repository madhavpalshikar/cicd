# 1. Creating Jekins Container

    ## Build Image
    docker build -t jenkins-ci:0.1 .

    ## Run Container
    docker run -p 8080:8080 -p 50000:50000 jenkins-ci:0.1

# 2. Creating Ansible Container

    ## Build Image
    docker build --build-arg ANSIBLE_VERSION=2.5.0 -t ansible-image:local .

    ## Run Contianer
    docker run --rm ansible-image:local ansible --version

# 3. Creating Ubuntu Container

    ## Build Image
    docker build -t ubuntu-ci:0.1 .

    ## Run Container
    docker run -d ubuntu-ci:0.1

    ## Connect Container In Interactive Mode
    docker exec -it CONTAINER-ID bash 
