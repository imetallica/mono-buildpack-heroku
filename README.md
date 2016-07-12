# mono-buildpack-heroku

A buildpack with builds Mono and a solution.

It caches the mono build - which takes about 10 minutes on free dyno. So after first deploy, it should be faster.
Some improvements could still be done, such as:

1. Support FAKE.
2. Support PAKET.
3. Support different Mono versions, so you can upgrade/downgrade your mono installation.

For now, it's using latest Mono (4.4.1.0).
