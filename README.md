# AliyunTrafficCheck
阿里云cdt流量检测,超过配置流量则关机,下月初开机.
# 食用方法
### win 

 下载Release中的AliyunTrafficCheck_win64.zip

 解压后修改appsetting.json中的配置,默认只需要填写"AccessKeyId" ,"AccessKeySecret"

### linux(arm,amd)

 下载对应版本 `tar zxvf` 进入文件夹 `chmod +x AliyunTrafficCheck` 后`./AliyunTrafficCheck`

### docker(未测试..)

  ```docker build -t $IMAGE_NAME .```

  ``` docker run -d --name $CONTAINER_NAME \
    -e Credentials__AccessKeyId="your_access_key_id" \
    -e Credentials__AccessKeySecret="your_access_key_secret" \
    -e InstanceId="" \
    -e RegionId="cn-hongkong" \
    -e MaxTraffic="180" \
    $IMAGE_NAME ```

## TODO
1.linux安装,卸载脚本.
