# mono-buildpack-heroku

A buildpack which builds Mono, F# and a solution.

It caches the mono and F# builds - which takes about 25 minutes on free dyno. After first deploy, it should be faster.
Some improvements could still be done, such as:

1. Support FAKE.
2. Support PAKET.
3. Support different Mono versions, so you can upgrade/downgrade your mono installation.

For now, it's using latest Mono (4.4.1.0) and F# (4.0.1.1).
