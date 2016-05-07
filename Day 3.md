# Brief history of Promises - Sam Mccone
Sync/async

### ryan dahl 2009 nodejs
Server-side, had promises

Promise was event emitter in first node commit

* thunks 1961
* futures 1977
* ... Deferred ...

### NASA 1961 - chimps into space - Algo Thunks
Leaves result in standard address space

### Futures - GC, 1977
Each formal param bound to separate process

### Joule Channel, 1995
Dataflow spread out through space

### E Lang - 1997
Non-blocking promises; promise, resolution, broken, local/remote

### Python Twisted Deferred, 2001

### JS Port 2005 - MochiKit
### Dojo, 2006
### Waterken Q, 2009
Made interacting with JSON endpoints easy
### Q, 2009?
#### Angular $q
#### jQuery, 2010
#### $.ajax(), 2010
#### API briar patch
#### A+ unification, 2012ish - then() always works
#### promises in es2015 tc39

# Multi-slot Transclusion - Ken Snyder
New in ng1.5, 2

Transplants multiple DOM nodes from one spot to another

Scopes still separated

Specify transclude: {dest: source, dest2: source2} in component/directive de=
finitions

shar.pn/flip
shar.pn/flip2

# ng2 animations
Nice API, missed a good bit of the talk; API is finalized, RC in the bext se=
veral weeks - working on CSS selectors, etc

# ng2 cli - Mike Brocchi
### CLI can
* Init
* Build
* Test
* e2e test
* Serve
* Deploy
* Generate components, services, pipes, routes, directives, classes

Generators also generate specs, units

Pro tip: live-type  your demo using snippets


Shorthand: ng g r =3D> ng generate route

At beta as of yesterday

Roadmap -
* Offline template compilation
* Lazy loading routes
* 3rd party addons
* Angular upgrades (code gen)
* CI integration
* Produce angular packages
* More customizations

# ng2 for the rest of us - Scott Moss
#### Build fun things and compare with what you already know
Knew 2015, build sys, angular 1
Didn't know observables, zone.js, typescript, angular 2

#### Started with docs, frustration
#### Learned typescript
Thought it was Java (was right IRL)

#### Component
Components are basically directives with templates
Decorators on properties
App is just a tree of components
Inputs, outputs define interfaces
Use lifecycle methods and builtin decorators for DOM interactions

#### Services
DI requires ts decorators - use @Injectable()
Service is just a class
Choose wisely where you provide your services

#### Observables and rxJs
Use observables for async as well

Use observables for:
* querying DOM
* UI
* HTTP

#### Tough stuff was ng choices, not NG
#### error driven learning
Zone gives really good responses
####  Adopt the "there's a thing for that" mentality
# NG react native renderer - Marc Laval
_Check out kitchen sink app_

ngReactNative project

Appium

Angular/react-native-renderer
mlaval/angular-react-native-seed

# Reactive - Matt Podwysocki
Alternative to promises
Chain events -> filters -> mutations -> reduction -> response/representation=


React to load, failure, users

1994, gang of 4 - difference btw iterable and events?  Events are just in ti=
me.

Observable is just subject/observer done right

Grammar, async values

Zen - everything is a stream

Must FlatMap it

Cancellation cleans entire event stream

ngrx are cool

Redux implemented as scan()

Standardizing is es2017

http://github.com/mattpodwysocki/ng-conf-2016

# Async with AngularFire - David East
Database as an observable

Yep, that's pretty much it.
