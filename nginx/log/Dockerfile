nginx:
    image: nginx
    ports:
      - "80:80"
    volumes:
      - ./nginx/nginx.conf:/etc/nginx/nginx.conf
      - ./nginx/log:/var/log/nginx
    depends_on:
      - spring-app
    networks:
      - elk