#Step 1 Pull down the initial nginx base image from dockerhub 
FROM nginx:mainline-alpine

#Step 2 Remove existing configuration
RUN rm /etc/nginx/conf.d/*

#Step 3  Add configuration
COPY ~/project/nginx_app/hello.conf /etc/nginx/conf.d/

#Step 4  Add index file for website
COPY ~/project/nginx_app/index.html /usr/share/nginx/html/

## Step 5:
# Expose port 80
EXPOSE 80
