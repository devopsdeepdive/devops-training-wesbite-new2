# Darvisha Technologies website

Static website package: `index.html`, `styles.css`, and `script.js`.

## Deploy to Ubuntu EC2 with Nginx

Copy these three files into your website directory (example: `/var/www/devopsdeepdive/`). Then run:

```bash
sudo chown -R www-data:www-data /var/www/devopsdeepdive
sudo find /var/www/devopsdeepdive -type d -exec chmod 755 {} \;
sudo find /var/www/devopsdeepdive -type f -exec chmod 644 {} \;
```

No Nginx restart is normally required for static HTML/CSS/JS changes. Refresh the browser with `Ctrl+F5`.

## Before publishing

- Confirm `info@darvishatech.com` is the correct company email.
- Replace the sample phone number `+91 98765 43210` and WhatsApp URL if needed.
- Replace social links currently set to `#` with the company's real Telegram, YouTube, LinkedIn and GitHub URLs.
- The registration form is an embedded Google Form. Keep the current form URL if it is the correct form.
