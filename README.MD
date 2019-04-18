### 非常简单的阿里云OSS文件上传

- 将`access_key_id/access_key_secret/endpoint/bucket`等信息写入到`/etc/environment/`文件中

```bash
ali_key="your_ali_oss_access_key"
ali_secret="your_ali_oss_access_secret"
ali_endpoint="your_ali_oss_endpoint"
ali_bucket="your_ali_oss_bucket_name"

```

- 保存后**注销重登陆**,使环境变量永久生效

- 下载并给予可执行权限
```bash
wget https://raw.githubusercontent.com/Humsan/simple_ali_upload/master/ali-oss-upload -O "ali_upload"

sudo chmod +x ali_upload
```

- 方便使用可以**mv**到用户自定义可执行程序目录下
```bash
mv ali_upload /usr/local/bin/ali_upload
```
- 使用方法
```bash
# upload_file : 你需要上传的文件(根据官方要求,不得大于5G)
# save_object : 在OSS上保存为'save_object'名
ali_upload upload_file [save_object]
```



- references
    - [PutObject](https://help.aliyun.com/document_detail/31978.html?spm=a2c4g.11186623.6.1127.60d9734csPYp3D)
    - [aliyun-oss-php-sdk](https://github.com/aliyun/aliyun-oss-php-sdk/blob/master/src/OSS/OssClient.php?spm=a2c4g.11186623.2.17.c31c734cUSWaD9)