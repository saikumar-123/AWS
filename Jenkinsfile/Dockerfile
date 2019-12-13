FROM docker-registry.ose.com/ocp-image/nginx:latest
ARG nginx_folder
ARG GIT_COMMIT
ENV TZ=America/New_York
LABEL revision=${GIT_COMMIT} 

USER root
RUN chmod -R 777 $HOME
RUN mv /etc/opt/rh/rh-nginx112/nginx/nginx.conf /etc/opt/rh/rh-nginx112/nginx/nginx.conf.bkp
COPY ./nginx/${nginx_folder}/nginx.conf  /etc/opt/rh/rh-nginx112/nginx/nginx.conf
# COPY ./nginx/${nginx_folder}/nginx-proxy.conf  /opt/app-root/etc/nginx.default.d/nginx-proxy.conf
USER 1001
