Kakapocoin integration/staging tree
================================

http://www.kakapocoin.org

Copyright (c) 2009 - 2013 Bitcoin Developers
Copyright (c) 2014 - Kakapocoin Developers

What is Kakapocoin?
----------------
The Kakapo Parrot of New Zealand is critically endangered; as of March 2014, with an additional six[4] from the first hatchings since 2011, the total known population is only 130 living individuals. The kakpocoin reflects these numbers in it's configuration.

Kakapocoin is a version Litecoin which in turn is a version of Bitcoin using scrypt as a proof-of-work algorithm.
 - 1.5 minute block targets
 - subsidy halves in 130k blocks (~1.3 years)
 - 130 million total coins
 - 130 coins per block
 - 1300 blocks to retarget difficulty


For more information, as well as an immediately useable, binary version of
the Kakapocoin client sofware, see http://www.kakapocoin.org.

License
-------

Kakapocoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Kakapocoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Kakapocoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./kakapocoin-qt_test

