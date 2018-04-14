To stop any continuing AWS charges:
 1. From your local machine, in your app folder, run:
 $ heroku addons:attach heroku-postgresql --as DATABASE

 You will be prompted to re-enter your app name to confirm.

 If you get an "Ambiguous identifier" error, run:
 $ heroku addons

 And replace "heroku-postgresql" above with the specific name of the database, in purple (e.g. postgresql-amorphous-57933)

 2. Go to Cloudwatch and delete all alarms
 3. Go to Cloudfront and delete all distros (cloudfront is pay per traffic bandwidth, so it will not affect your bill much to leave your distro setup)
 4. Go to Opsworks and stop all instances
 5. a. Go to EC2 - Instances and stop the Jenkins machine (terminate)
    b. If you have any other instances up that you created as part of this course, terminate them too.
 6. Go to RDS and delete all databases
 7. Cert Manager is free, either delete cert or not, no difference
 8. Route 53 costs $0.50 a month per hosted zone. Feel free to delete the zone or not.
 9. S3 is pay per data transfered, so you will not be charged if you stop using it.

If you'd like to use your new domain name and ssl cert for your heroku app, view:
 1. https://devcenter.heroku.com/articles/custom-domains
 2. https://devcenter.heroku.com/articles/ssl-endpoint (edited)

 
