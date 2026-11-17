This page tracks my effort to simplify my personal technical stack in February of 2026

# Migration from gogs to github
I currently use [[gogs]], I would like to move to a hosted git server like [[github]].  This would simplify my use of static content websites like [[hugo]].  

## Publishing
- [hugo-actions to run hugo on github](https://github.com/peaceiris/actions-hugo)

## Repos to move
- Homedir

## Secrets Management
- Use `pass` like in https://nali.org/wiki/tech/apps/imapfilter/
# Service Replacement
- FreshRSS
	- inoreader - possibly free tier, pro is $90/year (first year $60) or $10/month
	- ReadWise Reader - no free tier, $120/year or $13/month

# Install Single Node OpenShift on Risk
- [Install SNO Procedure](https://docs.redhat.com/en/documentation/openshift_container_platform/4.11/html/installing/installing-on-a-single-node)

# S3 content hosting
My idea is to move from VM storage to an [[AWS]] S3 bucket.

- [fuse-s3fs](https://github.com/s3fs-fuse/s3fs-fuse) to mount on VMs
- Running Hugo to S3 publishing
	- [glukhov](https://www.glukhov.org/post/2025/12/hugo-website-deployment-to-aws-s3-with-aws-cli/)
	- [blinc.nz](https://blinc.nz/posts/hugo-s3/)
## Pricing
- [AWS Calculator]()
	- S3 standard - $0.023/GB/mo

## Storage needs
- Git repositories - 2.1G
- File storage - 123G ($2.83)
