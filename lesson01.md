# faze's crawl guide

**Lesson 1**

---

**Overview**

* glossary
* playing online
* using the bots
* stats
* weapon delay
* weapon choice
* body armour choice
* shields
* character builds
* where to go from here

## glossary

* aut - arbitrary unit of time
* tactical - related to your current situation
* strategic - related to your overall strategy

## play online

1. these putty instructions are from memory, but they should be accurate
1. download http://dobrazupa.org/cszo_key.ppk
1. figure out how to save a session, and make a `cszo` or `crawl` saved session
1. configure putty to connect to ssh `crawl.s-z.org` on port 22 as the user
`crawl` using the cszo_key.ppk as the private key.
1. change character encoding to utf-8
1. set rows to 80, and columns to 24. you must play @ 80x24 to ensure your
games are viewable via footv, the ttyrec request player. 
1. change the font to whichever fixed-width font and font size you prefer.

as an aside, if you have access to a mac/linux machine, run the first command to
grab the key, and the second to connect:

    wget -O ~/.ssh/cszo_key http://dobrazupa.org/cszo_key && chmod 400 ~/.ssh/cszo_key
    ssh -i ~/.ssh/cszo_key crawl@crawl.s-z.org

## bots

1. use an irc client to connect to irc.freenode.net or use webchat.freenode.net
1. join ##crawl
1. if you prefer, or you're going to be looking up tons of stuff, you can start
a query with any of the bots by issuing the command `/q <nick>` in your irc
client. the bots can be queried privately, or from inside ##crawl.

### cheibriados

chei provides information on monsters for the current trunk version and the last
stable version. 

**syntax**: `%??monster` will return an entry detailing statistics for that
monster

chei has a few other functions, but they aren't necessary for you right now

### henzell

henzell hosts the learndb, which is the best source of information about crawl.
it can only be edited publicly, and it is updated quite often. still,
information can be slightly out of date.

**syntax**: `??topic` will return the first page about a topic, and `??topic[n]`
where `n` is the desired entry will return that entry.

### sequell

sequell is a thin wrapper around a postgresql database that keeps track of a
huge amount of information about every game that has been played online. ever.
sequell is also used to request games to be shown on footv. see `??footv` in the
learndb for more info. i could write an entire tutorial just about sequell, but
you are smart enough to learn how it works :P

**syntax**:
https://github.com/greensnark/dcss_henzell/blob/master/docs/listgame.txt

## stats

there are 3 statistics in crawl:

* str
* int
* dex

### str

strength affects how much weight you can carry, and which armours you can wear
without an increased penalty. 

*if your str is 8 or higher and you don't plan on wearing armour heavier than
leather, don't raise str. 

8 str is enough to carry every tactical item you'll need.

*If you have met the str requirements for the armour you plan to wear, don't
raise str. 

in summary, raise str if you need more carrying capacity or you need to meet
armour requirements

### int

if you are casting spells, int is the most important statistic. it affects spell
success and spellpower, both of which are important to a character that casts
spells.  if you cast spells, raise int at every level up as long as you have
enough carrying capacity.

### dex

dex affects dodging, stealth, and stabbing damage. if you are worshipping trog
and you have enough str to wear your desired armour, raise dex. otherwise, you
will rarely choose to raise dex.

## Suggested builds

sedk, polearms, meph, yred. guaranteed win. meph the zombies to hit the monsters.
