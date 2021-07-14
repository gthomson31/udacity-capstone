#Step 1 Pull down the initial nginx base image from dockerhub 
FROM nginx:mainline-alpine

#Step 2 Remove existing configuration
RUN rm /etc/nginx/conf.d/*

#Step 3  Add configuration
COPY hello.conf /etc/nginx/conf.d/

#Step 4  Add index file for website
COPY index.html /usr/share/nginx/html/