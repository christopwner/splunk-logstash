# splunk-logstash
Example docker compose configuration for Logstash with Splunk.

## how to use
Run with:

`# docker-compose up`

Appended to `app.log` to test logging to splunk:

`tail -n1 app.log >> app.log`
