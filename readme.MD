### create service account
```
eksctl create iamserviceaccount \
--cluster=$CLUSTER_NAME \
--namespace=roboshop \
--name=aws-secret-reader \
--attach-policy-arn=arn:aws:iam::$ACC_ID:policy/roboshopmysqlsecretReader \
--override-existing-serviceaccounts \
--region $REGION_CODE \
--approve
```