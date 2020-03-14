---
description: Follow this guide to send e-mails like "Forgot password" mails.
---

# Setup E-mail \(optional\)

## SMTP

The easiest solution to send mails with Dopenote is to use SMTP. 

{% hint style="info" %}
Notice, if you use `MAIL_PASSWORD` you should add this value to your `.env` file and then use ${MAIL\_PASSWORD} in the `docker-compose.yml` file, in case you want to save the docker-compose to a git repository \(also remember to gitignore the `.env` file\)
{% endhint %}

Add this to your `docker-compose.yml` file, below the `DB_PASSWORD` environment variable.

```text
    environment:
      - MAIL_DRIVER=smtp
      - MAIL_HOST=12.345.67.89
      - MAIL_FROM_ADDRESS=noreply@example.com
      - MAIL_PORT=25
      - MAIL_ENCRYPTION=null
      - MAIL_USERNAME=
      - MAIL_PASSWORD=${MAIL_PASSWORD}
```

### Troubleshooting

If  your emails doesnt get send you can check your log in the `web` container in the file `/app/storage/logs/laravel-{DATE}.log`

