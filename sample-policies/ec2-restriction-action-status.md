# RDS Actions and Status

## Works

```bash
aws ec2 run-instances \
--image-id ami-0dff809ca5daa2937 \
--count 1  \
--instance-type t3.nano \
--key-name keyname \
--subnet-id subnet-22222222 \
--associate-public-ip-address \
--security-group-ids sg-ddddddd \
--profile profilename \
--region ap-southeast-2 \
--dry-run


aws ec2 run-instances \
--image-id ami-0d692d1b5e7f63b6a \
--count 1  \
--instance-type t3.nano \
--key-name keyname \
--subnet-id subnet-22222222 \
--associate-public-ip-address \
--security-group-ids sg-ddddddd \
--profile profilename \
--region ap-southeast-2 \
--dry-run

#### Works for non io1 and st1 volumes

aws ec2 run-instances \
--image-id ami-0dff809ca5daa2937 \
--count 1  \
--instance-type t3.nano \
--key-name keyname \
--subnet-id subnet-22222222 \
--associate-public-ip-address \
--block-device-mappings file:///Users/keynamek/Desktop/mapping.json \
--security-group-ids sg-ddddddd \
--profile profilename \
--region ap-southeast-2 \
--dry-run
```

## Fails

```bash
aws ec2 run-instances \
--image-id ami-08bd00d7713a39e7d \
--count 1  \
--instance-type t3.nano \
--key-name keyname \
--subnet-id subnet-22222222 \
--associate-public-ip-address \
--security-group-ids sg-ddddddd \
--profile profilename \
--region ap-southeast-2 \
--dry-run

aws ec2 run-instances \
--image-id ami-0d692d1b5e7f63b6a \
--count 1  \
--instance-type t3.large \
--key-name keyname \
--subnet-id subnet-22222222 \
--associate-public-ip-address \
--security-group-ids sg-ddddddd \
--profile profilename \
--region ap-southeast-2 \
--dry-run

#### Fails on io1 and st1 volumes

aws ec2 run-instances \
--image-id ami-0dff809ca5daa2937 \
--count 1  \
--instance-type t3.nano \
--key-name keyname \
--subnet-id subnet-22222222 \
--associate-public-ip-address \
--block-device-mappings file:///Users/keynamek/Desktop/mapping.json \
--security-group-ids sg-ddddddd \
--profile profilename \
--region ap-southeast-2 \
--dry-run
```