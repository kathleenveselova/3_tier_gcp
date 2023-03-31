# Instructions how to create the resouses in us-central-1 region:

## Setting billing account. Creating the project:

#### 1) Open in terminal of "account"
#### 2) Run commands below:
```
terraform init
terraform apply -auto-approve
```

## BUILD The Resourses in us-central1 region:
### Creating Global VPC with auto configured subnets. Creating ASG with LB. Creating CloudSQL to use with wordpress.

#### 1) Create project.tfvars file (the name of the file is very important, it should be exactly <project.tfvars>). Write the code with nesessary region and zone. For example, if you'd like to create resources in us-central1 region and central1-a zone, you should put the code below:
```
region = "us-central1"

zone = "us-central1-a"
```

#### 2) Open in terminal of "project"
#### 3) Run command below:
```
make build-project
```


## DESTROY The Resourses in us-central1 region:
### Destroying Global VPC with auto configured subnets. Destroying ASG with LB. Destroying CloudSQL to use with wordpress.

### 1) Open in terminal of "project"
### 2) Run command below:
```
make destroy-project
```