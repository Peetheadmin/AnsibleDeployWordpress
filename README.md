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


![screen shot 2018-02-07 at 11 58 14 pm](https://user-images.githubusercontent.com/12737517/35960150-99f79486-0c76-11e8-9183-32ef0d807db0.png)



Step 5: Installed necessary packages(git, ansible, cfn-heat ...) to download the repo(mentioned in step3), run playbook, wait handle and  referencing parameters in Userdata.

![screen shot 2018-02-08 at 12 02 57 am](https://user-images.githubusercontent.com/12737517/35960206-ce8a78d0-0c76-11e8-8570-449f641e47cf.png)

Step 6: Tested the functioning of the CFT and pushed the Repository to GitHub https://github.com/Peetheadmin/AnsibleDeployWordpress.git

**To Build the stack**:

1. Download  this repository https://github.com/Peetheadmin/AnsibleDeployWordpress.git .

2. Create a stack using CloudFormation.json file in cloud formation.

3. Fill parameters of Stackname, DatabaseName, DBUser, DBPassword.. and choose an existing keypair for SSH connection.

4. The User parameters will give you access to corresponding mysqlDB and user on EC2 instance built.

**Output**:

Stack up and running, able to access EC2 instance and MySQLDB with input username and password.

![screen shot 2018-02-08 at 2 12 29 am 2](https://user-images.githubusercontent.com/12737517/35960366-64849a82-0c77-11e8-9c18-2eeebd60b53f.png)

**Access wordpress using url located here**

![screen shot 2018-02-08 at 2 14 27 am](https://user-images.githubusercontent.com/12737517/35960385-7533416c-0c77-11e8-8274-bc68b202a2fe.png)
