# CFT to automate installation of Wordpress using Ansible

Setup Wordpress on ubuntu linux EC2 instance using ansible and automate this using a cloud formation template

**Objective**:

Use CM tools such as Puppet, Ansible, or Chef to automate the installation of basic Drupal or WordPress.Setup a sample site. Automate the solution using Cloudformation template.

**Deliverable**:

A cloudformation template that accepts user inputs as parameters where applicable ( for example, Admin password). This template should setup VPC, create subnets, launch a CM instance, pull the necessary code (modules, classes, recipes etc) from a GIT repo (or S3), and configure the web instance for basic Drupal or Wordpress setup.

**Approach**:

Step 1: For this assessment, I set up a test environment on VMWare Workstation to install wordpress on localhost using ansible(using a Ubuntu Linux image).

Step 2: Created a playbook for the installation of Apache, MySQL, PHP, Wordpress in the test Environment.

Step 3: After success of Step 2, I pushed this playbook to my GitHub account.

Step 4: Built a CloudFormation Template with parameters(Name.Password,.,etc;) and resources(VPC,subnets.,etc;) mentioned in the rerqurirements


**Mapping between AWS Resources**

<img width="573" alt="cft resource mapping" src="https://cloud.githubusercontent.com/assets/19828746/24269797/081cd75e-0fe9-11e7-85b1-757bce47ed18.png">


Step 5: Installed necessary packages(git, ansible, cfn-heat ...) to download the repo(mentioned in step3), run playbook, wait handle and  referencing parameters in Userdata. 

<img width="1280" alt="parameter2userdata" src="https://cloud.githubusercontent.com/assets/19828746/24136992/1333b1ba-0de8-11e7-8719-117c5e317d21.png">

Step 6: Tested the functioning of the CFT and pushed the Repository to GitHub https://github.com/sriramgaddipati/UbuntuAnsible 

**To Build the stack**:

1. Download  this repository https://github.com/sriramgaddipati/Ubun .

2. Create a stack using CloudFormation.json file in cloud formation.

3. Fill parameters of Stackname, DatabaseName, DBUser, DBPassword.. and choose an existing keypair for SSH connection.

4. The User parameters will give you access to corresponding mysqlDB and user on EC2 instance built.

**Output**:

Stack up and running, able to access EC2 instance and MySQLDB with input username and password. 

<img width="1280" alt="built stack" src="https://cloud.githubusercontent.com/assets/19828746/24136041/539ca676-0de3-11e7-9d24-b1d8a0611740.png">

**Access wordpress using url located here**

<img width="1257" alt="wordpress url" src="https://cloud.githubusercontent.com/assets/19828746/24271202/aaa93c1a-0fee-11e7-9e67-3183ff6e3691.png">


