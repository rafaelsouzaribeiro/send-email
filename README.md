<h1>How to use?</h1>

```go
loginauth "github.com/rafaelsouzaribeiro/send-email/pkg/login-auth"

auth := loginauth.LoginAuth("email", "password")
	subject := "Subject: Test Email from Go\n"
	body := "This is a test email message from Go.\n"
	msg := []byte(subject + "\n" + body)

	err := smtp.SendMail("smtp-mail.outlook.com:25", auth, "fromemail", []string{"rafaelribeirosouza86@hotmail.com"}, msg)

	if err != nil {
		panic(err)
	}

	fmt.Println("Email successfully sent!")
```
