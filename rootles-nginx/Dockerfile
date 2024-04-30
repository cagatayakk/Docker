FROM nginx
RUN usermod -aG tty nginx
RUN chown -R nginx:nginx  /var/cache/nginx
COPY nginx.conf /etc/nginx/nginx.conf
USER nginx