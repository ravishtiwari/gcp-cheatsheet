# GSUtil Cheat Sheet 

## Bucket Operations
| gsutil Command | Description |
| ------ | ------ |
| mb | Make Bucket or create bucket |
| cp | Copy object(s) to and from Storage bucket |
| mv | Move/Rename object(s) to and from Storage bucket |
| rm | Remove bucket/bucket objects|
| ls | list bucket contents |

### Create a Bucket
> gsutil mb -p <project_id> -c <class> -l <localtion> -b <bucket_acl> gs://<bucket_name>/

*Example*
-- Creating a multi regional bucket with default options:
```sh
$ gsutil mb  -p my-gcp-project gs://gcp-storage-demo-test0/
```

-- Creating a regional bucket in **Mumbai** region with bucket acl turned off:
```sh
$ gsutil mb -p my-gcp-project -c regional -l asia-south1 -b off gs://g-cloud-storage/
```

-- Creating a regional bucket in **Mumbai** region with bucket acl turned off and 6 month retention of uploaded:
```sh
$ gsutil mb -p my-gcp-project -c regional --retention 6m -l asia-south1 -b off gs://g-cloud-storage/
```
