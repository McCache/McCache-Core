# McCache Core
This is the base McCache distributed hash table to be wrapper by other languages

## Introduction
This repo at this point in time is to collect ideas for the next version of "McCache for Python".  If we are to port `McCache` to other languages, we should **not** be re-writing `McCache` in the language we are going to port to.  We need a common core where the logic is consistent and tested.

## Ideas
* We should be considering system languages that has a big or up trending following, such as:
  * `C/C++` ,the old faithful.
  * `Rust` ,the current hot kid on the block.
  * `Zig` or `V` ,the up and coming contender.

* Current I am partial to use straight `C`.  The following are some stable libraries that I think we may need to build on:
  * According to this [Hash Benchmark](https://github.com/andremedeiros/hash_benchmark):
    * [Tommy's Dyn Hash](https://www.tommyds.it/doc/tommyhashdyn_8h) seem to be the "best".  We should not pick it just because a benchmark.  Ease of use and maintainability is just as important.
  * [ENet](https://www.npmjs.com/package/enet.c/v/1.4.6?activeTab=readme), a reliable UDP C library, seems to be used to implement online gaming.
  * [NNG](https://github.com/nanomsg/nng), a messaging library, to implement queues.  Or should we stick to `stdlib`?
* [Swig](https://www.swig.org/) is a candidate tool to generate the bindings for the popular languages such as:
  * C#
  * Java
  * Python
  * Ruby
* Extending Python with `C`.
  * https://www.youtube.com/watch?v=HrEzCI3jIHw
  * https://www.youtube.com/watch?v=nHEF1epuuco
  * https://www.youtube.com/watch?v=hPjw7UlcDsc
