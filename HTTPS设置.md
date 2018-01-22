HTTPS设置
#### 基于以下环境配置    
服务器类型：阿里云轻量应用服务器    
证书类型：   

厂商 | 证书类型 | 到期时间
---- | ---- | -------
腾讯云|TrustAsia TLS RSA CA(1年)|2019-01-12 20:00:00


#### 安装OpenSSL模块
```
yum install mod_ssl openssl
```


#### 证书文件
下载并解压证书文件，Apache证书文件如下（PEM编码）：

- www.developboot.com.csr   
- 1_root_bundle.crt     
- 2_www.developboot.com.crt     
- 3_www.developboot.com     

1_root_bundle.crt 文件包括一段证书代码 “-----BEGIN CERTIFICATE-----”和“-----END CERTIFICATE-----”,
2_www.domain.com_cert.crt 文件包括一段证书代码 “-----BEGIN CERTIFICATE-----”和“-----END CERTIFICATE-----”,
3_www.domain.com.key 文件包括一段私钥代码“-----BEGIN RSA PRIVATE KEY-----”和“-----END RSA PRIVATE KEY-----”。
www.developboot.com.csr 证书请求

将证书放在指定的路径

证书名称 | 路径
----|----
1_root_bundle.crt | /usr/local/apache/conf
2_www.developboot.com.crt | /usr/local/apache/conf
3_www.developboot.com.key | /usr/local/apache/conf

#### 证书安装
1. 编辑Apache根目录下 conf/httpd.conf 文件，
找到 #LoadModule ssl_module modules/mod_ssl.so 和 #Include conf/extra/httpd-ssl.conf，去掉前面的#号注释；
2. 编辑Apache根目录下 conf/extra/httpd-ssl.conf 文件，修改如下内容：
```
<VirtualHost _default_:443>
    DocumentRoot "/home/www/htdocs"
    ServerName www.developboot.com:443
    SSLEngine on
    SSLCertificateFile /usr/local/apache/conf/2_www.developboot.com.crt
    SSLCertificateKeyFile /usr/local/apache/conf/3_www.developboot.com.key
    SSLCertificateChainFile /usr/local/apache/conf/1_root_bundle.crt
</VirtualHost>
```

**DocumentRoot**的路径是WordPress的安装路径。直接访问WordPress。
**DocumentRoot**的路径可以参考`conf/httpd.conf`文件中的**DocumentRoot**与其一直。

3. 重启Apache 
```
/usr/local/apache/bin/apachectl restart
```

配置完成后，重新启动 Apache 就可以使用https://www.developboot.com来访问了。


#### WordPress设置
控制台->设置     
将修改下面选项：

WordPress地址（URL）https://www.developboot.com     
站点地址（URL）     https://www.developboot.com







