# Go CDK URL opener for awsdynamo with consistency read option.

## DEPRECATION NOTICE
This opener is deprecated.

Please use [Go CDK](https://github.com/google/go-cloud) with consistent_read option which is available from [v0.22.0](https://github.com/google/go-cloud/releases/tag/v0.22.0).

## Usage

### Import
```
import _ "github.com/initig/gocdk_awsdynamo_consistent_read_opener"
```

### URL example (strongly consistent read)
```
crdynamodb://mytable?partition_key=partkey&sort_key=sortkey&consistent_read=true
```
```
crdynamodb://mytable?partition_key=partkey&sort_key=sortkey
```
note: the default value of consistent_read is true, thus if consistent_read is not provided, treat as true.
### URL example (eventually consistent read)
```
crdynamodb://mytable?partition_key=partkey&sort_key=sortkey&consistent_read=false
```
```
dynamodb://mytable?partition_key=partkey&sort_key=sortkey
```
note: we recommend using dynamodb scheme instead using crdynamodb scheme with consistent_read param as false, because which is completely as same as original dynamodb scheme opener.