# AWS-STORE-API
Hosts a website on aws andallows search operaton as well as generate report

GO to AWS and login in to Amazon cloud9.

RUN the following commands:-

cd /home/ec2-user/environment

  To get the required files you can either use aws s3 storage or are provided in the github as well. 
wget https://aws-tc-largeobjects.s3-us-west-2.amazonaws.com/DEV-AWS-MO-Building_2.0/lab-1-s3.zip

 To unzip the file.  Run the following command:

    unzip lab-1-s3.zip
  
  To create a s3 bucket using CLI-
  aws s3api create-bucket --bucket ag-2021-4-26-s3site --region us-west-2 --create-bucket-configuration LocationConstraint=us-west-2

Next create a website_security_policy.json to allowonly a particular ip address to operate the website.

Write the static ip and bucket name in json file.

Next create a permission file and attach the json file with it.

RUN the following command to attach the policy to bucket.

cd python_3.6.8

ls

sudo pip3 install boto3 && sudo pip3 install --upgrade awscli && python3 permissions.py

#for node.js

npm install aws-sdk && node permissions.js
   
#for java

mvn clean install, then run mvn exec:java -Dexec.mainClass=com.mycompany.app.App
    
    
TO UPLOAD A WEBSITE:-

TO UPLOAD the sample website provides--upload_items.py provide it with bucket name and then run it on cli.

run the following command.

python3 upload_items.py

#for node.js

node upload_items.js

#for java

mvn exec:java -Dexec.mainClass=com.mycompany.app.App


## now visit the website url to see the changes.
https://ag-2021-4-26-s3site.s3-us-west-2.amazonaws.com/index.html



