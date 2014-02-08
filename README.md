okcupid-parser
==============

TODO
==============
- Get OkCupid accounts set up in a variety of cities
- Figure out how to scrape data off of them. Cron? Maybe long running process is better...
- Save data? Don't save data?
- Use classifier, label
- Make tumblr account? Or send back to other users? I think tumblr may be better since our names are going to be public
- Write blog post thing about what we did, how we did it, why we did it, etc
- Write a service that auto-deletes spammy stuff from you inbox (or archives it or something). Maybe this is actually browser extensions!


Install procedure
==============
1. Install and run [Mongodb](http://www.mongodb.org/) on standard port
1. Copy config file ```config/default.js.sample``` to ```config/default.js``` and fill in the appropriate fields

'run' file
==============
- ```./run sandbox``` to run the web app server locally with default port of 4000 (hostname of localhost:4000). Additionally, you can get pretty output via ```./run sandbox | util/pretty.js```
- ```./run production``` to run the server locally using client-side optimized output. This also uses ```config/production.js```
- ```./run test``` to run unit tests
- ```./run lint``` to run js linter

High level framework documentation
==============
The framework is built in layers. Layers can be asynchronous.

1. Routes -- routes for a single resource only to transform parameters (app/routes/)
  - calls middleware for parameter checks (app/middleware)
1. Handlers -- functions that deal with data

Rebase workflow
==============

For collaborators, I prefer [rebase workflow](http://randyfay.com/node/91) as opposed to merge workflow.
