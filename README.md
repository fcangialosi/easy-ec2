# Easy EC2 CLI

Wrapper around EC2's command line tools for dealing with instances by nickname

Quickly list all instances in your default region:

	ec2 ls

Start (or stop) an instance by nickname (this should be set ahead of time in AWS
console):

	ec2 start NICKNAME

Modify the instance type (e.g. from t2.nano to t2.small) of an instance by
nickname:

	ec2 change-type NICKNAME t2.small


You can also specify a different region, e.g.

	ec2 ls --region us-west-1

If the instance you are looking for is outside of your default region, you must
supply this flag or the tool won't be able to find it.

## Dependencies

1. AWS CLI 

On OS X: 

	brew install aws

Other platforms, if you have python (*note*: you have to manually add the
executable to your path):

	sudo pip install --upgrade awscli

2. gnu-sed

On OS X:

	brew install gnu-sed

## Configuration

If you haven't used the AWS CLI tools before, when you first run `ec2`, it will
ask you to configure a few parameters (*note*: these will be saved in ~/.aws)

You will need to specify your Access Key ID and Secret Access Key. These can be
found in the [AWS IAM Management
Console](https://console.aws.amazon.com/iam/home?#/home). If you haven't
already, you may need to create a new user here to get the proper keys.
