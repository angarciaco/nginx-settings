# nginx-settings
Settings for http and server block in Nginx. This is for Drupal, Symfony and some anothers.

## Security

Enable / uncomment line for don't sending header version of server:

```sh
server_tokens off;
```

If we have installed nginx using apt-get in Debian or Ubuntu, we might need to install the package nginx-extras to set or clear "Server" header.

Once this is done, we can add the lines below in nginx.conf (usually /etc/nginx/nginx.conf) into http{ ... }:

So, to clear the "Server" header altogether:

```sh
more_clear_headers Server; 
```

And, to Set a custom string as "Server":

```sh
more_set_headers 'Server: some-string-here';
```

By @angarciaco
