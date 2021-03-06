!SLIDE bullets
# design(API) #

* ![geemus](../images/geemus.png)
* @geemus (Wesley Beary)
* [heroku](https://heroku.com/home) hacker laureate

!SLIDE[bg=/images/fog.png] background-fit

!SLIDE[bg=/images/heroku.svg] background-fit

!SLIDE bullets
# nom nom

* consuming isn't producing
* consuming is simpler
* (albeit often frustrating)

!SLIDE[bg=/images/design.jpg] background-fit

!SLIDE bullets
# The Feels

* user should feel empowered
* borrow from UX, info design, etc

!SLIDE bullets incremental
# Heroku == my first API!

* no pressure...

!SLIDE bullets incremental
# Let me tell you about API...

* HAD: organic, inconsistent, private
* WANTED: crafted, coherent, public

!SLIDE bullets
# Divide! Conquer?

* extract common patterns
* destroy all snowflakes
* repeat

!SLIDE bullets
# Tedium Ensues

* copy, paste, tweak
* checklist driven development
* hating all of the things

!SLIDE bullets
# Up && Right

!SLIDE[bg=/images/uncle-sam.png] background-fit

!SLIDE bullets
# http api design

* [github.com/interagent/http-api-design](https://github.com/interagent/http-api-design)
* like 12-factor for APIs
* explain feels (WIP)
* patterns rather than solutions

!SLIDE bullets
# describing APIs?

* machine readable, human writable
* json-schema and json hyper-schema
* via yaml

!SLIDE[bg=/images/pyramid-schema.jpg] background-fit

!SLIDE bullets
# manipulating schemata

* [github.com/interagent/prmd](https://github.com/interagent/prmd)
* generators, verifiers, docs, stubs, etc

!SLIDE[bg=/images/owl.png] background-fit
!SLIDE[bg=/images/rest.png] background-fit

!SLIDE bullets
# utilizing schemata

* [github.com/interagent/pliny](https://github.com/interagent/pliny)
* like rails for APIs
* [github.com/interagent/committee](https://github.com/interagent/committee)
* rack middleware for APIs

!SLIDE[bg=/images/umbrellas.jpg] background-fit

!SLIDE bullets
# consuming APIs

* [github.com/excon/excon](https://github.com/excon/excon)
* Usable, fast, simple HTTP 1.1 for Ruby

!SLIDE
# Lessons Learned?

!SLIDE bullets incremental
# nesting(s)?

* `* /parents/{p-id}/children/{c-id}`
* NO!
* `* /children/{c-id}`
* `GET /parents/{p-id}/children/` (maybe)

!SLIDE bullets incremental
# actions/transitions

* `POST /resources/{r-id}/{action}`
* NO!
* `POST /resources/{r-id}/actions/{action}`
* `POST /actions/{action}/resources`

!SLIDE bullets incremental
# singletons

* `* /account/payment-methods`
* NO!
* `* /users/~/payment-methods`

!SLIDE bullets incremental
# YES!

* i/o parity
* UUIDs + friendly
* Request-Ids

!SLIDE bullets incremental
# Development Woes

* steep(ish) learning curve
* seductive specialization

!SLIDE[bg=/images/change.jpg] background-fit

!SLIDE bullets
# Stability (per resource)

* prototype (week)
* development (month)
* production (year)

!SLIDE bullets
# Versioning?

* default :(
* scope? fallbacks?
* multiversion support
* operational overhead

!SLIDE
# Conclusion?

!SLIDE[bg=/images/no-idea.jpg] background-fit

!SLIDE bullets
# Let's be lost together!

* github.com/interagent
* @geemus
* showoff-api-design.herokuapp.com

