# Go SMTP

> Go 语言 SMTP 邮件发送模块


## 使用示例

```go
package main

import "github.com/oyps/gosmtp"

func main() {
	gosmtp.SendSmtp(gosmtp.SmtpOption{
		Host:        "smtp.exmail.qq.com",
		Port:        465,
		Username:    "example@example.com",
		Password:    "",
		Nick:        "xxx 邮件服务",
		Subject:     "来自 xxx 的验证码",
		Body:        "您的验证码是 666666，请及时登录使用",
		From:        "example@example.com",
		To:          []string{"example@163.com"},
		ContentType: "text/html; charset=utf-8",
	})
}
```