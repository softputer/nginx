# Nginx

### Supported Nginx versions

You can changed the nginx version just by changing the ENV NGINX_VERSION to the your desired version.

### How to use this image

This image is simply a base image for you.  There are several ways for you to get started.

#### Create a `Dockerfile`

```dockerfile
FROM softputer/nginx
COPY nginx.conf /etc/nginx/nginx.conf
CMD ["nginx"]
```

Above is the simplest method to use this image. But in reality, sometimes nginx is dynamically generated, you have to reload nginx.conf every certain time. This is controlled by your program which is executed when your image is started.

For example: your program is a binary named controller.

```reload
FROM softputer/nginx
COPY controller /
CMD ["/controller"]
```

#### Attention

If you have any questions about the usage of this image or the configuration of nginx, you can contact my by email: gyj3023@foxmail.com.
