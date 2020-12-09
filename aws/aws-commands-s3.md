## Amplify Commands S3  
  
### Command reference  
[AWS Cli](https://docs.aws.amazon.com/cli/latest/index.html)  
  
[AWS Cli S3](https://docs.aws.amazon.com/cli/latest/reference/s3/index.html)  
  
[User Guide](https://docs.aws.amazon.com/cli/latest/userguide/cli-services-s3.html)  
  
[Quick Reference](http://queirozf.com/entries/aws-s3-common-cli-commands-reference)  
  
### Commands  
  
**Buckets**  
  
[s3api](https://docs.aws.amazon.com/cli/latest/reference/s3api/)  
aws s3api list-buckets  
  
#### Repositories  
**basic operations**  
$aws s3 help  
$aws s3 ls  
$aws s3 ls s3://bucket-name  
$aws s3 cp file.txt s3://my-bucket/  
$aws s3 rm s3://my-bucket/path/MyFile2.rtf  
  
##### Sync
**Attempt sync without --delete option - nothing happens**  
$ aws s3 sync . s3://my-bucket/path  
  
**Sync with deletion - object is deleted from bucket**  
$ aws s3 sync . s3://my-bucket/path --delete  
delete: s3://my-bucket/path/MyFile1.txt  
  
**Delete object from bucket**  
$ aws s3 rm s3://my-bucket/path/MySubdirectory/MyFile3.txt  
delete: s3://my-bucket/path/MySubdirectory/MyFile3.txt  
  
**Sync with deletion - local file is deleted**  
$ aws s3 sync s3://my-bucket/path . --delete  
delete: MySubdirectory\MyFile3.txt  
  
**Sync with Infrequent Access storage class**  
$ aws s3 sync . s3://my-bucket/path --storage-class STANDARD_IA