# LocalStack Docker Sample

## Run

```bash
# show config
docker-compose run --rm aws-cli aws configure list

# make bucket
docker-compose run --rm aws-cli s3 mb s3://sample-bucket --endpoint-url=http://localstack:4566

# show bucket list
docker-compose run --rm aws-cli s3api list-buckets --endpoint-url=http://localstack:4566

# cp file to bucket
docker-compose run --rm aws-cli s3 cp sample.txt s3://sample-bucket/sample-dir/ --endpoint-url=http://localstack:4566

# ls files in bucket
docker-compose run --rm aws-cli s3 ls s3://sample-bucket/sample-dir/ --endpoint-url=http://localstack:4566
```

## Explorer

- [health](http://localhost:4566/health)
- [sample-bucket files](http://localhost:4566/sample-bucket)
