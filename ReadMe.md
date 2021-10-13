# My personal blog and website

I wanted a minimalist blog engine, so I choose ghost.

I created my own theme, available in ./theme.

## Architecture

This project is composed of:
- A regular ghost hosting (official Docker image, untouched)
- A nginx reverse proxy to provide a SSL connection (official nginx image, with custom config)
- A custom and minimalist ghost theme, composed of only two page templates (home page and post)

The SSL certificates are self-signed, and will allow you to serve your app in https only in local.

## Run

Here is the .env template that I use:
```sh
url=https://tommarx.dev # tommarx.dev is redirected to localhost on my computer
NODE_ENV=development
```

And to launch:
```sh
docker-compose up [-d]
```