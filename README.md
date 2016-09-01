# loris-cloudformation

These Amazon AWS Cloudformation templates may be used to deploy Loris servers into AWS.

The template file "loris_efs_autoscaling_template.json" can be used to deploy a group of
Loris servers into a specified VPC.
The server group will autoscale depending on server load and use a shared Elastic File System
to cache source and derived images.  The original source images are pulled from an S3
bucket which must be configured in the Resolver section of the loris2.conf file.

The template file "loris_template.json" may be used to deploy a simple Loris server into
the default VPC.
