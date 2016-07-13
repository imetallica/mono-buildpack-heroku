# mono-buildpack-heroku

> A buildpack which builds Mono (includes C#), F# and a solution.

Supports C# and F# out of the box.
  - ASP.NET apps should be using the `OWIN.SelfHosting` package and getting the `PORT` variable directly from the environment.
  - If you want to play with F#, there is an WebSharper package here: [SharpHero](https://github.com/imetallica/SharpHero).

It caches the mono and F# builds - which takes about 25 minutes on free dyno. After first deploy, it should be faster.
Some improvements could still be done, such as:

1. Support FAKE.
2. Support PAKET.
3. Support different Mono versions, so you can upgrade/downgrade your mono installation.

For now, it's using latest Mono (4.4.1.0) and F# (4.0.1.1).

Problems:
  - I'm not sure why it's not setting env variables. So, you should copy/paste what's on `/.profile.d/*.sh` and create a `.profile` file on your application repository, so it can set Mono path properly.
  - Test it with more different projects.
