# Submission 1

## Which Categories Best Fit Your Submission and Why?

Eiter "Best Contribution to Operational Tools, Availability and Manageability" or "Best Usability Enhancement"

## Describe your Submission

I have created [Ansible](https://github.com/ansible/ansible/) playbooks to build instances (or AMIs) for various NetflixOSS projects. So far I have
* Aminator
* Asgard
* Edda
* Eureka

I will be adding more soon.

To build AMIs, you can use the Ansible Provisioner I have added to Aminator:

https://github.com/Netflix/aminator/pull/121

## Provide Links to Github Repo's for your Submission

https://github.com/Answers4AWS/netflixoss-ansible



# Submission 2

## Which Categories Best Fit Your Submission and Why?

Best New Monkey

## Describe your Submission

I have created a monkey that makes sure there are backups available in case something happens.

It does this by first looping through all EBS volumes, and creating snapshots of them with a specific prefix in the description.

Then it loops through all snapshots looking for that prefix, and removed the oldest ones. You can configure the maximum number of snapshots per volume to keep.

This monkey has no dependencies other than Python 2.7 and Boto. Edda is not used, though if others find this useful, there may be valuable info to pull in from edda.


## Provide Links to Github Repo's for your Submission

https://github.com/Answers4AWS/backup-monkey


(Note: [Answers for AWS](http://answersforaws.com/about/) is my consulting company. I am using that Github account to host my code.)