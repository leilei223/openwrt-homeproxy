# openwrt-homeproxy
### 1、将基础配置文件“homeproxy无订阅自行添加”下载到本地，重命名为“homeproxy”
### 2、通过ssh连接openwrt，并将homeproxy上传至/etc/config 文件目录下，
### 3、进入openwrt 服务目录下打开 homeproxy  添加订阅 即可正常使用这个配置模板， 分流超级精细和精准。
### 4、使用前，请进入Ruleset settings 查看geosite-claude goesite-facebook goeip-facebook 规则文件，请到https://github.com/SagerNet/sing-geosite/blob/rule-set/geosite-115.srs 去下载 或者自行添加goesite/goeip连接（claude 输入anthropic 来添加查询，facebook 就直接输入facebook就行），这两个我是无法通过二进制的连接使用的 因此我是把相应的 .srs文件下载到本地使用的，下载后放置到/etc/homeproxy/ruleset文件目录下，若不需要这个规则 请在 ## Ruleset settings 下手动删除geosite-claude goesite-facebook goeip-facebook ，并到 ## 路由规则  下删除对应的规则。
