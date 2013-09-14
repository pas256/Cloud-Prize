# Submission 1

## Which Categories Best Fit Your Submission and Why?

Either "Best Contribution to Operational Tools, Availability and Manageability" or "Best Usability Enhancement" or possibly "Best new feature"

## Describe your Submission

My goal was to make it much easier to get started with NeflixOSS. In order to accomplish this goal, I have created [Ansible](https://github.com/ansible/ansible/) playbooks to build instances (or AMIs) for various NetflixOSS projects. So far I have:
* Aminator
* Asgard
* Edda
* Eureka
* Ice
* Simian Army

Using these playbooks, I have also built AMIs for the some of the above projects, and made them public for anyone to use. The list and 1-click links to launch the AMIs can be found here:

https://github.com/Answers4AWS/netflixoss-ansible/wiki/AMIs-for-NetflixOSS

Some of the projects also have CloudFormation templates to automate the tedious stuff like creating Security Groups, ASGs and IAM Roles:

https://github.com/Answers4AWS/netflixoss-ansible/tree/master/cloudformation

The CloudFormation templates are definitely the easiest way to get started.

As an alternative (and the gain greater exposure for NeflixOSS), I have made some AMIs available via the AWS Marketplace:

https://aws.amazon.com/marketplace/seller-profile/?id=35bf36f1-7d03-4257-b273-8c97b3a5a48c


### Ansible Provisioner for Aminator

To build AMIs, you can use the Ansible Provisioner I have added to Aminator:

https://github.com/aminator-plugins/ansible-provisioner

This could perhaps be its own submission, but is a lot more powerful when combined with the above playbook. This allows anyone to easily build the same AMIs I have and run their own compiled versions of NetflixOSS projects.

## Provide Links to Github Repo's for your Submission

 - https://github.com/Answers4AWS/netflixoss-ansible
 - https://github.com/aminator-plugins/ansible-provisioner


* * *

# Submission 2

## Which Categories Best Fit Your Submission and Why?

Best New Monkey

## Describe your Submission

I have created Backup Monkey - a service that makes sure there are backups available in case something happens.

It does this by first looping through all EBS volumes, and creating snapshots of them with a specific prefix in the description.

Then it loops through all snapshots looking for that prefix, and removes the oldest ones. You can configure the maximum number of snapshots per volume to keep. This basically gives you a rolling backup system for EBS.

This monkey has no dependencies other than Python 2.7 and Boto. Edda is not used, though if others find this useful, there may be valuable info to pull in from edda.

It can be easily installed by running `pip install backup_monkey`.

## Provide Links to Github Repo's for your Submission

 - https://github.com/Answers4AWS/backup-monkey
 - https://pypi.python.org/pypi/backup_monkey (shows usage as number of downloads)


* * *

# Submission 3

## Which Categories Best Fit Your Submission and Why?

Best New Monkey

## Describe your Submission

Graffiti Monkey is a service that goes around tagging things.

It will loop through EBS volumes that are attached to instances, and copy the `Name` tag from the instance to the volume. It also adds 2 additional tags (`instance_id` and `device`). Then, it loops through the snapshots, and copies those 3 tags from the EBS volume to the Snapshot. This way, if an EC2 instance is terminated, you always know which EBS volumes and snapshots were associated with it.

Special thanks to Joe Sondow for the name (much better than Tag Propagation Monkey)


## Provide Links to Github Repo's for your Submission

 - https://github.com/Answers4AWS/graffiti-monkey
 - https://pypi.python.org/pypi/graffiti_monkey (shows usage as number of downloads)



* * *

# Notes

* If it makes more sense (or increases my chances of winning), combined the 2 monkeys together to be the __First Simian Battalion__. (Am I allowed to use that name?)
* [Answers for AWS](http://answersforaws.com/about/) is my consulting company. I am using that Github account to host my code.
