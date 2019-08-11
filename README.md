# Totakoko Infrastructure

This project contains the [compose-deploy](https://github.com/totakoko/compose-deploy) infrastructure running totakoko.com.

Everything runs on a single [Online](https://www.online.net/en/server-dedicated/start-2-l) dedicated server.


## Security

The goal of this repository is to manage all services with git and be as open-source as possible.
Secrets like passwords are not publicly visible and are only defined in the CI system.

If you discover a vulnerability in this repository, please send an email at *security@totakoko.com*.


## CI Variables

These environment variables have been defined in the CI system:
- SSH_HOST
- SSH_FINGERPRINT_BASE64
- SSH_PRIVATE_KEY_BASE64
- cd_mealplanner_couchdb_COUCHDB_PASSWORD
- cd_mealplanner_couchdb_COUCHDB_USER
- cd_mealplanner_server_MP_COUCHDB_PASSWORD
- cd_mealplanner_server_MP_COUCHDB_USER
- cd_netdata__BASIC_AUTH
- cd_wekan_wekan_MAIL_FROM
- cd_wekan_wekan_MAIL_URL
