# Talk proposals

Various talks I’d love to give (linked
to slides/videos if given in the past).



## Persist, Little Objects!

**Accepted to Arrrrcamp 2012, Ghent.**

Object persistence in Ruby is a tricky subject – everyone knows how
to do it (‘simply use an ORM, plug it into a relational database and
you’re done!’), most know the drawbacks (‘well, sure, you need to use
a document database for the more schema-less cases… or serialise the
variable parts… and, of course, object references need to be handled
separately…’), but few experiment with alternatives.

This talk, after recalling the popular database-driven persistence
solutions, concentrates on the less known, but more interesting
and often quite useful approaches – from file-based PStore (ideal
for small apps), through Candy’s out-of-the-way magic, to MagLev’s
true cross-process transparent object persistence.



## C-C-C-Combo Maker

Ruby is a wonderful high-level lanuguage for expressing ideas and
algorithms, but even after the rewriting it umpteen times the most
sophisticated algorithm can be a CPU-bound bottleneck. Similarly,
accessing (especially custom) system devices straight from Ruby is
usually doable, but easier via the provided C drivers.

This talk, based on experience with algorithm optimisation and
custom device drivers gained when working at the Warsaw University
of Technology, shows how easy it is to marry Ruby and C – from writing
MRI-targeting C extensions, through building a proper FFI-oriented
wrapper, to rewriting crucial – and yet, slow – parts of your codebase
in C using RubyInline, without leaving the Ruby method.



## Going Clean and Simple with minitest/spec

The Ruby community is known for praising well-tested code, with
a lot of projects being developed in a test- (or spec-) driven
fashion. minitest/spec is a simple and minimalistic DSL for
behaviour specification and behaviour-driven development, gaining
popularity ever since being a part of Ruby 1.9 standard library.

This talk presents minitest/spec’s virtues and vices, the benefits
and drawbacks of mocking with minitest/mock, as well as the interesting
world of asserting algorithmic performance with minitest/benchmark.



## Ruby on the Command-Line

Ruby, thanks to its various frameworks, is known to be *the* language
for web applications – and recent developments in graphic libraries
make it a worthy contestant in the world of GUI-driven desktop
programs. But Ruby is also great for writing command-line applications;
the ability to mix no-boilerplate toplevel functions with full-fledged
OOP means its usage can vary from one-off trivial scripts to
complicated, option-heavy commandline powerhouses.

This talk presetens the nits and bolts of writing a command-line
application with Ruby – from option parsing and accessing
standard input/output to playing nice with POSIX standards
like exit codes and signal/interrupt handling.



## REST, Assured

Since its first appearance – eleven years ago – REST has grown
from being a PhD dissertation into a widely accepted best practice
when it comes to designing and implementing remote APIs. In the
Ruby world REST started achieving wide recognition four years ago,
and its adoption grew significantly with every subsequent Rails
release – and yet all over the web you can hear grumpy voices
remarking that most services aren’t *really* RESTful, just *kinda*
RESTful, that doing CRUD on resources via HTTP verbs is a nice
starting point, but definitely isn’t enough, and that JSON is
a nice format, but lacks hypermedia vocabulary.

This talk, while briefly refreshing REST basics, concentrates on
the more advanced (as in: not provided by Rails out-of-the-box)
REST ‘features’ and current best practices – explaining why it’s
beneficial to have a discoverable REST design, how to sanely do
API versioning and authentication, and what’s with all this recent
talk about HATEOAS and 100% REST compliance via hypermedia controls.



## Decoupling Persistence (Like There’s Some Tomorrow)

**Given at wroc_love.rb 2012, Wrocław**
([slides](http://decoupling-wrocloverb-2012.heroku.com),
[video](https://www.youtube.com/watch?v=w7Eol9N3jGI))
and **Scottish Ruby Conference 2012, Edinburgh**
([slides](http://talks.chastell.net/src-2012)).

_When I open up a Rails project and the models dir is full of 100%
ActiveRecord classes I shudder. Model ≠ Persistence._ — Ben Mabey

From DCI to presenters, from Uncle Bob’s [architecture
talk](http://confreaks.com/videos/759) and Avdi Grimm’s
[_Objects on Rails_](http://objectsonrails.com) book to
the proliferation of (competing? complementing?) database
systems, it seems the time has come to seriously consider
decoupling our objects’ persistence from the rest of the application.

This talk – after describing the general vices of strong object/database
coupling and the all-too-usual `rails g model`-driven development
– covers the various approaches to separating the objects’ persistence
layer, along with their virtues (cleaner, simpler tests! backend
independence! no RDBMS-related shortcuts impacting the design!)
and potential vices (performance? perceived compexity? YAGNI?).



## Persisting Relations Across Time and Space

**Given at RubyConf 2011, New Orleans**
([slides](http://persistence-rubyconf-2011.heroku.com),
[video](http://confreaks.net/videos/657)).

Entities and their relations are the backbone of most Ruby
applications – from trivial, one-off commandline utilities
to full-blown social network websites. The good old relational
databases, while showing extreme abilities in both adaptation
and survival, are no longer the obvious choice for persistence
– and sometimes obviously not an ideal one.

This talk discusses various entity/relation modeling approaches
and different persistence techniques – from rigid schemas in
suits to collections of hippie free-form documents; from good
old (transactional!) PStore through join-table-happy RDBMS-es
and muscle-flexing NoSQL hools to (social!) graph databases,
waiting patiently for broader recognition and prime time.

Quite a few interesting Ruby libraries for gluing all this together
are also pondered upon – from world-class champions like Active
Record and ARel to less known gems like Candy and Ambition.



## From Profiling Ruby to Frankenstein Programming

**Given at EuRuKo 2010, Cracow**
([slides](http://profiling-ruby-euruko-2010.heroku.com)),
**Ruby and Rails 2010, Amsterdam**
([slides](http://profiling-ruby-rar-2010.heroku.com))
and **Scottish Ruby Conference 2011, Edinburgh**
([slides](http://profiling-ruby-src-2011.heroku.com),
[video](http://confreaks.net/videos/547)).

Ruby is ‘known to be slow’ – but what does that exactly mean, does
it really matter, and – more importantly – what can we do about this?

This presentation, based on hands-on experience of using Ruby for
scientific computations, shows how to profile Ruby applications
(including webapps), how to interpret the results and what to do
with the bottlenecks – from algorithmic optimisation through using
dedicated libraries to rewriting them (in place!) in ‘faster’ languages.



## Bio

Piotr Szotkowski is an assistant professor at Warsaw University of
Technology (where he happily sneaks Ruby, EventMachine and newfangled
database systems into the creaking world of twentieth-century academia),
a Ruby developer at [Rebased](http://rebased.pl) and an alumnus of
[Mendicant University](http://university.rubymendicant.com). He’s
also a long-time contributor to various open source projects for
the civic sector and co-organiser of [NetWtorek](http://netwtorek.pl)
– monthly [NetTuesday](http://netsquared.org/share/meetup)
meetings of people from the NGO/non-profit and IT sectors,
as well as [SocHack](http://sochack.pl) – quarterly 48-hour
hackatons for worthy causes, in coordination with [Random
Hacks of Kindness](http://www.rhok.org), [Open Data
Day](http://www.opendataday.org) and [Open Education
Week](http://www.openeducationweek.org).
