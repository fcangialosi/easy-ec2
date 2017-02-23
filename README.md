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
