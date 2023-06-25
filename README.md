# caddy-cloudflare
A simple build of Caddy with the Cloudflare DNS mod baked in.

# Example Caddyfile

If you are setting up a Caddyfile, you will need to configure an API token in Cloudflare. Once you have obtained the token, you can inject it via an environment variable as below.
```
*.example.com, example.com {
	tls {
		dns cloudflare {env.CLOUDFLARE_API_TOKEN}
    }
}
```
Alternatively, you can simply paste the token directly into your config like the example below.
```
*.example.com, example.com {
	tls {
		dns cloudflare abcd1234
    }
}
```
Instead of `abcd1234`, simply add your full API token.
