# Set up a FREE SSL on amazon AWS ec2
If you are using AWS Elastic Beanstalk, you may need to have your website to have a valid certificate without paying for a (non needed) load balancer (when you have only one instance)

## Steps 0 : 
Add elastic beanstalk configurations : 
* CERTDOMAIN : your domain name
* EMAIL : your email address

## Steps 1 : 
This configures the nginx server to answer to the letsencrypt challenge + request a new certificate.

Do this just the first time !!

Place the one/.ebextensions folder in the root of the zip you are deploying.

## Step 2 :
This configures the https gateway for nginx server.
Now replace two/.ebextensions folder in the root of the zip you are deploying (on every deployment).


### Notes :
Check 999_https_custom.conf to point to the right port of your application
