AWS Integration Pack
=====
The StackStorm AWS integration pack supplies action integration for EC2 and Route53.

#### Setup

You will need to add a set of AWS credentials, and default zone to the config.yaml file:

	---
	setup:
	  region: ""
	  aws_access_key_id: ""
	  aws_secret_access_key: ""
	interval: 20
	st2_user_data: ""

You can generate the access key and secret access key by following these directions:

http://docs.aws.amazon.com/IAM/latest/UserGuide/ManagingCredentials.html#Using_CreateAccessKey

##### st2_user_data

Optionally, you can set the user_data to set a default file to be used during new instance creation.  Put your user_data file somewhere accessible by the StackStorm user, and use the st2_user_data config option to set it.

	st2_user_data: "/full/path/to/file"

This file/script will be used for all invocations of the ec2_run_instances action

#### Route53 Actions

* r53\_build\_base\_http\_request
* r53\_change\_rrsets
* r53\_close
* r53\_create\_health\_check
* r53\_create\_hosted\_zone
* r53\_create\_zone
* r53\_delete\_health\_check
* r53\_delete\_hosted\_zone
* r53\_get\_all\_hosted\_zones
* r53\_get\_all\_rrsets
* r53\_get\_change
* r53\_get\_hosted\_zone
* r53\_get\_hosted\_zone\_by\_name
* r53\_get\_http\_connection
* r53\_get\_list\_health\_checks
* r53\_get\_path
* r53\_get\_proxy\_auth\_header
* r53\_get\_proxy\_url\_with\_auth
* r53\_get\_zone
* r53\_get\_zones
* r53\_handle\_proxy
* r53\_make\_request
* r53\_new\_http\_connection
* r53\_prefix\_proxy\_to\_path
* r53\_proxy\_ssl
* r53\_put\_http\_connection
* r53\_server\_name
* r53\_set\_host\_header
* r53\_set\_request\_hook
* r53\_skip\_proxy
* r53\_zone\_add\_a
* r53\_zone\_add\_cname
* r53\_zone\_add\_mx
* r53\_zone\_add\_record
* r53\_zone\_delete
* r53\_zone\_delete\_a
* r53\_zone\_delete\_cname
* r53\_zone\_delete\_mx
* r53\_zone\_delete\_record
* r53\_zone\_find\_records
* r53\_zone\_get\_a
* r53\_zone\_get\_cname
* r53\_zone\_get\_mx
* r53\_zone\_get\_nameservers
* r53\_zone\_get\_records
* r53\_zone\_update\_a
* r53\_zone\_update\_cname
* r53\_zone\_update\_mx
* r53\_zone\_update\_record

#### EC2 Actions

* ec2\_allocate\_address
* ec2\_assign\_private\_ip\_addresses
* ec2\_associate\_address
* ec2\_associate\_address\_object
* ec2\_attach\_network\_interface
* ec2\_attach\_volume
* ec2\_authorize\_security\_group
* ec2\_authorize\_security\_group\_deprecated
* ec2\_authorize\_security\_group\_egress
* ec2\_build\_base\_http\_request
* ec2\_build\_complex\_list\_params
* ec2\_build\_configurations\_param\_list
* ec2\_build\_filter\_params
* ec2\_build\_list\_params
* ec2\_build\_tag\_param\_list
* ec2\_bundle\_instance
* ec2\_cancel\_bundle\_task
* ec2\_cancel\_reserved\_instances\_listing
* ec2\_cancel\_spot\_instance\_requests
* ec2\_close
* ec2\_confirm\_product\_instance
* ec2\_copy\_image
* ec2\_copy\_snapshot
* ec2\_create\_image
* ec2\_create\_key\_pair
* ec2\_create\_network\_interface
* ec2\_create\_placement\_group
* ec2\_create\_reserved\_instances\_listing
* ec2\_create\_security\_group
* ec2\_create\_snapshot
* ec2\_create\_spot\_datafeed\_subscription
* ec2\_create\_tags
* ec2\_create\_volume
* ec2\_delete\_key\_pair
* ec2\_delete\_network\_interface
* ec2\_delete\_placement\_group
* ec2\_delete\_security\_group
* ec2\_delete\_snapshot
* ec2\_delete\_spot\_datafeed\_subscription
* ec2\_delete\_tags
* ec2\_delete\_volume
* ec2\_deregister\_image
* ec2\_describe\_account\_attributes
* ec2\_describe\_reserved\_instances\_modifications
* ec2\_describe\_vpc\_attribute
* ec2\_detach\_network\_interface
* ec2\_detach\_volume
* ec2\_disassociate\_address
* ec2\_enable\_volume\_io
* ec2\_get\_all\_addresses
* ec2\_get\_all\_bundle\_tasks
* ec2\_get\_all\_images
* ec2\_get\_all\_instance\_status
* ec2\_get\_all\_instance\_types
* ec2\_get\_all\_instances
* ec2\_get\_all\_kernels
* ec2\_get\_all\_key\_pairs
* ec2\_get\_all\_network\_interfaces
* ec2\_get\_all\_placement\_groups
* ec2\_get\_all\_ramdisks
* ec2\_get\_all\_regions
* ec2\_get\_all\_reservations
* ec2\_get\_all\_reserved\_instances
* ec2\_get\_all\_reserved\_instances\_offerings
* ec2\_get\_all\_security\_groups
* ec2\_get\_all\_snapshots
* ec2\_get\_all\_spot\_instance\_requests
* ec2\_get\_all\_tags
* ec2\_get\_all\_volume\_status
* ec2\_get\_all\_volumes
* ec2\_get\_all\_zones
* ec2\_get\_console\_output
* ec2\_get\_http\_connection
* ec2\_get\_image
* ec2\_get\_image\_attribute
* ec2\_get\_instance\_attribute
* ec2\_get\_key\_pair
* ec2\_get\_list
* ec2\_get\_object
* ec2\_get\_only\_instances
* ec2\_get\_params
* ec2\_get\_password\_data
* ec2\_get\_path
* ec2\_get\_proxy\_auth\_header
* ec2\_get\_proxy\_url\_with\_auth
* ec2\_get\_snapshot\_attribute
* ec2\_get\_spot\_datafeed\_subscription
* ec2\_get\_spot\_price\_history
* ec2\_get\_status
* ec2\_get\_utf8\_value
* ec2\_get\_volume\_attribute
* ec2\_handle\_proxy
* ec2\_import\_key\_pair
* ec2\_make\_request
* ec2\_modify\_image\_attribute
* ec2\_modify\_instance\_attribute
* ec2\_modify\_network\_interface\_attribute
* ec2\_modify\_reserved\_instances
* ec2\_modify\_snapshot\_attribute
* ec2\_modify\_volume\_attribute
* ec2\_modify\_vpc\_attribute
* ec2\_monitor\_instance
* ec2\_monitor\_instances
* ec2\_new\_http\_connection
* ec2\_prefix\_proxy\_to\_path
* ec2\_proxy\_ssl
* ec2\_purchase\_reserved\_instance\_offering
* ec2\_put\_http\_connection
* ec2\_reboot\_instances
* ec2\_register\_image
* ec2\_release\_address
* ec2\_request\_spot\_instances
* ec2\_reset\_image\_attribute
* ec2\_reset\_instance\_attribute
* ec2\_reset\_snapshot\_attribute
* ec2\_revoke\_security\_group
* ec2\_revoke\_security\_group\_deprecated
* ec2\_revoke\_security\_group\_egress
* ec2\_run\_instances
* ec2\_server\_name
* ec2\_set\_host\_header
* ec2\_set\_request\_hook
* ec2\_skip\_proxy
* ec2\_start\_instances
* ec2\_stop\_instances
* ec2\_terminate\_instances
* ec2\_trim\_snapshots
* ec2\_unassign\_private\_ip\_addresses
* ec2\_unmonitor\_instance
* ec2\_unmonitor\_instances
* ec2\_wait\_for\_state
