- 将`access_key_id/access_key_secret/endpoint/bucket`等信息写入到`/etc/environment/`文件中

```bash
ali_key="your_ali_oss_access_key"
ali_secret="your_ali_oss_access_secret"
ali_endpoint="your_ali_oss_endpoint"
ali_bucket="your_ali_oss_bucket_name"

```

- 保存后**注销重登陆**,使环境变量永久生效 