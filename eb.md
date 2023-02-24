# Elastic Beanstalk Commands
1. `eb init`
```
% eb init
Select a default region
1) us-east-1 : US East (N. Virginia)
2) us-west-1 : US West (N. California)
3) us-west-2 : US West (Oregon)
4) eu-west-1 : EU (Ireland)
5) eu-central-1 : EU (Frankfurt)
6) ap-south-1 : Asia Pacific (Mumbai)
7) ap-southeast-1 : Asia Pacific (Singapore)
8) ap-southeast-2 : Asia Pacific (Sydney)
9) ap-northeast-1 : Asia Pacific (Tokyo)
10) ap-northeast-2 : Asia Pacific (Seoul)
11) sa-east-1 : South America (Sao Paulo)
12) cn-north-1 : China (Beijing)
13) cn-northwest-1 : China (Ningxia)
14) us-east-2 : US East (Ohio)
15) ca-central-1 : Canada (Central)
16) eu-west-2 : EU (London)
17) eu-west-3 : EU (Paris)
18) eu-north-1 : EU (Stockholm)
19) eu-south-1 : EU (Milano)
20) ap-east-1 : Asia Pacific (Hong Kong)
21) me-south-1 : Middle East (Bahrain)
22) af-south-1 : Africa (Cape Town)
    (default is 3):


Enter Application Name
(default is "image-processing-microservice"):
Application image-processing-microservice has been created.

It appears you are using Node.js. Is this correct?
(Y/n): Y
Select a platform branch.
1) Node.js 16 running on 64bit Amazon Linux 2
2) Node.js 14 running on 64bit Amazon Linux 2
   (default is 1):

Cannot setup CodeCommit because there is no Source Control setup, continuing with initialization
Do you want to set up SSH for your instances?
(Y/n): n
```
2. `eb create`
```
% eb create
Enter Environment Name
(default is image-processing-microservice-dev):
Enter DNS CNAME prefix
(default is image-processing-microservice-dev):

Select a load balancer type
1) classic
2) application
3) network
   (default is 2):


Would you like to enable Spot Fleet requests for this environment? (y/N): y
Enter a list of one or more valid EC2 instance types separated by commas (at least two instance types are recommended).
(Defaults provided on Enter):


2.0+ Platforms require a service role. We will attempt to create one for you. You can specify your own role using the --service-role option.
Type "view" to see the policy, or just press ENTER to continue:
Creating application version archive "app-230224_004546609925".
Uploading: [##################################################] 100% Done...
Environment details for: image-processing-microservice-dev
Application name: image-processing-microservice
Region: us-west-2
Deployed Version: app-230224_004546609925
Environment ID: e-wx4xc3kren
Platform: arn:aws:elasticbeanstalk:us-west-2::platform/Node.js 16 running on 64bit Amazon Linux 2/5.6.4
Tier: WebServer-Standard-1.0
CNAME: image-processing-microservice-dev.us-west-2.elasticbeanstalk.com
Updated: 2023-02-23 22:46:57.154000+00:00
Printing Status:
2023-02-23 22:46:55    INFO    createEnvironment is starting.
2023-02-23 22:46:57    INFO    Using elasticbeanstalk-us-west-2-228849525122 as Amazon S3 storage bucket for environment data.
2023-02-23 22:47:24    INFO    Created security group named: sg-085ebcd1a97b0b31d
2023-02-23 22:47:40    INFO    Created security group named: awseb-e-wx4xc3kren-stack-AWSEBSecurityGroup-OATSA6DM8LCR
2023-02-23 22:47:40    INFO    Created target group named: arn:aws:elasticloadbalancing:us-west-2:228849525122:targetgroup/awseb-AWSEB-ZNDEP0J8UFPZ/dd0e644cca67652a
2023-02-23 22:48:57    INFO    Created load balancer named: arn:aws:elasticloadbalancing:us-west-2:228849525122:loadbalancer/app/awseb-AWSEB-QKVCR6G7J4LR/e68f0fa2cd61712a
2023-02-23 22:49:15    INFO    Created Load Balancer listener named: arn:aws:elasticloadbalancing:us-west-2:228849525122:listener/app/awseb-AWSEB-QKVCR6G7J4LR/e68f0fa2cd61712a/c198bf0b5009944d
2023-02-23 22:49:46    INFO    Created Auto Scaling group named: awseb-e-wx4xc3kren-stack-AWSEBAutoScalingGroup-1RJAF7SUD4X5V
2023-02-23 22:49:46    INFO    Waiting for EC2 instances to launch. This may take a few minutes.
2023-02-23 22:50:01    INFO    Created Auto Scaling group policy named: arn:aws:autoscaling:us-west-2:228849525122:scalingPolicy:c24e0d50-75fe-4c6c-8c0c-7022d0561d95:autoScalingGroupName/awseb-e-wx4xc3kren-stack-AWSEBAutoScalingGroup-1RJAF7SUD4X5V:policyName/awseb-e-wx4xc3kren-stack-AWSEBAutoScalingScaleDownPolicy-bPJ2B8NCuQUz
2023-02-23 22:50:01    INFO    Created Auto Scaling group policy named: arn:aws:autoscaling:us-west-2:228849525122:scalingPolicy:2223912c-e8db-4b41-b8d4-8d14769a32c6:autoScalingGroupName/awseb-e-wx4xc3kren-stack-AWSEBAutoScalingGroup-1RJAF7SUD4X5V:policyName/awseb-e-wx4xc3kren-stack-AWSEBAutoScalingScaleUpPolicy-OvdoGfYIsndT
2023-02-23 22:50:02    INFO    Created CloudWatch alarm named: awseb-e-wx4xc3kren-stack-AWSEBCloudwatchAlarmHigh-1FFBVKWKC9M3H
2023-02-23 22:50:02    INFO    Created CloudWatch alarm named: awseb-e-wx4xc3kren-stack-AWSEBCloudwatchAlarmLow-1WUEO8PUVWNDD
2023-02-23 22:50:07    INFO    Instance deployment: You didn't specify a Node.js version in the 'package.json' file in your source bundle. The deployment didn't install a specific Node.js version.
2023-02-23 22:50:10    INFO    Instance deployment completed successfully.
2023-02-23 22:50:26    INFO    Application available at image-processing-microservice-dev.us-west-2.elasticbeanstalk.com.
2023-02-23 22:50:26    INFO    Successfully launched environment: image-processing-microservice-dev
```
3. `eb deploy`
```
% eb deploy
Creating application version archive "app-230224_005251998422".
Uploading: [##################################################] 100% Done...
2023-02-23 22:54:06    INFO    Environment update is starting.      
2023-02-23 22:54:11    INFO    Deploying new version to instance(s).
2023-02-23 22:54:15    INFO    Instance deployment: You didn't specify a Node.js version in the 'package.json' file in your source bundle. The deployment didn't install a specific Node.js version.
2023-02-23 22:54:18    INFO    Instance deployment completed successfully.
2023-02-23 22:54:24    INFO    New application version was deployed to running EC2 instances.
2023-02-23 22:54:24    INFO    Environment update completed successfully.
```
