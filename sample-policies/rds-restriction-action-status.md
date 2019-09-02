# RDS Actions and Status

## Works

```bash
aws rds create-db-instance \
    --allocated-storage 20 --db-instance-class db.t3.micro \
    --db-instance-identifier test-instance \
    --engine mysql \
    --enable-cloudwatch-logs-exports '["audit","error","general","slowquery"]' \
    --master-username master \
    --master-user-password secret99
```

## Fails

```bash
aws rds create-db-instance \
    --allocated-storage 120 --db-instance-class db.t3.micro \
    --db-instance-identifier test-instance1 \
    --engine mysql \
    --enable-cloudwatch-logs-exports '["audit","error","general","slowquery"]' \
    --master-username master \
    --master-user-password secret99

aws rds create-db-instance \
    --allocated-storage 20 --db-instance-class db.t3.large \
    --db-instance-identifier test-instance1 \
    --engine mysql \
    --enable-cloudwatch-logs-exports '["audit","error","general","slowquery"]' \
    --master-username master \
    --master-user-password secret99

aws rds create-db-instance \
    --allocated-storage 20 --db-instance-class db.t3.micro \
    --db-instance-identifier test-instance \
    --engine oracle-se \
    --enable-cloudwatch-logs-exports '["audit","error","general","slowquery"]' \
    --master-username master \
    --master-user-password secret99

aws rds create-db-instance \
    --allocated-storage 20 --db-instance-class db.t3.micro \
    --db-instance-identifier test-instance \
    --engine sqlserver-ee \
    --enable-cloudwatch-logs-exports '["audit","error","general","slowquery"]' \
    --master-username master \
    --master-user-password secret99


aws rds create-db-instance \
    --allocated-storage 20 --db-instance-class db.t3.micro \
    --db-instance-identifier test-instance \
    --engine mysql \
    --enable-cloudwatch-logs-exports '["audit","error","general","slowquery"]' \
    --master-username master \
    --master-user-password secret99 \
    --multi-az

aws rds create-db-instance \
    --allocated-storage 20 --db-instance-class db.t3.micro \
    --db-instance-identifier test-instance \
    --engine mysql \
    --enable-cloudwatch-logs-exports '["audit","error","general","slowquery"]' \
    --master-username master \
    --master-user-password secret99 \
    --iops 300
```