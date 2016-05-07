# Keynote - Brad Green, Google angular team manager guy

* Lots of stuff they're working on for RC
    * Zones
    * Style guide
    * Codealyzer
    * CLI
    * design
        * electon toolkits
        * telerik native UI
        * ng-lightning for SF
        * ng2-bootstrap
        * vaadin web components
* Rangle/Kiva info

# angular universal

Handles rendering, promises, store, state

* Gap events: preboot
* Async: zone.js
* Dependencies: DI

Zone.js for promise transfer

Platform deps pushed to the edge for render

# Brain Stimulation - Dr. Adam Lozano

Brain engineer

Idea: adjusting dials on brain function for those with neurologic or psychia=
tric illness

* movement
* vision
* appetite
* mood
* memory and cognition

## Deep brain stim
Terminal installed in brain, controller elsewhere under skin as with pacemak=
er

### Parkinsons
Before and after - tremors (from 1995)

Stimulator on for 21 years, 5th battery

Ongoing application suppresses symptoms/pathological output

### Dystonia
Typically resulted in death in 3yrs

Added influence to normalize behavior of motor circuit; patient now 26, func=
tioning normally

### Depression

Past electroshock, applied to cv25 area

### Appetite/cognitive function

Severely obese man; burning ventral medial hypothalmus/(sp? Forenix?) result=
s in eating forever (fullness function).  Similar for hunger.  Ask about hun=
ger as inserting electrode.  Triggered memory function; no immediately falsi=
fiable result; memory function through the roof.  Media frenzy.

### Applied to alzheimer's
Childhood memory returned immediately; alzheimers seems to decrease metaboli=
sm; therapy turns glucose metabolism back on.

Progressive alzheimer's atrophies brain; brain grows in patient.  Stimulatio=
n releases growth factors -> brain growth.  Grows at 3x normal rate. =20

## conclusion
Large unmet need (millions) to treat
Several circuits are accessible
Activity can be modulated
Expansion of indications
Multidisciplinary convergence of tech/bio is essential
Hope is to help more patients

# Routing - Misko Hevery
Routing originates in a component using tree mapping of segments.  Arguments=
 can be on a per-segment basis which is nice.  State routing makes more sens=
e to me - URL as an input into initial state and an externalized partial rep=
resentation of application state.  Angular approach to routing loads compone=
nts lazily - component name specified during routing definition.  Lazy loadi=
ng is dependent on directory; CLI intended to mitigate this with code and st=
ructure generation.

# Janet Frazier - Girl Scouts
Importance of women in STEM
81% interested; 13% have STEM as first choice
Main question after initial exposure - can I find a job, succeed, fit in env=
ironment dominated by men?

# The egghead.io guy just got gifted a cat.  Little left field but hey, free=
 cat.  #kittensareforever
# #petebacondarwin - Components Components Components ...  And Angular 1.5
Angular 1 born 2009, kind of like mr miyagi or mickey from rocky

Pete is lead ng1 dev

Components as future of web apps; angular 1.5 <3 components

__App as tree; route to components; unidirectional data flows__

### 3 component roles:
* Presentation
  * stateless-ish
* Business
* bind data to presentation; initiate state changes
  * render other components
* View
  * specialized business components
  * understand router, component tree

### Various syntactic and scoping changes - overview

### Single-direction data binding

### Component enumeration
* Lifecycle
  * $onInit
  * $onDestroy
  * $onChanges

### scope is dead; long live ctrl-component type ish mush

### $componentController
### Says router rooter
RootRouter refactored out
### Further reading
On the github
# Dave - vmware
UA Arch @ vmware
VMWare runs submarines && helos
Betting the house on angular
### ng-challenge
Stuff for coding competition/recruiting
# igor & vanessa - augury
### looking deeply into app
* __injector graph__
* __router tree__

Github.com/rangle/augury
augury.angular.io

# kara erickson and jeremy elbourn - angular material 2 - "titanium octopus"=

### New in 2 (1.1.0 for ng2)
* $mdColors
* $mdPanel
* Sample apps

### Puppy Love demo - dating app for dogs
* Add imports/deps
* theme has default colors for customization on top of palette
* use components, directives, etc
* component interactions  by ref (onclick -> thing.open)
* __doge ipsum__ - http://dogeipsum.github.io
* Tweak repr - standard CSS overrides
* md-card > md-card-image, md-card-title, md-card-title, ...
* css display flex/etc - I'm behind :/
* md-fab fabrication? For toggle

### Alpha state
Working on test/deploy/doc/new features
Screenshot tests (ex: baseline unexpectedly moves)
Accessibility tests - what screenreader reads/etc
### Component toolkit
* overlays
* mobile
  * gestures
  * responsive
  * accessibility
* a11y
* more
  * virt scrolling
  * selection model
  * testing utils
 =20
### WHEN WHEN WHEN
Parity with ng1 -> beta, 2016
Add advanced stuff sometime

github.com/kara/puppy-love @karaforthewin @jelbourn ?

# Julie Ralph - Protractor - Testing your tasks
### Testing zones
Zone is effectively an isolated execution context; zones have hierarchy and f=
ork kind of like processes (but no PIDs)

### Zone API
Missed, like ngz but moar

### Event loop model
* microtask queue (promises)
* macrotask queue (xhr/timeouts)
* event task (user input)

Zone spec

### Ng2 change detection
Runs on ngZone.onMicroTaskEmpty()=20

### NgZone API
* onMicroEmpty
* onError
* run
* runOutsideAngular
runOutside lets you do timeouts/etc without change detection (things UI does=
n't care about)

### E2E testing - avoiding test flakes and race conditions
Test asks "is page stable?" =3D are queues empty?

### setInterval falls apart =3D ?
exit zone to start interval, re-enter to trigger update (use scope/etc)

### Unit Testing
Async and testAsync test helpers, wrap test function in async wrappers

Wrappers track tasks, time out, ensures clean zones, etc...  It('stuff', asy=
nc(() =3D> { ... Tests here ... })

#### builder.createAsync - nonprecise timing for tests

#### fakeAsync - precise timing control
tick() to control clock
Warns on pending queue at the end of time; drains microtasks each tick



# Anas Firdousi - functional reactive
Great way to to get talk spots

### Functional (as in a mathematical function)
* Separation is good
* reduce random ghost inputs/etc
* separate mutation from calculation
* independent calculation pipelines (example with compose pipeline)

#### Pure functions

* mapping
* one to one function of {range =3D> domain}
* ?
* ?
* ...  __Reducers__
* time travel with purity
* implications for angular universal
* makes fns
* Purity is:
* reliable
* testable
* portable
* memoizable
* parallelizable

#### Currying
#### Composition of functions
#### Functors and Monads
Functor is an object you can map over
Chaining maps =3D pretty sweet
Maybe functor to handle errors in chains
mjoin is to objects as flatten is to arrays
### Reactive
Bacon/.../rx?

Programming with async data streams

Makes async easy to think about

#### Patterns behind patterns
Observer pattern - observer, observable; subscriptions, etc...  Map/filter/r=
educe to maintain application state

Push v pull

Nothing is not a stream - events, time, data inputs, av, services, forms, sp=
eech, ...

##### Iterator Pattern
Iterate the same way over everything - polymorphic traversal of collections (=
streams)

Linked list model - hasNext(), etc

### streams over time
Merge streams of user input over time (reactive user interfaces)
### reactions over time
All inputs are observable in ng2, #4062

###=20