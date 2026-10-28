# Darvisha Technologies — DevOps DeepDive website

## Package contents
- `index.html` — website HTML with Darvisha Technologies branding
- `styles.css` — website styles
- `script.js` — navigation and page interactions
- `images/darvisha-mark.png` — supplied blue cloud D logo, used in the header beside the company name
- `images/darvisha-technologies-logo.png` — supplied full Darvisha Technologies logo, used in the footer

The two logo image files are copied from the images supplied by the site owner; they have not been redesigned.

## Deploy to the existing Ubuntu/Nginx website
Back up the live website first, then copy the contents of this package into `/var/www/devopsdeepdive/`, preserving the `images/` directory.

Example, if the extracted package folder is in `/home/ubuntu/darvisha-website-package`:

```bash
sudo cp -a /var/www/devopsdeepdive /var/www/devopsdeepdive-backup-$(date +%Y%m%d-%H%M%S)
sudo cp /home/ubuntu/darvisha-website-package/index.html /var/www/devopsdeepdive/index.html
sudo cp /home/ubuntu/darvisha-website-package/styles.css /var/www/devopsdeepdive/styles.css
sudo cp /home/ubuntu/darvisha-website-package/script.js /var/www/devopsdeepdive/script.js
sudo mkdir -p /var/www/devopsdeepdive/images
sudo cp /home/ubuntu/darvisha-website-package/images/* /var/www/devopsdeepdive/images/
sudo chown -R www-data:www-data /var/www/devopsdeepdive
sudo find /var/www/devopsdeepdive -type d -exec chmod 755 {} \;
sudo find /var/www/devopsdeepdive -type f -exec chmod 644 {} \;
```

Then refresh the site with `Ctrl+F5`. This package does not change the live site until you deploy it.
