# Dart hello world for Cloudflare Workers

Your [Dart](https://dart.dev/) code in [index.dart](https://github.com/cloudflare/dart-worker-hello-world/blob/master/index.dart), running on Cloudflare Workers

In addition to [Wrangler](https://github.com/cloudflare/wrangler) you will need to [install Dart](https://dart.dev/get-dart).

#### Wrangler

To generate using [wrangler](https://github.com/cloudflare/wrangler)

```
wrangler generate projectname https://github.com/cloudflare/dart-worker-hello-world
```

Further documentation for Wrangler can be found [here](https://developers.cloudflare.com/workers/tooling/wrangler).

#### Dart

After installing Dart per the linked instructions above,

```
cd projectname

# run once to get dependencies
pub get

dart2js -O2 -o index.js index.dart
```

That will compile your code into index.js, after which you can run `wrangler publish` to push it to Cloudflare.

For more information on how Dart translates to JavaScript, see the [docs for dart2js](https://dart.dev/tools/dart2js) and the [interop guide](https://dart.dev/web/js-interop).