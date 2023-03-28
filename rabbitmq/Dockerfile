FROM rabbitmq:3-management-alpine

ADD init.sh /init.sh
RUN chmod +x /init.sh
EXPOSE 15672

# Define default command
CMD ["/init.sh"]
