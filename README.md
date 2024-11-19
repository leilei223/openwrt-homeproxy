# openwrt-homeproxy精细分流配置文件
#### 1、将基础配置文件“homeproxy无订阅自行添加”下载到本地，重命名为“homeproxy”
#### 2、通过ssh连接openwrt，并将homeproxy上传至/etc/config 文件目录下，
#### 3、进入openwrt 服务目录下打开 homeproxy  自行添加机场订阅即可
#### 4、使用前，请进入Ruleset settings 查看geosite-claude goesite-facebook goeip-facebook 规则文件，请到https://github.com/SagerNet/sing-geosite/blob/rule-set/geosite-115.srs 去下载 或者自行添加goesite/goeip连接（claude 输入anthropic 来添加查询，facebook 就直接输入facebook就行），这两个我是无法通过二进制的连接使用的 因此我是把相应的 .srs文件下载到本地使用的，下载后放置到/etc/homeproxy/ruleset文件目录下，![image](https://github.com/user-attachments/assets/b9e10182-5853-41c1-88b5-4dd6dc91b2fa)

若不需要这个规则 请在 ## Ruleset settings下手动删除geosite-claude goesite-facebook goeip-facebook ，![image](https://github.com/user-attachments/assets/e0249ecd-e102-4f1f-b1f4-7c87db3590a6)
![image](https://github.com/user-attachments/assets/90d6c99c-2c64-48b6-b192-7f2ac8b1838a)


并到 ## 路由规则  下删除对应的 claude:goesite 和 facebook:goesite&goeip。
![image](https://github.com/user-attachments/assets/94a73ac4-5580-4648-8b9a-f59e2339bcf7)
![image](https://github.com/user-attachments/assets/2d67bbfa-3c2b-4425-b721-40993de07420)
#### 5、配置好后即可正常使用这个配置模板，全自动，分流超级精细和精准。
