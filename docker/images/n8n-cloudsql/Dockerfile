FROM n8nio/n8n

# Download proxy
RUN wget "https://storage.googleapis.com/cloudsql-proxy/v1.21.0/cloud_sql_proxy.linux.amd64" -O /cloud_sql_proxy
RUN chmod +x /cloud_sql_proxy

COPY docker-entrypoint.sh /docker-entrypoint.sh
RUN chmod +x /docker-entrypoint.sh

ENTRYPOINT ["tini", "--", "/docker-entrypoint.sh"]

EXPOSE 5678/tcp