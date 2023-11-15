# Simple Push Notifications

Simple push notifications for testing purposes

## Starting

1. To serve an application with `Service Worker`s, [one needs to have SSL or use localhost](https://stackoverflow.com/questions/52299246/cant-find-serviceworker-in-navigator-anymore).
So start by generating self-signed SSL keys and certificates.

```
openssl req -new -x509 -keyout key.pem -out cert.pem -days 365 -nodes
```

2. Then serve
```
python https-server.py
```

3. After that, go to `https://localhost:4443`. Note the '**https**'

## iOS devices

Push notifications work as PWAs, so you need to open safari and `Share > Add to Home Screen`.

## Untrusted Warning

You'd need a ca-signed certificate to get rid of the untrusted warning in the browser.

## Credits
- Forked from [Algoritm211](https://github.com/Algoritm211/test-push-notifications-pwa)
- Https python script based on [DannyHinshaw](https://gist.github.com/DannyHinshaw/a3ac5991d66a2fe6d97a569c6cdac534)
