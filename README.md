# Running in Production

* **Before running the container in production, edit `init.sh` and remove logging of sensitive data (username, password)**



# Q&A

* **How to check if the RabbitMQ is running OK?**. It is best to hit `http://localhost:15672` on the browser of our choice. We should see a login page. Provide `guest` for both username and password and hit Login.



# Troubleshooting

* **Permissions issue**. If you get permissions error when spinning up the RabbitMQ container, your should fix the permissions on your local `rabbitmq_log` directory: `sudo chmod 666 -R rabbitmq_log/`. (Or better (if not in production) just delete those directories, Docker will recreate them after restart.)

  This directory is set up in `volumes` section of `docker-compose.yml` to store the volume data and is automatically created after the very first execution of `docker-compose up rabbitmq`.
