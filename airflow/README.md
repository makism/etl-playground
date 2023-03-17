
Following the instructions from https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html:

```bash
curl -LfO 'https://airflow.apache.org/docs/apache-airflow/2.5.2/docker-compose.yaml'
```

You have to update the env with your user id:
```bash
echo -e "AIRFLOW_UID=$(id -u)" > .env
```

You need to fun this once-time command to initialize the database:
```bash
docker-compose up airflow-init
```

Finally, bring up the service with:
```bash
docker-compose up 
```
