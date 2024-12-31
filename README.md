## Cloudflare API v4 

### Dynamic DNS Update in Bash, without unnecessary requests

### 食用：

    wget --no-check-certificate https://raw.githubusercontent.com/Huiaini/cloudflare-api-v4-ddns/master/cf-v4-ddns.sh
    
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
    
#### Srart
 
    bash cf-v4-ddns.sh
    
#### Cron Scheduled tasks

    echo '*/5 * * * * bash /root/cf-v4-ddns.sh' >>/var/spool/cron/root
    
#### You need to push the IP to Cloudflare every time you run it. Use the vi command to modify line 45.

    FORCE=true

#### You can use it happily.
    
## Thank [YuLeWang]（https://github.com/yulewang） Provide Script.
