---
layout: post
title:  "The FULL significance of the 12 Factor App mindset"
date:   2017-01-01 17:00:00
categories: Philosophy
---

# [Twelve Factor apps](http://12factor.net/) have become absolutely NECESSARY in the softare-as-a-service realm ... but there is a LUCKY 13th factor that is essential for NEW work.
The twelve factors given below are not goals; they are requirements.  If we cannot meet the [twelve factor](http://12factor.net/) requirements, we should not pollute the world with our careless, reckless, ill-conceived app.  The [twelve factor](http://12factor.net/) format is inspired by Martin Fowler’s books [Patterns of Enterprise Application Architecture and Refactoring](https://www.safaribooksonline.com/library/view/patterns-of-enterprise/0321127420/).

But the 12 factors need to reconcieved ... in less trusting, less naive, more paranoid manner  that focuses on security rather than feature bloat. A much less trusting mindset is necessary develop more secure, reliable, scalable, survivable system ... fundamentally, this means that the back-end datastores must be designed for survivability, in radically more decentralized and more distributed, *eg at least CockroachDB, probably blockchain* ... the MOST necessary thing about an app happens BEFORE you start PRACTICING WRITING CODE for a new product ... BEFORE YOU START monkeying around with code, before you start thinking about architecture, it is important to not just conceive of a new [incrementally-better] product [because that's what you will do AFTER you have a new product] ... the first thing that you must do is reconceive the customers for a new emergent product ... the process of becoming [something more], becoming emergent must be and can be continually created, re-created, reconceived.  

This means moving from an "Application Platform-as-a-Service" to a "Container Platform-as-a-Service" to in order to enable [a more highly distributed SQL database with support for ACID transactions, horizontal scalability and survivability](https://github.com/cockroachdb/cockroach#design).  The ultimate intent is a radically more diffuse, distributed, decentralized transaction database using blockchain architecture.  In highly distributed systems [like bitcoin], suspicion, pessimism and paranoia are used as architecture requirements to build highly reliable systems from extremely unreliable, untrustworthy components ... which is possible by focusing on the most core elements of a transaction and assuming throughout the design process that all nodes and channels of the network, as well as all bots or participants that might use the system are untrustworthy even potentially malicious.  

But the 12 Factor App mindset STILL matters ... let's look at WHY.


## I. Version-Controlled Codebase / Blog
There can be many deployments, but a twelve-factor app is ALWAYS tracked in a version control system, such as Git, Mercurial, or Subversion. ALWAYS! ALWAYS! ALWAYS!  And "ALWAYS!" means that it necessary to center an workflow around the code repositories in version control system ... for example, meetings should not be physical, but instead be conducted via repository-centric chat with archived transcripts.

## II. Dependencies
A twelve-factor app never relies on implicit existence of system-wide packages. It declares all dependencies, completely and exactly, via a dependency declaration manifest.  

## III. Config
The twelve-factor app stores config in environment variables (often shortened to env vars or env). Env vars are easy to change between deploys without changing any code; unlike config files, there is little chance of them being checked into the code repo accidentally. In a twelve-factor app, env vars are granular controls, each fully orthogonal to other env vars. They are never grouped together as “environments”, but instead are independently managed for each deploy.

## IV. Backing Services
A backing service is any service the app consumes over the network as part of its normal operation. Examples include datastores (such as MySQL or CouchDB), messaging/queueing systems (such as RabbitMQ or Beanstalkd), SMTP services for outbound email (such as Postfix), and caching systems (such as Memcached). The code for a twelve-factor app made no distinction between local and third party services. To the app, both are attached resources, accessed via a URL or other locator/credentials stored in the config ... but our new architecture requirements will force to build highly reliable backing service systems from extremely unreliable, untrustworthy components.

## V. Build, release, run
The twelve-factor app uses strict separation between the build, release, and run stages. Every release should always have a unique release ID, such as a timestamp of the release (such as 2011-04-06-20:32:17) or an incrementing number (such as v100). Releases are an append-only ledger and a release cannot be mutated once it is created. Any change MUST create a new release.

## VI. Processes
Twelve-factor processes are necessarily stateless and must be constructed so that they don't persist and share almost nothing. The rare data that needs to persist must be stored in a stateful backing service, typically a highly-distributed database system. The memory space or filesystem of the process should be used as a momentarily brief, single-transaction cache pulling from a *Cockroach-ey* database system with support for ACID transactions, horizontal scalability and survivability](https://github.com/cockroachdb/cockroach#design).  

## VII. Port binding
The twelve-factor app is completely self-contained and does not rely on runtime injection of a webserver into the execution environment to create a web-facing service. Typically, the web app exports HTTP as a service by binding to a port, and listening to requests coming in on that port. HTTP is not the only service that can be exported by port binding. Nearly any kind of server software can be run via a process binding to a port and awaiting incoming requests. Examples include ejabberd (speaking XMPP), and Redis (speaking the Redis protocol).

## VIII. Concurrency
In the twelve-factor app, processes are a first class citizen. Processes in the twelve-factor app take strong cues from the [unix process model for running service daemons](http://adam.herokuapp.com/past/2011/5/9/applying_the_unix_process_model_to_web_apps/).

## IX. Disposability
The twelve-factor app’s processes must be disposable and destroyable, meaning they must be started or stopped at a moment’s notice ... the more temporary the better. This facilitates fast elastic scaling, rapid deployment of code or config changes, and robustness of production deploys.

## X. Dev/prod parity
The twelve-factor app is designed for continuous deployment by making the gap between development and production as small as possible... make the time gap small ... make the personnel gap small ... make the tools gap small.

## XI. Logs
A twelve-factor app never concerns itself with routing or storage of its output stream. It should not attempt to write to or manage logfiles -- it must assume that logging will tend to attract malicious use.

## XII. Admin processes
Run admin/management tasks as one-off processes. One-off admin processes should be run in an identical environment as the regular long-running processes of the app. They run against a release, using the same codebase and config as any process run against that release. Admin code must ship with application code to avoid synchronization issues.
