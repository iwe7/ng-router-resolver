# ng-router-resolver

> Resolve routes from Angular Module

_Now in POC stage, PRs are welcome!_

This project is aimed to be used as a cli/programmatic tool with Angular projects
to statically analyze routes in `NgModules` and do some useful stuff with it.

As a use case you might want to generate some rules for ServiceWorker based on routes
to add some offline/cache capabilities to any Angular application.

## Usage

It parses given Angular TS module and collects all routes including lazy-routes.

It does not run your Angular app on the server but statically analyzes your code via AST.

### Programmatic

```ts
import { NgRouterResolver } from '../src/resolver';

const routes = NgRouterResolver.fromModule('./src/app/app.module.ts');
```

It will return an array of type same as `Route` from `@angular/route` package.

### CLI

**TBD**

Syntax will be something like this:

```bash
$ ng-router-resolver src/app/app.module.ts
```

## Next Steps

- ~~Collect children routes~~ [DONE]
- ~~Collect lazy routes from other modules~~ [DONE]
- ~~Support Identifiers in routes configuration~~ [DONE]
- ~~Support Spread operators in routes configuration~~ [DONE]
- ~~Collect routes from other impoted modules~~ [DONE]
- ~~Organize internal code structure to transition from POC to some stable version~~ [DONE]
- Create a CLI for resolving routes and dumping them as JSON structure into file

## License

MIT © [Alex Malkevich](malkevich.alex@gmail.com)
