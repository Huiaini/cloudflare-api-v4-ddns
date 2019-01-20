## Cloudflare API v4 

### Dynamic DNS Update in Bash, without unnecessary requests

### 食用：

    wget -N --no-check-certificate "https://raw.githubusercontent.com/Huiaini/cloudflare-api-v4-ddns/master/cf-v4-ddns.sh
    chmod +x cf-v4-ddns.sh
    
#### 配置
    
    vim cf-v4-ddns.sh
    
 API key, see https://www.cloudflare.com/a/account/my-account
 
    CFKEY= （Cloudflare 账号KEY）
    
 Username, eg: user@example.com
 
    CFUSER=（Cloudflare 邮箱）
    
 Zone name, eg: example.com  
 
    CFZONE_NAME=（Cloudflare 主域名）
    
 Hostname to update, eg: homeserver.example.com
 
    CFRECORD_NAME=（Cloudflare 二级域名）
    
#### 运行
 
    bash cf-v4-ddns.sh
    
#### Cron定时任务

echo  '*/5 * * * * bash /root/cf-v4-ddns.sh ' >>/var/spool/cron/root

#### 就能愉快的使用了
    
## 感谢 [yulewang]（https://github.com/yulewang?tab=repositories） 提供脚本
