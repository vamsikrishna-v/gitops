FROM nginx

COPY server.conf /etc/nginx/conf.d/default.conf

WORKDIR /usr/share/nginx/html
COPY webdir .

CMD sed -i -e 's/$PORT/'"$PORT"'/g' /etc/nginx/conf.d/default.conf && nginx -g 'daemon off;'