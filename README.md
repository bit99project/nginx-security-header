# nginx-security-header

```
##Common headers for security
add_header Feature-Policy "geolocation none;midi none;notifications none;push none;sync-xhr none;microphone none;camera none;magnetometer none;gyroscope none;speaker self;vibrate none;fullscreen self;payment none;";

##HSTS
add_header Strict-Transport-Security "max-age=31536000; includeSubdomains; preload";
## 只允许本站用 frame 来嵌套
add_header X-Frame-Options "SAMEORIGIN";
##允许https访问default-src *.xx.com https
add_header Content-Security-Policy "default-src *.xx.com https: wss: data: 'unsafe-inline' 'unsafe-eval' always";
## XSS 保护
add_header X-Xss-Protection "1; mode=block";
## 禁止嗅探文件类型
add_header X-Content-Type-Options "nosniff";
add_header Referrer-Policy "strict-origin-when-cross-origin";

```
