# splunk-logstash
Example docker compose configuration for Logstash with Splunk.

## how to use
Run with:

`# docker-compose up`

Append to `app.log` to test logging to splunk:

`tail -n1 app.log >> app.log`

Navigate to https://localhost:8000 to view splunk deployment and logs. The password for `admin` login is in the `.env` file.

## caveat
Be aware of possible permission issues with the `settings/filebeats.yml` file. Requires `root` ownership and owner/group write only. That can be setup with following:

* `# chown root settings/filebeats.yml`
* `# chmod go-w settings/filebeats.yml`

See https://www.elastic.co/guide/en/beats/libbeat/current/config-file-permissions.html for more info.
