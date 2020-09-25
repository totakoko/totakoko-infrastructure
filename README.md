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
- SSH_PORT
- SSH_FINGERPRINT_BASE64
- SSH_PRIVATE_KEY_BASE64
- cd_gitlab__DB_PASS
- cd_gitlab_gitlab_SMTP_USER
- cd_gitlab_gitlab_SMTP_PASS
- cd_gitlab_gitlab_GITLAB_SECRETS_DB_KEY_BASE
- cd_gitlab_gitlab_GITLAB_SECRETS_SECRET_KEY_BASE
- cd_gitlab_gitlab_GITLAB_SECRETS_OTP_KEY_BASE
- cd_mealplanner_couchdb_COUCHDB_PASSWORD
- cd_mealplanner_couchdb_COUCHDB_USER
- cd_mealplanner_server_MP_COUCHDB_PASSWORD
- cd_mealplanner_server_MP_COUCHDB_USER
- cd_netdata__BASIC_AUTH
- cd_nextcloud_db_MYSQL_PASSWORD
- cd_nextcloud_db_MYSQL_ROOT_PASSWORD
- cd_nextcloud_nextcloud_MYSQL_PASSWORD
- cd_nextcloud_nextcloud_NEXTCLOUD_ADMIN_PASSWORD
- cd_wekan_wekan_MAIL_FROM
- cd_wekan_wekan_MAIL_URL


## Additional settings

- SSH port was changed from 22 to 2222, so that it does not conflict with GitLab.
- Docker login with registry.totakoko.com


### Nextcloud configuration

Since a change in Nextcloud 17, the configuration `'overwriteprotocol' => 'https'` must be added into `/srv/data/nextcloud/app/config/config.php`. (see [issue](https://github.com/nextcloud/server/issues/17409#issuecomment-538684976))

