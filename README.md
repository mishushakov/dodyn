# DoDyn

Simple One-Line shell script to update your DNS records with DigitalOcean API, that makes use of ipify.org API to retrieve your IP.

# Dependencies

- curl

## Installation

1. Connect your Domain to DigitalOcean DNS
2. Set the `DODYN_DOMAIN` Environment Variable to your root Domain (not a subdomain!), example: `ushakov.co`
3. Get a Personal Access token on [API Page](https://cloud.digitalocean.com/account/api) and set the `DODYN_TOKEN` Environment Variable
4. Find out your Record ID ([guide](https://developers.digitalocean.com/documentation/v2/#list-all-domain-records)) and set the `DODYN_RECORD` Environment Variable
5. Make sure the script is executable, if not `chmod +x dodyn.sh`
6. Test the script manually, the output should be like this: ![](https://i.imgur.com/rJy2bwZ.png)
7. Set up a cronjob to automatically update your record each 30 minutes (recommended amount of time) `*/30 * * * * dodyn.sh`
8. (When running at home) Make sure your ports are open

Thank you.