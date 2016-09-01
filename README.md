Amazon AWS Cloudformation templates for deploying Loris
===========

# loris_efs_autoscaling_template.json

This template file may be used to deploy a group of
Loris servers into a specified VPC.
The server group will:
 * autoscale depending on CPU load sending email notifications when it does
 * use a shared Elastic File System to cache images
 * pull source images from an S3 bucket

You will need to edit the json template file to point to your own loris2.conf and 000-default.conf
files in your S3 bucket (or wherever you choose to make them available).

# loris_template.json

This template may be used to deploy a simple Loris server into
the default VPC.

You will need to edit the json template file to point to your own loris2.conf and 000-default.conf
files in your S3 bucket (or wherever you choose to make them available).

# loris2.conf

Configuration file for the Loris application.  You will need to edit the loris2.conf file to set
 "source_prefix" in the resolver section to the S3 bucket containing your source images.

# 000-default.conf

Apache configuration file specifying the number of Loris processes and threads to run.
