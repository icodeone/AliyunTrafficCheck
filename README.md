# AliyunTrafficCheck
阿里云cdt流量检测,超过配置流量则关机,下月初开机.
# 食用方法
1.win
1.1下载Release中的AliyunTrafficCheck_win64.zip
1.2.解压后修改appsetting.json中的配置,默认只需要填写"AccessKeyId" ,"AccessKeySecret"
2.linux(arm,amd)
2.1 下载对应版本 `tar zxvf` 进入文件夹 `chmod +x AliyunTrafficCheck` 后`./AliyunTrafficCheck`
3.docker(未测试..)
3.1 ```docker build -t $IMAGE_NAME .```
3.2 ```docker run -d --name $CONTAINER_NAME \
    -e Credentials__AccessKeyId="your_access_key_id" \
    -e Credentials__AccessKeySecret="your_access_key_secret" \
    -e InstanceId="" \
    -e RegionId="cn-hongkong" \
    -e MaxTraffic="180" \
    $IMAGE_NAME```
## TODO
1.linux安装,卸载脚本.