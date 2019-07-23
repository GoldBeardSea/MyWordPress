# lab 41: Deployment
> Deploy a WordPress application to AWS!

## Features
### Create a full cloud deployment pipeline for your assigned application.
* Instantiate the appropriate server architecture
* Create, initialize, and load any databases
* Connect the application to the created database
* Automate the entire process with a CI/CD pipeline
  * Connect to github and auto-deploy from master
  * Run all automated tests


## Setup
Please visit [AWS] (https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/php-hawordpress-tutorial.html) for more detailed instructions.
1. Login to AWS and create an RDS database instance:
    1. Open the Amazon RDS console.
  2. Choose Databases in the navigation pane.
  3. Choose Create database.
  4. Choose a database engine. Choose Next.
  5. Choose a use case, if prompted.
  6. Under Specify DB details, review the default settings and adjust as necessary. Pay attention to the following options:
    * DB instance class – Choose an instance size that has an appropriate amount of memory and CPU power for your workload.
    * Multi-AZ deployment – For high availability, set to Create replica in different zone.
    * Master username and Master password – The database username and password. Make a note of these settings because you'll use them later.
  7. Choose Next.
  8. Under Database options, for Database name, type ebdb. Make a note of the Database port value for use later.
  9. Verify the default settings for the remaining options, and choose Create database.
2. Download [WordPress] (https://wordpress.org/)
  1. Download the configuration files from the sample [repository] (https://github.com/aws-samples/eb-php-wordpress/releases/download/v1.1/eb-php-wordpress-v1.zip)
  2. Extract WordPress and change the name of the folder.
  3. Extract the configuration files over the WordPress installation.
3. Create an Elastic Beanstalk Instance.
  1. Open the Elastic Beanstalk console using this preconfigured [link] (console.aws.amazon.com/elasticbeanstalk/home#/newApplication?applicationName=tutorials&environmentType=LoadBalanced).
  2. For Platform, choose the platform that matches the language used by your application.
  3. For Application code, choose Sample application.
  4. Choose Review and launch.
  5. Review the available options. When you're satisfied with them, choose Create app.
4. Create CodePipeline
  1. Go to AWS CodePipeline console 
  2. Set up a pipeline based around your source code in our case github. 
  3. Identify the github repositority and the branch to launch. 
  4. Skip Build for now. 
  5. Review and launch pipeline. 
  6. Edit and add build and test stages. 


![Code Pipeline](https://raw.githubusercontent.com/GoldBeardSea/MyWordPress/master/assets/Screen%20Shot%202019-07-23%20at%2012.52.03%20PM.png)


## Collaborators
* **Anthony Berry**  [Antberry] (https://github.com/Antberry)
* **Charles Clemens** [CClemensJr] (https://github.com/CClemensJr)
* **Matthew Burger** [mattburger] (https://github.com/mattburger)
* **Timothy Busch** [GoldBeardSea] (https://github.com/GoldBeardSea)
