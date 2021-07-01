Litecoin Lithium 
===============================


![giphy](https://user-images.githubusercontent.com/73909878/124115687-f50dd600-da22-11eb-8d05-0a576a7c218a.gif)

integration/staging tree
= = = = = = = = = = = = = = = = 
https://litecoin-host.web.app/

Copyright (c) 2021 Litecoin Lithium Developers

What is Litecoin Lithium?
----------------

Lithium is a lite version of Litecoin using scrypt as a proof-of-work algorithm.
 - 2.5 minute block targets
 - subsidy halves in 840k blocks (~4 years)
 - ~84 million total coins

The rest is the same as Bitcoin.
 - 50 coins per block
 - 2021 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the Lithium client sofware, see https://litecoin-host.web.app/

License
-------



Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Lithium
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/lithium-project/lithium/tags) are created
regularly to indicate new official, stable release versions of Lithium.

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
    ./lithium-qt_test

