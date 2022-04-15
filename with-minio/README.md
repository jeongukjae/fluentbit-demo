# Run fluent bit with minio

```sh
$ docker compose up # open localhost:9000 in the web browser and create "sample-bucket" bucket.
[+] Running 2/0
 ⠿ Container with-minio-minio-1       Created                                                                                                    0.0s
 ⠿ Container with-minio-fluent-bit-1  Created                                                                                                    0.0s
Attaching to with-minio-fluent-bit-1, with-minio-minio-1
with-minio-minio-1       | API: http://172.19.0.2:9000  http://127.0.0.1:9000
with-minio-minio-1       |
with-minio-minio-1       | Console: http://172.19.0.2:9001 http://127.0.0.1:9001
with-minio-minio-1       |
with-minio-minio-1       | Documentation: https://docs.min.io
with-minio-minio-1       | Finished loading IAM sub-system (took 0.0s of 0.0s to load data).
with-minio-fluent-bit-1  | Fluent Bit v1.9.2
with-minio-fluent-bit-1  | * Copyright (C) 2015-2022 The Fluent Bit Authors
with-minio-fluent-bit-1  | * Fluent Bit is a CNCF sub-project under the umbrella of Fluentd
with-minio-fluent-bit-1  | * https://fluentbit.io
with-minio-fluent-bit-1  |
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [fluent bit] version=1.9.2, commit=27a63c11d3, pid=1
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [storage] version=1.1.6, type=memory+filesystem, sync=normal, checksum=disabled, max_chunks_up=128
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [storage] backlog input plugin: storage_backlog.1
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [cmetrics] version=0.3.0
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [input:storage_backlog:storage_backlog.1] queue memory limit: 95.4M
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [output:s3:s3.0] Using upload size 1000000 bytes
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [output:s3:s3.0] total_file_size is less than 10 MB, will use PutObject API
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [sp] stream processor started
with-minio-fluent-bit-1  | [2022/04/15 08:54:03] [ info] [output:s3:s3.0] worker #0 started
with-minio-fluent-bit-1  | [2022/04/15 08:54:15] [ info] [output:s3:s3.0] upload_timeout reached for dummy.0
with-minio-fluent-bit-1  | [2022/04/15 08:54:15] [ info] [output:s3:s3.0] Successfully uploaded object /sample-log/2022/04/15/08/04/04/1YoMBhmq.gz
with-minio-fluent-bit-1  | [2022/04/15 08:54:27] [ info] [output:s3:s3.0] upload_timeout reached for dummy.0
with-minio-fluent-bit-1  | [2022/04/15 08:54:27] [ info] [output:s3:s3.0] Successfully uploaded object /sample-log/2022/04/15/08/04/16/S92UQcw4.gz
```

## Sample log file

```json
{"date":"2022-04-15T08:54:51.687162Z","message":"dummy"}
{"date":"2022-04-15T08:54:52.687158Z","message":"dummy"}
{"date":"2022-04-15T08:54:53.687180Z","message":"dummy"}
{"date":"2022-04-15T08:54:54.687181Z","message":"dummy"}
{"date":"2022-04-15T08:54:55.687165Z","message":"dummy"}
{"date":"2022-04-15T08:54:56.687153Z","message":"dummy"}
{"date":"2022-04-15T08:54:57.687179Z","message":"dummy"}
{"date":"2022-04-15T08:54:58.687165Z","message":"dummy"}
{"date":"2022-04-15T08:54:59.687168Z","message":"dummy"}
{"date":"2022-04-15T08:55:00.687170Z","message":"dummy"}
{"date":"2022-04-15T08:55:01.687177Z","message":"dummy"}
{"date":"2022-04-15T08:55:02.687173Z","message":"dummy"}
```
