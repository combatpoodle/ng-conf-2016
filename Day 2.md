# electron
onehungrymind/electrogram repo, user is ??

## 01 - electron

* install electron-prebuilt
* main.js
* run electron
* create start task - electron main.js

Internet is down, talk rework on the fly; slides should be posted at some po=
int

createwindow =3D main
index.html hello world

## 02 - adding angular
Angular just goes in src or app

Tweak build system

Webpack electron-renderer

ts-loader

Add app tag for angular2 to populate; something about electron output

## ??? -> be an expert (no explanation given)

# Becoming an ng2 contributor - alexcastillo
Feedback: https://ow.ly/4nrlo3

Gitter: https://gitter.im/ng-contrib/angular

https://ng-contrib.org

Review of pull request process

ng-contrib info to align to language/etc; CLA; bot associates CLA to PRs and=
 flags

http://castillo.io


# Angular + Webpack - Sean Larkin
### Javascript modules
... What is, How to use/etc...

Web app bundling

### Webpack =3D module bundler
Looks at everything as modules (JS, CSS, etc)

#### how to use
* webpack.config.js
* webpack cli

### Core Concepts
#### Entry
The contextual root of the application (from which other deps are tracked)

Can be array (browser, vendor, etc)

#### Output
Path, filename, translators, etc
Output =3D bundle for single page app

Multi entry - web/mobile/desktop for separate bundles; separate library targ=
ets, etc

#### Loaders
This is common point of trouble - ts, babel, css, etc

Loaders indicate tool used to consume resources; tell webpack how to load an=
d translate

{test: /\.ts$/, loader: 'ts'}

Props: test, loader, loaders, include, exclude

Also check out preLoaders (lint), postLoaders (?) - parallel to loaders in c=
onfig

##### Chaining loaders
loaders: ['style', 'css', 'less']

Chain is Right to Left

### Plugins
Is an es5 class which implements apply() for compilation

Pass to plugins array as  class instance

Check bell-on-error; webpack.optimize.UglifyJsUgin, webpack.optimize.Commons=
ChunkPlugin

### Future
Just one guy working on it, a few hours a week

##### Webpack 2
* native es2015 support
* Tree shaking
* faster compilation
* More builtin optimizations

## ng2 webpack
Patrick Stapleton is smart guy - AngularClass/angular-webpack-starter, angul=
ar-webpack-lite, ...

## midwest dev chat on slack

# Horizon stack
Horizon client
Horizon Server
RethinkDB

Framework-agnostic
Kubernetes pre-built

### Deps and install
* Rethink
* node
* np m install -g horizon
* hz init mypronect
* hz serve [--dev] (dev changes i dex behavior)

### Client API
#### Collections (json docs)
* Queries return cursors of rxjs observables=20
Simar to activerecord/promise chains

* find, findAll, ...

### Horizon API
### Observables
Reactive extensions to JS
### Realtime updates
Add .watch() to query; default is to broadcast entire set; can send deltas a=
s needed

Individual changes with raw hanges: true - includes old_val, new_val

### Available today
* Store over WS
* Track live updates
* ...
* oauth

Soon

* schema
* ACL
* Admin UI
* Optimistic updates
* graphql, falcor - supposedly really cool; falcor is infinite stream of dat=
a

### Clusters/cloud with horizon cloud

### Involvement

http://horizon.io

### Angular2
github.com/rethinkdb/typescript-horizon-workshop
