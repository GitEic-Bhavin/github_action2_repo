FROM nginx

RUN apt-get update && apt-get upgrade -y && apt-get install npm -y
# RUN apt-get install npm -y
COPY nginx.conf /etc/nginx/nginx.conf

COPY package*.json /etc/nginx/
COPY . /etc/nginx/

WORKDIR /etc/nginx/
RUN npm install
# RUN npm start

EXPOSE 80

CMD service nginx start && node index.js

# Here, First nginx should start before start nodjs app by, node index.js, otherwise you will unable to connect to server.

# but, by this , only node index.js is running not nginx.
# CMD ["nginx", "-g", "daemon off;"]
# ENTRYPOINT ["node", "index.js"]



